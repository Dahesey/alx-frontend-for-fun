
Short Specializations
Average: 65.69%
Flexbox
HTML
CSS
Front-end
 Weight: 1
 Project over - took place from Aug 12, 2024 6:00 AM to Aug 19, 2024 6:00 AM
 Manual QA review was done on Sep 2, 2024 8:15 AM
 An auto review will be launched at the deadline
In a nutshell…

Manual QA review: 0.0/0 mandatory & 0.0/11 optional
Auto QA review: 0.0/0 mandatory & 0.0/161 optional
Altogether:  0.0%
Mandatory: no mandatory tasks
Optional: 0.0%
Overall comment:
Project was failed automatically.



Resources
Read or watch:

A Complete Guide to Flexbox | CSS-Tricks
Flexbox Froggy - A game for learning CSS flexbox
Flexbox Defense
Flexbox Cheatsheet
CSS Flexible Box Layout - CSS: Cascading Style Sheets | MDN
afonsopacifer/awesome-flexbox: A curated list of CSS Flexible Box Layout Module or only Flexbox.
Build with Flexbox
Flexplorer
CSS Flexible Box Layout Module Level 1
FLEX: A simple visual cheatsheet for flexbox
Learning Objectives
At the end of this project, you are expected to be able to explain to anyone, without the help of Google:

What is Flexbox?
How to convert float positioning to a flex display
How to horizontally and vertically align elements using Flexbox
The difference between the main and cross axes
Properties that work on flex elements vs flex container
Shorthands for flex
How to create a new page with flex in mind
Requirements
Allowed editors: vi, vim, emacs
A README.md at the root of the project directory is mandatory
All of your code will be executed on Ubuntu 18.04 using Python 3.7.x
All of your files should end with a new line
Files
Required images for your HTML files
Download the images linked in the CSS Advanced project and place them into an images directory at the root of the project.

HTML starter file


CSS starter file
Click to expand/hide file contents

/* SUMMARY
    1. GLOBAL
    2. LAYOUT
    3. SECTION
    4. CARD
*/

/*** 1. GLOBAL ***/

/* Reset / Normalize
   ============================= */

/*! normalize.css v8.0.1 | MIT License | github.com/necolas/normalize.css */html{line-height:1.15;-webkit-text-size-adjust:100%}body{margin:0}main{display:block}h1{font-size:2em;margin:.67em 0}hr{box-sizing:content-box;height:0;overflow:visible}pre{font-family:monospace,monospace;font-size:1em}a{background-color:transparent}abbr[title]{border-bottom:none;text-decoration:underline;text-decoration:underline dotted}b,strong{font-weight:bolder}code,kbd,samp{font-family:monospace,monospace;font-size:1em}small{font-size:80%}sub,sup{font-size:75%;line-height:0;position:relative;vertical-align:baseline}sub{bottom:-.25em}sup{top:-.5em}img{border-style:none}button,input,optgroup,select,textarea{font-family:inherit;font-size:100%;line-height:1.15;margin:0}button,input{overflow:visible}button,select{text-transform:none}[type=button],[type=reset],[type=submit],button{-webkit-appearance:button}[type=button]::-moz-focus-inner,[type=reset]::-moz-focus-inner,[type=submit]::-moz-focus-inner,button::-moz-focus-inner{border-style:none;padding:0}[type=button]:-moz-focusring,[type=reset]:-moz-focusring,[type=submit]:-moz-focusring,button:-moz-focusring{outline:1px dotted ButtonText}fieldset{padding:.35em .75em .625em}legend{box-sizing:border-box;color:inherit;display:table;max-width:100%;padding:0;white-space:normal}progress{vertical-align:baseline}textarea{overflow:auto}[type=checkbox],[type=radio]{box-sizing:border-box;padding:0}[type=number]::-webkit-inner-spin-button,[type=number]::-webkit-outer-spin-button{height:auto}[type=search]{-webkit-appearance:textfield;outline-offset:-2px}[type=search]::-webkit-search-decoration{-webkit-appearance:none}::-webkit-file-upload-button{-webkit-appearance:button;font:inherit}details{display:block}summary{display:list-item}template{display:none}[hidden]{display:none}

