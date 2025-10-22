# CS 260 Notes

[My startup - Simon](https://simon.cs260.click)

## Helpful links

- [Course instruction](https://github.com/webprogramming260)
- [Canvas](https://byu.instructure.com)
- [MDN](https://developer.mozilla.org)

## AWS

My IP address is: 54.81.96.130
Launching my AMI I initially put it on a private subnet. Even though it had a public IP address and the security group was right, I wasn't able to connect to it.

## Caddy

No problems worked just like it said in the [instruction](https://github.com/webprogramming260/.github/blob/main/profile/webServers/https/https.md).

## HTML

target = -none -> open on a different page 
there are a ton of aria tags (e.g. aria-expanded = whether it is in a state of expanded or not)

## CSS
Cascading Style Sheets -> transforms HTML into an experience 
rules -> selector -> declarations -> property -> property value 
rule = p(selector){colour(property):(declaration) green (value);}

Three ways to apply CSS
1) style 
    <p style="colour:green"> CSS</p>
2) style element in head element of document -> apply to whole document 
    <head><style> p {color: green;} </style></head>
3) HTML syntax <link> *
hyperlink reference to an external file with css rules
must be in head element of document 

innermost box (content)-> padding (background colour) -> border (colour, thickness and line style)-> margin 



SELECTORS

Element type selector 
whole sections, eg: body, h1, etc

Combinators 
descendant combinator -> section h2{....}
sibling, parent, etc 
Helps put specific css in a smaller section 
sec

Class selector
.summary{}
p.summary{}

ID Selector 
#physics{xyz}

Attribute selector 
certain classificant and referenced attribute 
p{class='summary'={....}}

Pseudo Selector
special circumstances -> hovering over element, etc
section:hover{xyz} 



DECLARATIONS
specify changes when selector matches 
units -> px, pt (1/72 of inch), in, cm, %, em, rem, ex, vw, vh, vmin, vmax
colour -> keyword, rgb hex, rgb function, hsl, 

Vue, Svelte -> Combines HTML, CSS, JavaScript into a single file 
but Svelte needs a compiler, but Vue doesn't

React -> combines Javascript and HTML
css must be declared out side JSX file 

Angular Component -> seperate files, chose when to combine 


This took a couple hours to get it how I wanted. It was important to make it responsive and Bootstrap helped with that. It looks great on all kinds of screen sizes.

Bootstrap seems a bit like magic. It styles things nicely, but is very opinionated. You either do, or you do not. There doesn't seem to be much in between.

I did like the navbar it made it super easy to build a responsive header.

```html
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container-fluid">
          <a class="navbar-brand">
            <img src="logo.svg" width="30" height="30" class="d-inline-block align-top" alt="" />
            Calmer
          </a>
          <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent">
            <span class="navbar-toggler-icon"></span>
          </button>
          <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
              <li class="nav-item">
                <a class="nav-link active" href="play.html">Play</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="about.html">About</a>
              </li>
              <li class="nav-item">
                <a class="nav-link" href="index.html">Logout</a>
              </li>
            </ul>
          </div>
        </div>
      </nav>
    </header>
```

I also used SVG to make the icon and logo for the app. This turned out to be a piece of cake.

```html
<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg">
  <rect width="100" height="100" fill="#0066aa" rx="10" ry="10" />
  <text x="50%" y="50%" dominant-baseline="central" text-anchor="middle" font-size="72" font-family="Arial" fill="white">C</text>
</svg>
```

## React Part 1: Routing

Setting up Vite and React was pretty simple. I had a bit of trouble because of conflicting CSS. This isn't as straight forward as you would find with Svelte or Vue, but I made it work in the end. If there was a ton of CSS it would be a real problem. It sure was nice to have the code structured in a more usable way.

## React Part 2: Reactivity

This was a lot of fun to see it all come together. I had to keep remembering to use React state instead of just manipulating the DOM directly.

Handling the toggling of the checkboxes was particularly interesting.

```jsx
<div className="input-group sound-button-container">
  {calmSoundTypes.map((sound, index) => (
    <div key={index} className="form-check form-switch">
      <input
        className="form-check-input"
        type="checkbox"
        value={sound}
        id={sound}
        onChange={() => togglePlay(sound)}
        checked={selectedSounds.includes(sound)}
      ></input>
      <label className="form-check-label" htmlFor={sound}>
        {sound}
      </label>
    </div>
  ))}
</div>
```

#Midterm
In the following code, what does the link element do?
In the following code,  what does a div tag do?
In the following code, what is the difference between the #title and .grid selector?
In the following code, what is the difference between padding and margin?
Given this HTML and this CSS how will the images be displayed using flex?
What does the following padding CSS do?
What does the following code using arrow syntax function declaration do?
What does the following code using map with an array output?
What does the following code output using getElementByID and addEventListener?
What does the following line of Javascript do using a # selector?
Which of the following are true? (mark all that are true about the DOM)
By default, the HTML span element has a default CSS display property value of: 
How would you use CSS to change all the div elements to have a background color of red?
How would you display an image with a hyperlink in HTML?
In the CSS box model, what is the ordering of the box layers starting at the inside and working out?
Given the following HTML, what CSS would you use to set the text "trouble" to green and leave the "double" text unaffected?
What will the following code output when executed using a for loop and console.log?
How would you use JavaScript to select an element with the id of “byu” and change the text color of that element to green?
What is the opening HTML tag for a paragraph, ordered list, unordered list, second level heading, first level heading, third level heading?
How do you declare the document type to be html?
What is valid javascript syntax for if, else, for, while, switch statements?
What is the correct syntax for creating a javascript object?
Is it possible to add new properties to javascript objects?
If you want to include JavaScript on an HTML page, which tag do you use?
Given the following HTML, what JavaScript could you use to set the text "animal" to "crow" and leave the "fish" text unaffected?
Which of the following correctly describes JSON?
What does the console command chmod, pwd, cd, ls, vim, nano, mkdir, mv, rm, man, ssh, ps, wget, sudo  do?
Which of the following console command creates a remote shell session?
Which of the following is true when the -la parameter is specified for the ls console command?
Which of the following is true for the domain name banana.fruit.bozo.click, which is the top level domain, which is a subdomain, which is a root domain?
Is a web certificate is necessary to use HTTPS.
Can a DNS A record can point to an IP address or another A record.
Port 443, 80, 22 is reserved for which protocol?
What will the following code using Promises output when executed?
