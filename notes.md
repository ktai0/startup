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
there are inherited and non-inherited declarations

Three ways to apply CSS
1) style 
    <p style="colour:green"> CSS</p>
2) style element in head element of document -> apply to whole document 
    <head><style> p {color: green;} </style></head>
3) HTML syntax <link> *
hyperlink reference to an external file with css rules
must be in head element of document 

innermost box (content)-> padding (background colour) -> border (colour, thickness and line style)-> margin 



### css-SELECTORS
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



### css-DECLARATIONS
specify changes when selector matches 
units -> px, pt (1/72 of inch), in, cm, %, em, rem, ex, vw, vh, vmin, vmax
colour -> keyword, rgb hex, rgb function, hsl, 

### css-fonts
serif -little stroke attached 
sans-serif -> no stroke

importing fonts
@font-face {font-family: 'quicksand';src:url(...');}

@import url('....')
p{font-family: 'name'}

### css-Animation 
1) define the animation name & duration 
  p{text:.... font:.... animation-name:... animation-duration: xs;}
2) define keyframes 
  @keyframes (animation-name) {
    from{
      font-size: 0vh;
    }
    to {
      font-size:20vh; 
    }
  }

### CSS debugging
  html page element -> inspect 

### Responsive design 
changes display for desktops, mobile phones, kiosks, etc... 

1. Display property 
html -> div class ="xyz"    css -> .xyz{display: xyz}
xyz= 
1) none -> dont display 
2) block -> fill parent element width 
3) inline -> as big as its content (e.g # of char)
4) flex -> element's children in flexible orientation 
5) grid -> element's children in grid orientation 

2. meta tag 
Do not scale -> 
<meta name="viewport" content="width=device-width,initial-scale=1" />

3. Float 
arrange element to left or right in proportion to another element
e.g. wrap text around picture, moves when display parameters changes.

4. Media 
automatically detects size of webpage and coonsults css rules to change 
@media (orientaton: xyz){ div{ transform:...;}}
boolean 

### CSS - GRID
helps with responsive grids 
html -> <div class="parentElement"> ..... </div>
css -> .parentElement{ 
  display: grid;
  grid-template-columns: repeat (auto-fill, minmax(300px,1fr)(layout of grid columns) 
  grid-auto-rows: height of row 
  grid-gap: ... 
}


### CSS-flexbox
compartamentalization of website so it moves around eachother as the web size changes 
display: flex;

justify-content -> align the content horizontally within box 
align-content -> align the content veritcally within box


### CSS-frameworks
set package of css rules through open source 

1) Tailwind 
  smaller definitions applied to individual HTML elements
  moves css rules out of css file and into HTML

2) Bootstrap
  CDN + add HTML link + Bootstrap javascript module a the end of body 
  <!DOCTYPE html>
<html lang="en">
  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-rbsA2VBKQhggwzxH7pPCaAqO46MgnOM80zW1RWuH61DGLwZJEdK2Kadq2F9CUG65" crossorigin="anonymous" />
  </head>
  <body>
    ...
  </body>
</html>

if need javascript 
<body>
  ...

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js" integrity="sha384-kenU1KFdBIe4zVF0s0G1M5b4hcpxyD9F7jL+jjXkk+Q2h455rYXK/7HAuoJl+0I4" crossorigin="anonymous"></script>
</body>

// Bootstrap styled button
<button type="button" class="btn btn-primary">Bootstrap</button>

// Default browser styled button
<button type="button">Plain</button>

## Javascript
most used language, goes through interpreter

console.log -> print function 
console.log('hello'+' '+'world') -> hello world 

JavaScript console -> JS debugger console 
Log's the outputs
times the run time of code 
count how many times a block of code is called

### Functions
zero or more parameters 
zero or more return statements 
no type declarations 

function labeler(value, title = 'title') {
  console.log(`${title}=${value}`);
}
labeler();
// OUTPUT: title=undefined
labeler('fish');
// OUTPUT: title=fish
labeler('fish', 'animal');
// OUTPUT: animal=fish

anonymous functions -> no name functions 
const add = function (a, b) {
  return a + b;
};

### arrow function 
=> is the function keyword 

const a = [1, 2, 3, 4];

// standard function syntax
a.sort(function (v1, v2) {
  return v1 - v2;
});

// arrow function syntax
a.sort((v1, v2) => v1 - v2);

if no curly braces -> no need for return keyword

closure ???

### array 
The Array object has several interesting static functions associated with it. Here are some of the interesting ones.