/* Variables
   ============================= */

   :root {
    --color-primary: #D73953;
    --color-black:  #090909;
    --color-white: #ffffff;
    --color-grey: #a0a0a0;
    --color-light-grey: #f3f3f3;
    --color-dark-grey: #353535;
  
    --text-color: var(--color-black);
  
    --font-family-base: 'Open Sans', 'Helvetica Neue', Helvetica, Arial, sans-serif;
    --font-family-title: 'Raleway', 'Helvetica Neue', Helvetica, Arial, sans-serif;
  
    --font-size-small: 1.2rem;
    --font-size-medium: 1.6rem;
    --font-size-large: 1.8rem;
    --font-size-x-large: 2.3rem;
    --font-size-xx-large: 4.8rem;
  
    --font-weight-regular: 400;
    --font-weight-bold: 700;
  
    --line-height-small: 1.2;
    --line-height-base: 1.5;
    --line-height-big: 1.8;
  
    /** SECTION **/
    --section-padding: 5rem 0;
    --section-header-padding: 0 0 3rem;
    --section-header-align: center;
    --section-title-font-size: var(--font-size-xx-large);
    --section-title-font-weight: var(--font-weight-bold);
    --section-title-line-height: var(--line-height-small);
    --section-title-margin: 0;
    --section-title-color: var(--color-black);
    --section-tagline-transform: uppercase;
    --section-tagline-color: var(--color-primary);
    --section-tagline-font-family: var(--font-family-headings);
    --section-tagline-font-weight: var(--font-weight-bold);
    --section-tagline-margin: 0;
    --section-body-padding: 2rem 0 4rem;
    --section-footer-padding: 3rem 0 0;
    --section-footer-align: center;
  
    /** HEADER **/
    --header-padding: 4rem 0 0;
    --header-logo-position: relative;
    --header-logo-link-display: inline-block;
    --header-logo-link-position: absolute;
    --header-logo-link-top: -1rem;
    --header-logo-link-left: 0;
  
    /** FOOTER **/
    --footer-padding: 5rem 0 1rem;
  
    /** NAVBAR **/
    --nav-item-font-family: var(--font-family-headings);
    --nav-item-font-weight: var(--font-weight-bold);
    --nav-item-font-size: var(--font-size-medium);
    --nav-item-letter-spacing: .04rem;
    --nav-item-display: inline-block;
    --nav-item-margin: 0 2rem 0 0;
    --nav-item-link-hover: var(--color-white);
  
    /** BUTTON **/
    --button-display: inline-block;
    --button-padding: 1.5rem 3rem;
    --button-border: var(--color-primary) solid 0.2rem;
    --button-color: var(--color-black);
    --button-text-decoration: none;
    --button-font-size: var(--font-size-large);
    --button-hover-color: var(--color-white);
    --button-hover-text-decoration: none;
    --button-hover-background: var(--color-primary);
  
    /** MOTION **/
    --transition-duration: .3s;
    --transition-cubic-bezier: cubic-bezier(0.17, 0.67, 0, 1.01);
  }
  
  /* Base
      ============================= */
  
  *, *:before, *:after {
    box-sizing: border-box;
  }
  
  html {
  scroll-behavior: smooth;
  font-size: 62.5%;
  }
  
  body {
    color: var(--text-color);
    font-family: var(--font-family-base);
    font-size: var(--font-size-medium);
    font-weight: var(--font-weight-regular);
    line-height: var(--line-height-base);
  }
  
  h1, h2, h3, h4, h5, h6 {
    font-family: var(--font-family-title);
    font-weight: var(--font-weight-bold);
  }
  
  a {
    color: var(--text-color);
    text-decoration: none;
  }
  
  a:visited {
    font-style: italic;
  }
  
  a:hover {
    text-decoration: underline;
  }
  
  a:active {
    background-color: var(--color-light-grey);
  }
  
  .button {
    display: var(--button-display);
    padding: var(--button-padding);
    border: var(--button-border);
    font-size: var(--button-font-size);
    color: var(--button-color);
    text-decoration: var(--button-text-decoration);
  }
  
  .button:hover {
    color: var(--button-hover-color);
    text-decoration: var(--button-hover-text-decoration);
    background: var(--button-hover-background);
    transition-duration: var(--transition-duration);
    transition-property: color, background-color;
  }
  
  /* Helpers
      ============================= */
  
  .visually-hidden:not(:focus):not(:active) {
    position: absolute !important;
    height: 1px;
    width: 1px;
    overflow: hidden;
    clip: rect(1px, 1px, 1px, 1px);
    white-space: nowrap;
  }
  
  /*** 2. LAYOUT ***/
  
  /* Layout
      ============================= */
  
  .container {
    width: 960px;
    margin-left: auto;
    margin-right: auto;
  }
  
  /* Grid
      ============================= */
  
  ul.row {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  
  .row::after {
    content: '';
    display: table;
    clear: both;
  }
  
  [class*='col-'] {
    float: left;
    padding: 0.5rem;
  }
  
  .col-1-3 {
    width: 33.33%;
  }
  
  .col-1-2 {
    width: 50%;
  }
  
  /* Navbar
      ============================= */
  
  .navbar-menu {
    float: right;
  }
  
  .nav {
    margin: 0;
    padding: 0;
    list-style: none;
    text-align: center;
  }
  
  .nav .nav-item {
    font-family: var(--nav-item-font-family);
    font-weight: var(--nav-item-font-weight);
    font-size: var(--nav-item-font-size);
    letter-spacing: var(--nav-item-letter-spacing);
    display: var(--nav-item-display);
    margin: var(--nav-item-margin);
  }
  
  .nav .nav-link {
    display: block;
    padding: 0.5rem 0;
    position: relative;
  }
  
  .nav .nav-link:hover {
    color: var(--nav-item-link-hover);
    text-decoration: none;
  }
  
  .nav .nav-link::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    background-color: var(--color-white);
    width: 0;
    height: 0.2rem;
    transition: var(--transition-duration) var(--transition-cubic-bezier);
  }
  
  .nav .nav-item:hover .nav-link::before {
    background-color: var(--color-primary);
    width: 100%;
  }
  
  /* Header
      ============================= */
  
  .header {
    padding: var(--header-padding);
         position: relative;
         z-index: 3;
         background: transparent;
  }
  
  .header-logo {
    position: var(--header-logo-position);
  }
  
  .header-logo a {
    display: var(--header-logo-link-display);
    position: var(--header-logo-link-position);
    top: var(--header-logo-link-top);
    left: var(--header-logo-link-left);
  }
  
  /* Footer
      ============================= */
  
  .footer {
    --nav-item-font-weight: normal;
    --nav-item-font-size: var(--font-size-small);
    padding: var(--footer-padding);
  }
  
  .footer-copyright {
    margin: 0;
    font-size: var(--font-size-small);
    color: var(--text-color);
  }
  
  .footer ul {
    text-align: right;
  }
  
  .footer-address {
    color: var(--text-color);
  }
  
  .social-link {
    display: block;
  }
  
  .social-link > svg {
    fill: var(--text-color);
  }
  
  /*** 3. SECTION ***/
  
  /* Section (all styles)
      ============================= */
  
  .section {
    padding: var(--section-padding);
  }
  
  .section-header {
    text-align: var(--section-header-align);
    padding: var(--section-header-padding);
  }
  
  .section-title {
    font-size: var(--section-title-font-size);
    font-weight: var(--section-title-font-weight);
    line-height: var(--section-title-line-height);
    margin: var(--section-title-margin);
    color: var(--section-title-color);
  }
  
  .section-tagline {
    color: var(--section-tagline-color);
    font-family: var(--section-tagline-font-family);
    text-transform: var(--section-tagline-transform);
    font-weight: var(--section-tagline-font-weight);
    margin: var(--section-tagline-margin);
  }
  
  .section-body {
    padding: var(--section-body-padding);
  }
  
  .section-footer {
    padding: var(--section-footer-padding);
    text-align: var(--section-footer-align);
  }
  
  /* Section theming
      ============================= */
  
  [data-section-theme="dark"] {
    --button-color: var(--color-white);
    --text-color: var(--color-white);
    --section-title-color: var(--color-white);
    background-color: #010101;
  }
  
  /* Section HERO
      ============================= */
  
  .section-hero {
    background-position: 75% 0;
    background-repeat: no-repeat;
    background-size: 90rem auto;
    background-color: #010101;
  }
  
  .section-hero .section-title {
    margin-bottom: 5rem;
  }
  
  .section-hero .section-inner {
    padding: 10rem 40rem 2rem 0;
  }
  
  /*** 4. CARD ***/
  
  /* Card (all styles)
      ============================= */
  
  .card-category {
    color: var(--color-primary);
  }
  
  /* Card WORK
      ============================= */
  
  .card-work .card-outer {
    position: relative;
    overflow: hidden;
  }
  
  .card-work:hover .card-outer {
    transform: scale(0.95);
  }
  
  .card-work .card-image img {
    height: 30rem;
    width: 100%;
    object-fit: cover;
    vertical-align: bottom;
  }
  
  .card-work:hover .card-image {
    transform: scale(1.2);
    transition: var(--transition-duration) var(--transition-cubic-bezier);
  }
  
  .card-work .card-inner {
    position: absolute;
    top: -0.1rem;
    left: -0.1rem;
    right: -0.1rem;
    bottom: -0.1rem;
    z-index: 1;
    transition: var(--transition-duration) var(--transition-cubic-bezier);
  }
  
  .card-work:hover .card-inner {
    background-color: rgba(0, 0, 0, 0.7);
  }
  
  .card-work .card-title {
    text-align: center;
    margin: 0;
    opacity: 0;
    height: 100%;
    position: relative;
  }
  
  .card-work .card-title a {
    display: block;
    text-decoration: none;
    padding-top: 45%;
  }
  
  .card-work .card-title a::after {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    content: '';
  }
  
  .card-work:hover .card-title {
    opacity: 1;
  }
  
  /* Card SERVICES
      ============================= */
  
  .card-services .card-title {
    margin: 0;
  }
  
  .card-services a {
    display: block;
    padding: 2rem;
    background-color: var(--color-light-grey);
  }
  
  .card-services a:hover {
    color: var(--color-white);
    background: var(--color-primary);
    text-decoration: none;
    transition-duration: 0.3s;
    transition-property: color, background-color;
  }
  
  /* Card TESTIMONIAL
      ============================= */
  
  .card-testimonial {
    text-align: center;
  }
  
  .card-testimonial .card-avatar {
    border-radius: 50%;
    width: 10rem;
    height: 10rem;
  }
  
  .card-testimonial .card-quote cite {
    display: block;
    padding-top: 1rem;
    color: var(--color-primary);
  }
  
  .card-testimonial .card-quote {
    position: relative;
  }
  
  .card-testimonial .card-quote::before {
    content: '\201C';
    position: absolute;
    top: -4.5rem;
    left: -1rem;
    color: #efeded;
    font-size: 10rem;
    z-index: -1;
  }
    
