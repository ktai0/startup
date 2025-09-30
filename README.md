# Operation Ryugaku Ninja 

[My Notes](notes.md)
Recently, Japanese companies have made tons of money helping Japanese students come overseas to study English. The services that they provide are nothing special !! Helping them find houses, editing their essays, etc…. However, students can do this themselves with facebook marketplace and chatGPT. One particular company has been offering these innately free and easy actions at an absurd price, creating a financial barrier for students to access this educational opportunity. I am going to do something about this !!!


> [!NOTE]
>  This is a template for your startup application. You must modify this `README.md` file for each phase of your development. You only need to fill in the section for each deliverable when that deliverable is submitted in Canvas. Without completing the section for a deliverable, the TA will not know what to look for when grading your submission. Feel free to add additional information to each deliverable description, but make sure you at least have the list of rubric items and a description of what you did for each item.

> [!NOTE]
>  If you are not familiar with Markdown then you should review the [documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) before continuing.

## 🚀 Specification Deliverable

> [!NOTE]
>  Fill in this sections as the submission artifact for this deliverable. You can refer to this [example](https://github.com/webprogramming260/startup-example/blob/main/README.md) for inspiration.

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [x] Proper use of Markdown
- [x] A concise and compelling elevator pitch
- [x] Description of key features
- [x] Description of how you will use each technology
- [x] One or more rough sketches of your application. Images must be embedded in this file using Markdown image references.

### Elevator pitch

Recently, there has been a increase in Japanese "study abroad assistant" companies offering to help place students in different parts of the world. One comapny that targets students coming to Utah is charging 13,500 USD per person (with normal exhange rates, it would be more like 20,000 USD)! They don't do anything special. Help them find houses and edit their essays for them, maybe go for a few company tours. However, the company is becoming increasingly selfish with their pricing and services. I want to provide all of the information they provide for free !! From how to find houses to what prompts to put into AI editing tools for editing application essays. Let's help make education more accessible to those who want it.  

### Design

![Design image](Design.png)

The main idea is to have a webiste that looks similar to a FAQ page. There will be a list of frequently asked questions, but through inputting a keyword, they can get to their desired information faster than scrolling. Another big part of this website is the ability to follow along with images or videos. For example, a series of images explaining how to find houses on facebook marketplace. 

### Key features

- A toggle feature to expand different sections of information 
- A text input feature to help search their desired information 
- images of different types of apartments 
- login/logout/create an account if they desire more personalised help with essay and other functions

### Technologies

I am going to use the required technologies in the following ways.

- **HTML** - 2 HTML pages, one for information, the second one to create an account
- **CSS** - An easy to follow flow for the user, paying special attention to creating a phone-friendly layout
- **React** - Using react mainly to compartamentalise information for the toggle feature. Also provides login function and structure for the keyword serarch. 
- **Service** - login/logout and retreiving images for overall aesthetic use
- **DB/Login** - storing user information, register and login users. Store clicks -> lsit questions in most frequently clicked on question ?
- **WebSocket** - Display number of users registered and receiving assistance. 

## 🚀 AWS deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [x] **Server deployed and accessible with custom domain name** - [My server link](https://ryugakuninja.click/).

## 🚀 HTML deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [x] **HTML pages** - Completed linking and basic structure of all needed HTML pages
- [x] **Proper HTML element usage** - Used HTML tags including BODY, NAV, MAIN, HEADER, FOOTER on all pages
- [x] **Links** - Succesfully linked all needed pages, and even linked a logo with the homepage
- [x] **Text** - Finished the instructions and texts for the homepage and housing page
- [x] **3rd party API placeholder** - Goal: embedding google maps, but made a div for it. 
- [x] **Images** - Implemented a logo at the header of each website
- [ ] **Login placeholder** - I did not complete this part of the deliverable.
- [ ] **DB data placeholder** - I did not complete this part of the deliverable.
- [ ] **WebSocket placeholder** - I did not complete this part of the deliverable.

## 🚀 CSS deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Header, footer, and main content body** - I did not complete this part of the deliverable.
- [ ] **Navigation elements** - I did not complete this part of the deliverable.
- [ ] **Responsive to window resizing** - I did not complete this part of the deliverable.
- [ ] **Application elements** - I did not complete this part of the deliverable.
- [ ] **Application text content** - I did not complete this part of the deliverable.
- [ ] **Application images** - I did not complete this part of the deliverable.

## 🚀 React part 1: Routing deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Bundled using Vite** - I did not complete this part of the deliverable.
- [ ] **Components** - I did not complete this part of the deliverable.
- [ ] **Router** - I did not complete this part of the deliverable.

## 🚀 React part 2: Reactivity deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **All functionality implemented or mocked out** - I did not complete this part of the deliverable.
- [ ] **Hooks** - I did not complete this part of the deliverable.

## 🚀 Service deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Node.js/Express HTTP service** - I did not complete this part of the deliverable.
- [ ] **Static middleware for frontend** - I did not complete this part of the deliverable.
- [ ] **Calls to third party endpoints** - I did not complete this part of the deliverable.
- [ ] **Backend service endpoints** - I did not complete this part of the deliverable.
- [ ] **Frontend calls service endpoints** - I did not complete this part of the deliverable.
- [ ] **Supports registration, login, logout, and restricted endpoint** - I did not complete this part of the deliverable.


## 🚀 DB deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Stores data in MongoDB** - I did not complete this part of the deliverable.
- [ ] **Stores credentials in MongoDB** - I did not complete this part of the deliverable.

## 🚀 WebSocket deliverable

For this deliverable I did the following. I checked the box `[x]` and added a description for things I completed.

- [ ] **Backend listens for WebSocket connection** - I did not complete this part of the deliverable.
- [ ] **Frontend makes WebSocket connection** - I did not complete this part of the deliverable.
- [ ] **Data sent over WebSocket connection** - I did not complete this part of the deliverable.
- [ ] **WebSocket data displayed** - I did not complete this part of the deliverable.
- [ ] **Application is fully functional** - I did not complete this part of the deliverable.