| Function | Meaning                                                   | Example                       |
| -------- | --------------------------------------------------------- | ----------------------------- |
| push     | Add an item to the end of the array                       | `a.push(4)`                   |
| pop      | Remove an item from the end of the array                  | `x = a.pop()`                 |
| slice    | Return a sub-array                                        | `a.slice(1,-1)`               |
| sort     | Run a function to sort an array in place                  | `a.sort((a,b) => b-a)`        |
| values   | Creates an iterator for use with a `for of` loop          | `for (i of a.values()) {...}` |
| find     | Find the first item satisfied by a test function          | `a.find(i => i < 2)`          |
| forEach  | Run a function on each array item                         | `a.forEach(console.log)`      |
| reduce   | Run a function to reduce each array item to a single item | `a.reduce((a, c) => a + c)`   |
| map      | Run a function to map an array to a new array             | `a.map(i => i+i)`             |
| filter   | Run a function to remove items                            | `a.filter(i => i%2)`          |
| every    | Run a function to test if all items match                 | `a.every(i => i < 3)`         |
| some     | Run a function to test if any items match                 | `a.some(i => i < 1)`          |


### OBJECT 
A JavaScript object represents a collection of name value pairs referred to as properties. The property name must be of type String or Symbol, but the value can be of any type. Objects also have common object-oriented functionality such as constructors, a this pointer, static properties and functions, and inheritance.

Objects can be created with the new operator.

Any function that returns an object is considered a constructor and can be invoked with the new operator.
function Person(name) {
  return {
    name: name,
  };
}

const p = new Person('Eich');
console.log(p);
// OUTPUT: {name: 'Eich'}

inheritence 
class Person {
  constructor(name) {
    this.name = name;
  }

  print() {
    return 'My name is ' + this.name;
  }
}

class Employee extends Person {
  constructor(name, position) {
    super(name);
    this.position = position;
  }

  print() {
    return super.print() + '. I am a ' + this.position;
  }
}

const e = new Employee('Eich', 'programmer');
console.log(e.print());
// OUTPUT: My name is Eich. I am a programmer


### JSON
JSON provides a simple, and yet effective way, to share and store data. By design JSON is easily convertible to, and from, JavaScript objects. This makes it a very convenient data format when working with web technologies. Because of its simplicity, standardization, and compatibility with JavaScript, JSON has become one of the world's most popular data formats.


Most commonly, a JSON document contains an object. Objects contain zero or more key value pairs. The key is always a string, and the value must be one of the valid JSON data types. Key value pairs are delimited with commas. Curly braces delimit an object, square brackets and commas delimit arrays, and strings are always delimited with double quotes.

You can convert JSON to, and from, JavaScript using the JSON.parse and JSON.stringify functions.

### adding to HTML
1) script block: <script></script> write code between script
2) external code: reference external file <script src='xyz'></script>
3) inline event attribute: create script first, and then use content in an inline piece of code

## Node
one language to run all of your server
1. Create your project directory
2. Initialize it for use with NPM by running npm init -y
3. Make sure .gitignore file contains node_modules
4. Install any desired packages with npm install <package name here>
5. Add require('<package name here>') to your application's JavaScript
6. Use the code the package provides in your JavaScript
7. Run your code with node index.js

### Debugging Node
frequent console.log functions

## web frameworks 
Vue, Svelte -> Combines HTML, CSS, JavaScript into a single file 
but Svelte needs a compiler, but Vue doesn't

React -> combines Javascript and HTML
css must be declared out side JSX file 

Angular Component -> seperate files, chose when to combine 

## Toolchains
Code repository - shared code 
Linter - makes the code properly formated, effecient 
Prettier - Formats code according to a shared standard.
Transpiler - Compiles code into a different format. For example, from JSX to JavaScript, TypeScript to JavaScript, or SCSS to CSS.
Polyfill - Generates backward compatible code for supporting old browser versions that do not support the latest standards.
Bundler - Packages code into bundles for delivery to the browser. This enables compatibility (for example with ES6 module support), or performance (with lazy loading).
Minifier - Removes whitespace and renames variables in order to make code smaller and more efficient to deploy.
Testing - Automated tests at multiple levels to ensure correctness.
Deployment - Automated packaging and delivery of code from the development environment to the production environment.

vite is a tool chain pack ?

## components 
JSX -> takes react, return and inserts into HTML
modularise back end code to represent front end compartments 
generate user interface -> JSX
rendering JSX -> through funciton or even through inline 

## React Part 1: Routing

Helps make what would be a multi page hmtl file set up, into a seamless one page html user experience. Basicallya compartamentalise the content, so content loads different times, but the headers/footers don't reload. 

function Page({ color }) {
  return (
    <div className="page" style={{ backgroundColor: color }}>
      <h1>{color}</h1>
    </div>
  );
}