Files for tasks 10 and onward
article.html



Quiz questions
Great! You've completed the quiz successfully! Keep going! (Show quiz)
Tasks
0. Add display flex
#advanced
Score: 0.0% (Checks completed: 0.0%)
Use the starter HTML and CSS files from this task to task 10. Copy the contents of the starter files into the files that you need to produce and make the necessary changes according to the task description.

When using display: flex; on a container, all direct children become flex-items (and no more inline or block elements).

With display flex, margins are not collapsing as they would with block items. Also remember that flexbox is 1-dimensional system (vs CSS Grid which is a 2 dimensional system)

In the /* Grid section within your CSS

Add a selector for the row class
Property: display, Value: flex
=> Now, all children from the row class are flex items

Entirely remove the row::after declaration
Remove the float: left inside [class*='col-']
=> All elements should appear same than before using the float

Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 0-index.html, 0-styles.css
  
1. Add new classes on sections
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task as the base for this task:

In the outermost section tag for services

Add the class section-services
In the outermost section tag for works

Add the class section-works
In the outermost section tag for about

Add the class section-about-us
In the outermost section tag for latest_news

Add the class section-latest-news
In the outermost section tag for testimonial

Add the class section-testimonial
In the outermost section tag for contact

Add the class section-contact
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 1-index.html, 1-styles.css
  
2. Reverse order Latest news cards
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task for this task:

The flex-direction property says how flex items are placed on the main axis and their direction (normal or reversed).

flex-direction is sometimes used when doing responsive design. Some elements may appear better when they are in column mode on mobile and row when on desktop.

row-reverse and column-reverse should be used in specific situation. The visual order of elements should be the same visually and in the HTML code. Refer to flex-direction - CSS: Cascading Style Sheets | MDN for more information

In your CSS file:

Before /*** 4. CARD ***/, add a new comment: /* Section Latest news ============================= */

Under that comment section, target the row class inside section-latest-news class

Property: flex-direction, Value: row-reverse
The Latest news should appear in a reverse order.

Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 2-index.html, 2-styles.css
  
3. Simplify services list
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task for this task:

flex-wrap is a property that can force the flex items to be in one or multiple lines. Learn more about it here.

In the Services section of 3-index.html, remove the second ul and put the 3 lielements under the first ul

Now, in your CSS file, before /*** 4. CARD ***/, add a new comment: /* Section SERVICES ============================= */

Under that comment section, add a new selector targeting the row class inside the section-services class

Property: flex-wrap, Value: wrap
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 3-index.html, 3-styles.css
  
4. Playing around with the spacing between flex service items
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task for this task:

In 4-styles.css file, within the Grid section

In .col-1-3 selector

Replace the current width with calc((100% / 3) - 2rem)
In .col-1-2 selector

Replace the current width with calc((100% / 2) - 2rem)
In [class*='col-']

Remove the padding declaration
Set Property: margin to 1rem
In ul.row declaration

Replace the current margin with -1rem
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 4-index.html, 4-styles.css
  
5. Flexify the header
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task for this task:

In your 5-index.html file, inside the Header section

Wrap the div with class header-logo and the nav with class navbar-menu with a div that has header-container as a class
In your 5-styles.css file,