function App() {
  return (
    <BrowserRouter>
      <div className="app">
        <nav>
          <NavLink to="/">Red</NavLink>
          <NavLink to="/green">Green</NavLink>
          <NavLink to="/blue">Blue</NavLink>
        </nav>

        <main>
          <Routes>
            <Route path="/" element={<Page color="red" />} exact />
            <Route path="/green" element={<Page color="green" />} />
            <Route path="/blue" element={<Page color="blue" />} />
          </Routes>
        </main>
      </div>
    </BrowserRouter>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);

## React Part 2: Reactivity

This was a lot of fun to see it all come together. I had to keep remembering to use React state instead of just manipulating the DOM directly.

Handling the toggling of the checkboxes was particularly interesting.

```jsx -> allows for html like markups even in javascript
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
  link references ? URL ?
In the following code,  what does a div tag do?
  creates a division element in the html 
In the following code, what is the difference between the #title and .grid selector?
  #title references an ID, .grid references class 
In the following code, what is the difference between padding and margin?
  padding is the space inside the border, margin is the space outside the border 
Given this HTML and this CSS how will the images be displayed using flex?
  flex row -> in a line 
  flex column -> up and down 
What does the following padding CSS do?
  creates space on top and bottom, and then left and right 
What does the following code using arrow syntax function declaration do?
  creates .... 
What does the following code using map with an array output?
  copies and mutates the array without changing original array 
What does the following code output using getElementByID and addEventListener?
  Typical pattern:
  const btn = document.getElementById('btn');
  btn.addEventListener('click', () => console.log('Clicked!'));
  Behavior: When user clicks the element with id 'btn', the callback runs and prints 'Clicked!'.
What does the following line of Javascript do using a # selector?
  document.querySelector('#title') selects the first element that matches the CSS selector #title (elemequerySelector accepts any CSS selector (classes, attributes, pseudos).
Which of the following are true? (mark all that are true about the DOM)
  everything is a node in the DOM, document object model 
By default, the HTML span element has a default CSS display property value of: 
    inline
How would you use CSS to change all the div elements to have a background color of red?
    .div {background-color: red;}
How would you display an image with a hyperlink in HTML?
    <a href="https://example.com">
    <img src="logo.png" alt="logo">
    </a>
In the CSS box model, what is the ordering of the box layers starting at the inside and working out? 
  content, padding, border, margin 
Given the following HTML, what CSS would you use to set the text "trouble" to green and leave the "double" text unaffected?
  span
  Given <p><span class="trouble">trouble</span> double</p>, use .trouble { color: green; }
What will the following code output when executed using a for loop and console.log?

How would you use JavaScript to select an element with the id of “byu” and change the text color of that element to green?
  const byu = document.getElementById('byu');
  byu.style.color = 'green';
What is the opening HTML tag for a paragraph, ordered list, unordered list, second level heading, first level heading, third level heading?
<p><ol><ul><h2><h1><h3>
How do you declare the document type to be html?
<!Doctype html>
What is valid javascript syntax for if, else, for, while, switch statements?
  if (x > 5) { ... } else { ... } for (...) { ... } while (...) { ... } switch (x) { case 1: ...; break; default: ... }
What is the correct syntax for creating a javascript object?
  const person = { name: "John", age: 30 };
Is it possible to add new properties to javascript objects?
  yes, person.city = "Provo";
If you want to include JavaScript on an HTML page, which tag do you use?
  <script src="script.js"></script>
Given the following HTML, what JavaScript could you use to set the text "animal" to "crow" and leave the "fish" text unaffected?
  <p id="animal">animal</p>
  <p id="fish">fish</p>
  
  const animal = document.getElementById('animal');
  animal.textContent = 'crow';
Which of the following correctly describes JSON?
  JSON (JavaScript Object Notation) is a text-based format for structured data using key-value pairs. Example: {
  "name": "John", "age": 25 }
What does the console command chmod, pwd, cd, ls, vim, nano, mkdir, mv, rm, man, ssh, ps, wget, sudo  do?
  chmod -> change permission 
  pwd -> print working directory 
  cd -> chage directory 
  ls -> list all files inside 
  vim -> text editor 
  nano -> text editor 
  mkdir -> make directory 
  mv-> move / rename
  rm -> remove 
  ssh -> remote shell
  ps-> process
  wget -> download files
  sudo -> run as admin
Which of the following console command creates a remote shell session?
  ssh
Which of the following is true when the -la parameter is specified for the ls console command?
  list all files including hidden ones in a long format 
Which of the following is true for the domain name banana.fruit.bozo.click, which is the top level domain, which is a subdomain, which is a root domain?
.click -> root domain.  
Is a web certificate is necessary to use HTTPS.
  yes
Can a DNS A record can point to an IP address or another A record.
  DNS points to IP address not A record 
Port 443, 80, 22 is reserved for which protocol?
  443 -> HTTPS, 80 -> HTTP, 22 -> SSH
What will the following code using Promises output when executed?
  Many possibilities depending on promise behavior. Examples:
1) Promise.resolve('Done').then(console.log) -> 'Done'
2) Promise.reject('Error').catch(console.error) -> 'Error'
3) new Promise(res => setTimeout(() => res('Hi'),1000)).then(console.log) -> 'Hi' after 1s
4) Async function returns value -> printed when awaited or .then
5) Promise chain: Promise.resolve(2).then(x=>x*2).then(x=>x+1).then(console.log) -> 5
6) Reject handled -> shows error via catch.