Inside the /* Header section
Add a selector for the header-container class
Property: display, Value: flex
Property: justify-content, Value: space-between
Remove header-logo and header-logo a rules
Remove the navbar-menu rule

In the variables section

Remove
header-logo-position
header-logo-link-display
header-logo-link-position
header-logo-link-top
header-logo-link-left
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 5-index.html, 5-styles.css
  
6. Flexify the navbar
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task for this task:

in 6-styles.css, inside the /* Navbarsection

In the nav class selector
Property: display, Value: flex
Inside the .nav .nav-item selector, remove the display declaration
Target .nav-item + .nav-item inside nav class
Move the margin declaration from .nav .nav-item inside the new selector.
In the variables section
Change the value of the variable nav-item-margin to be 0 0 0 2rem
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 6-index.html, 6-styles.css
  
7. Align center logo and navbar
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task for this task:

In 7-styles.css, inside the /* Header section, in the header-container class selector, set the property align-items to center

Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 7-index.html, 7-styles.css
  
8. Simplify the hero banner
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task for this task:

In 8-styles.cssInside the /* Section HERO section

In the selector targeting section-inner class in section-hero class, remove the padding and replace with
Property: display, Value: flex
Property: flex-direction, Value: column
Property: align-items, Value: flex-start
Property: justify-content, Value: center
Property: min-height, Value: 50vh
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 8-index.html, 8-styles.css
  
9. Better alignment about us
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the files from the previous task for this task:

In 9-styles.css, after the /* Section SERVICES section, create a /* Section ABOUT US section. Inside that new section, target all classes that begin with col- inside section-about-us class

Property: align-self, Value: center
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 9-index.html, 9-styles.css
  
10. Creating an article by fixing issues and updating hero styles
#advanced
Score: 0.0% (Checks completed: 0.0%)
Using the CSS file from the previous task and article.html (provided above in the project description) for this task:

In 10-styles.css, inside the /* Section HERO section

After the .section-hero, add a new hero-homepage class selector (you will need to add that class later in your html files)

Move all declarations inside section-hero inside the new hero-homepage class selector

Inside section-hero class selector

Property: position, Value: relative
Property: margin-top, Value: -8.5rem
Below, target .section-body inside section-hero class

Property: padding, Value: 10rem 4rem
Below, target .section-category inside section-hero class

Property: color, Value: point to the variable color-white
Property: text-transform, Value: uppercase
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 10-article.html, 10-styles.css
  
11. Update the new hero banner
#advanced
Score: 0.0% (Checks completed: 0.0%)
In 11-article.html in the Hero section

Add the hero-article class on the <header> which is in <main>
Add this background-image (pic-article-02.jpg) as an inline style still on the <header>
Inside the section with section-inner class
Add a span with the class section-category and the text Digital Life
Below, add an h1 with the class section-title and the following text Ut alios omittam, hunc appello, quem ille unum secutus est
At the end of 11-styles.css, create a new comment section

/*** ARTICLE PAGE ***/
/* Section HERO (article)
    ============================= */
Target the hero-article class

Property: background-size, Value: 150rem 100rem
Property: background-position, Value: 50% 0
Target the before pseudo element of hero-article class

Property: content, Value: empty
Property: background, Value: rgba(0, 0, 0, 0.8)
Property: position, Value: absolute
Property: top, Value: 0
Property: right, Value: 0
Property: left, Value: 0
Property: bottom, Value: 0
Property: z-index, Value: 0
Target the section-inner class inside the hero-article class

Property: text-align, Value: center
Property: align-items, Value: center
Property: min-height, Value: 40vh
Target the section-body class inside the hero-article class

Property: position, Value: relative
Property: padding, Value: 7rem 0 0
Property: z-index, Value: 2
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 11-article.html, 11-styles.css
  
12. The structure of the main article
#advanced
Score: 0.0% (Checks completed: 0.0%)
In your 12-article.html file, in the Hero section

After the header, create a <div>and set its class to main-article (this div will be siblings with the Hero section header)
Create a div inside the main-article div and set the class to container
Create a div with the class post inside the container div
Inside the post div:
Create a new article with the class post-content
Below the post-content article, add the comment <!-- Aside section -->
Sibling to the post-content article and after the comment, create an aside with the class post-aside
Inside post-aside aside, create 2 divs:
The first with the class post-meta
The second with the class post-share
In your 12-styles.css:

Target the main-article class

Property: padding, Value: 5rem 0
Add the below separator comment

/* Post
    ============================= */
Target the post class
Property: display, Value: flex
Target the post-content class
Property: width, Value: 100%
Target the post-aside class
Property: order, Value: -1
Property: min-width, Value: 20%
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 12-article.html, 12-styles.css
  
13. The meta list inside the aside section
#advanced
Score: 0.0% (Checks completed: 0.0%)
In your 13-article.html

Create an unordered list inside the post-meta div with the classes post-meta-list and row
Create a first <li> with the class post-meta-author
Create the HTML tag that show a stronger importance
Text: Written by:
Create a link
Href: #
Rel: author
Text: William Attaway
Create a second <li> with the class post-meta-date
Create the HTML tag that show a stronger importance
Text: Posted on:
Use the HTML tag for date / time - Datetime: 2019-10 - Text: October 2019
Create a third <li> with the class post-meta-tag
Create the HTML tag that show a stronger importance
Text: Tags:
Create an unordered list with the class tag-list
First <li> contain a link
Href: #
Rel: tag
Text: Web Design
Second <li> contain a link
Href: #
Rel: tag
Text: UX
Update 13-styles.css with this information

Add a separator comment

/* Post Meta
    ============================= */
Target the post-meta-list class

Property: flex-direction, Value: column
Target the strong tag inside post-meta-list class

Property: color, Value: point to the variable color-primary
Property: font-size, Value: point to the variable font-size-small
Property: text-transform, Value: uppercase
Property: display, Value: block
Target all classes that start with post-meta- inside post-meta-list class

Property: margin-bottom, Value: 1rem
Property: padding-bottom, Value: 1rem
Property: border-bottom, Values: 0.2rem solid and point to the color-light-grey variable
Target the last child of all classes that start with post-meta inside post-meta-list class

Property: border, Value: none
Property: margin-bottom, Value: 3rem
Add a separator comment

/* Tag list
    ============================= */
Target the tag-list class

Property: padding, Value: 0
Property: list-style, Value: none
Target all li inside the tag-list class

Property: display, Value: inline
Target the after pseudo element on the li inside tag-list class

Property: content, Value: ", " (space after the comma)
Target the after pseudo element of the last-child on the li inside tag-list class

Property: content, Value: empty
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 13-article.html, 13-styles.css
  
14. Add the share social icons
#advanced
Score: 0.0% (Checks completed: 0.0%)
In your 14-article.html, inside the post-share div

Copy paste the social nav list (already existing in the footer) inside
Remove the li with Instagram (3rd one)
Replace the href in the links with a default value ( #)
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 14-article.html, 14-styles.css
  
15. Finalizing the cherry on the cake that is the article
#advanced
Score: 0.0% (Checks completed: 0.0%)
In your 100-article.html

Inside the post-content article

Add a paragraph
Text: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Tum mihi Piso: Quid ergo? Tum ille: Ain tandem? Non autem hoc: igitur ne illud quidem. Sed quod proximum fuit non vidit. Nos commodius agimus. An nisi populari fama?
Add another paragraph
Text: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed haec omittamus; Hoc Hieronymus summum bonum esse dixit. Duo Reges: constructio interrete.
You should wrap the following text with a <b> tag: Hoc Hieronymus summum bonum esse dixit.
Add a heading level 2
Text: Prioris generis est docilitas, memoria
Add an ordered list
First li
Text: Nec enim, dum metuit, iustus est, et certe, si metuere destiterit, non erit;
Second li
Text: Quid enim de amicitia statueris utilitatis causa expetenda vides.
Add another paragraph
Text: Morbi pharetra congue ante ac tincidunt. Donec euismod eu mauris nec laoreet. Praesent id sodales ipsum. Aliquam erat volutpat. Ut porta sem eget libero faucibus, eget convallis nisi finibus. Interdum et malesuada fames ac ante ipsum primis in faucibus. Vestibulum accumsan euismod nunc quis viverra.
Create a <figure> HTML tag
Download the image and create an img tag to call it
Alt: Glasses, baby converse shoes, black bag, wipes on a dresser with an open drawer
Width: 620
Height: 350
Add a figcaption with the class img-caption
Text: Pugnant Stoici cum Peripateticis. Prioris generis est docilitas
Add a new paragraph
Text: Quare conare, quaeso. Dici enim nihil potest verius. Primum divisit ineleganter; Suam denique cuique naturam esse ad vivendum ducem.
Add a blockquote
Cite: https://www.holbertonschool.com/
Text: Ego autem tibi, Piso, assentior usu hoc venire, ut acrius aliquanto et attentius de claris viris locorum admonitu cogitemus.
Add a new paragraph
Text: Omnia contraria, quos etiam insanos esse vultis. Tibi hoc incredibile, quod beatissimum.
Add a heading level 2
Text: Piso igitur hoc modo, vir optimus tuique, ut scis, amantissimus.
Add a new paragraph
Text: Apparet statim, quae sint officia, quae actiones. Quae in controversiam veniunt, de iis, si placet, disseramus.
Create a link that wraps Apparet statim, quae sint officia, quae actiones.
Href: https://www.holbertonschool.com/
Target: _blank
Add the rel needed for target blank
Add an unordered list
First li: Tubulum fuisse, qua illum, cuius is condemnatus est rogatione, P.
Second li: Quis est autem dignus nomine hominis, qui unum diem totum velit esse in genere isto voluptatis?
Third li: Sed in rebus apertissimis nimium longi sumus.
Add one last paragraph:
Text: Hoc etsi multimodis reprehendi potest, tamen accipio, quod dant. Atqui, inquam, Cato, si istud optinueris, traducas me ad te totum licebit. Nemo nostrum istius generis asotos iucunde putat vivere. Res enim se praeclare habebat, et quidem in utraque parte. Qui autem esse poteris, nisi te amor ipse ceperit? Ita fit cum gravior, tum etiam splendidior oratio. De vacuitate doloris eadem sententia erit. Sin tantum modo ad indicia veteris memoriae cognoscenda, curiosorum.
Updating the CSS with more styling

In the 100-styles.css

Target all img inside the post class
Property: width, Value: 100%
Property: height, Value: auto
Target the first-child of paragraphs inside post-content class

Property: font-size, Value: point to the variable font-size-x-large
Target img-caption class inside post-content class

Property: margin, Value: 1rem 0
Property: padding, Value: 0 .5rem
Property: font-size, Value: point to the variable font-size-small
Property: color, Value: point to the variable color-grey (if the variable doesn’t exist, create it with the value of #a0a0a0)
Property: text-align, Value: center
Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 100-article.html, 100-styles.css
  
16. Timemachine boxes!
#advanced
Score: 0.0% (Checks completed: 0.0%)
Write a CSS file that display a set of boxes in the same layout as the example screenshot below.

Choose a custom color for each box
You must use flex
You are not allowed to use float
You are not allowed to use text-align
You are not allowed to use margin or padding
You are not allowed to change the HTML file
Use this 101-index.html file:

<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>101-index</title>
        <link href="101-style.css" media="all" rel="stylesheet" type="text/css">
    </head>
    <body>
        <div class="container">
            <div class="box box1">box 1</div>
            <div class="box box2">box 2</div>
            <div class="box box3">box 3</div>
            <div class="box box4">box 4</div>
            <div class="box box5">box 5</div>
        </div>
    </body>
</html>


Repo:

GitHub repository: alx-frontend-for-fun
Directory: flexbox
File: 101-style.css
Copyright © 2024 ALX, All rights reserved.
