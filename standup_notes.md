# Standup Notes

### Daily Scrum
##### Thursday, Jan 21, 2021
- What did you do yesterday?
   - N/A
- What will you do today?
   - transition from internal to external CSS (lab2 had a lot)
   - use Google Fonts instead of importing via font-family
   - if time allows, set up an external CSS that will do color formatting for diff coding languages
- Where are you blocked?
  - Wanted to set up custom color coding for the code section. E.g. when the word 'main' shows up color that, if 'return' color that, etc. Basic CSS will not look at text content. Checked Javascript, that won't work either. Kinda disappointed. Might have to brute force.
- Comfort Level — How close are we to hitting our sprint goals?
  - Only done 25% of features need. But it's aesthetic so far.

---

##### Friday, Jan 22, 2021
- What did you do yesterday?
   - external CSS doc
   - learned how to set up classes tied to css styling
   - finished data structures section and added more content
   - most color, padding, margins, border, etc. is done
- What will you do today?
   - all the selectors, display, position, flexbox, and grid
   - have a cool design idea for the earth's layers that could use position
   - try to do all this work using the Pomodoro Timer too
- Where are you blocked?
- Comfort Level — How close are we to hitting our sprint goals?

---

### Work Log

##### Selectors
- [x] Class Selector (.class)
   ```css
      .item1 {
         grid-row-start: 1;
         grid-row-end: 2;
         grid-column-start: 1;
         grid-column-end: 2;
      }
   ```
- [x] ID Selector (#id)
  ```html
      <a class="table of contents" href="#DataStructures">Data Structures </a> |
  ```
- [x] Universal Selector (*)
   ```css
      * {
         text-align: left;
      }
   ```
- [ ] Element Selector (element)
- [x] Attribute Selector (e.g. [attribute=foo])
   ```css
      body[class$="run"] {
         font-family: menlo;
         color: rgb(58, 58, 58);
         background-color: #f1f1f1;
         padding: 2px;
      }
   ```
- [x] Pseudo-class Selectors (e.g. p::hover)
  ```css
      a:hover[class~="contents"] {
         color: white;
         font-weight: bold;
      }
  ```
- [ ] Grouping / Combinators
- [x] Selector List (element, element)
  ```css
   h5, h6 {
      font-family: 'Overpass';
      color: rgb(211, 211, 211);
      font-size: 15px;
      margin: 1px 1px 10px 1px; /* top right bottom left */
   }
  ```
- [x] Descendant Combinator (element element)
  ```css
      ol li {
         font-weight: normal;
         color: rgb(193, 193, 193);
      }
   ```
- [x] Child Combinator (element > element)
  ```css
   details > code {
      font-family: menlo;
      color: rgb(203, 203, 203);
      background-color: hsla(0,100%,0%,0.3);    /* sets opacity of black color */
      padding-top: 3px;
      padding-right: 5px;
      padding-bottom: 3px;
      padding-left: 5px;
      margin: 3px 1px 1px 3px;    /* top right bottom left */
   }
   ```
- [x] General sibling combinator (element ~ element)
  ```css
      code ~ code[class="src"] {
         color: aquamarine;
      }
   ```
- [x] Adjacent sibling combinator (element + element)
  ```css
   /* Style for h5 text DIRECTLY AFTER h4 */
   h4 + h5 {
      color:rgb(225, 225, 225);
      background-color: hsla(0,100%,100%,0.02);
   }
  ```
- [x] Combining Two Selectors (element.class)
  ```css
      h2.section_title {
         color: #2558b1;
         font-size: 35px;
         font-family: 'Overpass', sans-serif;
         font-weight: bold;
         text-decoration: underline;
         text-decoration-color: rgb(28, 33, 52);
      }
  ```

##### CSS Topics       
- [x] Comments
   ```css
      /* literally all over style.css */
   ```
- Colors
   - [x] rgb(r, g, b), rgba(r, g, b, a)
   ```css
      h3[class="highlight"] {
         color: black;
         background-color: rgb(48, 201, 132);
      }
   ```
   - [x] #FFF, #FFFFFF
   ```css
      h4 {
         color: #30C886;
         font-size: 12px;
      }
   ```
   - [x] hsl(h, s, l),  hsla(h, s, l, a)
   ```css
      section[class="dark"] {
         background-color: hsla(0,0,0,0.5);    /* sets opacity of black color to 50% */
         padding: 10px;
         font-size: 14px;
      }
   ```
   - [x] Color name (i.e ‘green’)
   ```css
      h3[class="highlight"] {
         color: black;
         background-color: rgb(48, 201, 132);
      }
   ```
- Backgrounds
   - [x] background-color
- Borders
   - [x] border-style
   - [x] border-color
   - [x] border-width
   - [x] border-radius
  ```css
   /* table header */
   th {
      border-style: solid;
      border-color: #0B0E11;
      border-width: 3px;
      border-radius: 2px;
      text-align: center;
      padding-left: 15px;
      padding-right: 15px;
   }
  ```
- Unit
   - [ ] 3 relative
   - [ ] 3 absolute
   - [ ] Box Model CSS Box Model
- Margins
   - [x] Long (margin-top, margin-bottom, margin-left, margin-right)
   ```css
      h3[class="highlight"] {
         font-family: 'Overpass';
         font-weight: semi-bold;
         color:rgb(216, 216, 216);
         background-color: #063731;
         padding: 5px 5px 3px 10px; /* top right bottom left */
         margin-left: 5px;          /* space btw edge of page and section */
         margin-right: 5px;
         margin-top: 10px;
         margin-bottom: 10px;
      }
   ```
   - [x] Short (margin: top right bottom left)
   ```css
      code[class$="run"] {
         font-family: menlo;
         color: rgb(203, 203, 203);
         background-color: hsla(0,100%,0%,0.3);    /* sets opacity of black color */
         padding-top: 3px;
         padding-right: 5px;
         padding-bottom: 3px;
         padding-left: 5px;
         margin: 3px 1px 1px 3px;    /* top right bottom left */
      }
   ```
   - [x] auto
   ```css
      code {
         font-family: menlo;
         color: rgb(203, 203, 203);
         background-color: hsla(0,100%,0%,0.3);    /* sets opacity of black color */
         padding: 5px;
         margin: auto;
         font-size: 100%;
      }
   ```
- Padding
   - [x] Long (padding-top, padding-bottom, padding-left, padding-right)
   - [x] Shorthand (padding: top right bottom left)
   - [x] Height / Width
   ```css
      table {
         font-family: ibm plex sans;
         border-collapse: collapse;
         position: static;
         width: 100px;
         height: 20px;
      }
   ```
   - [x] Set the height and width for an element
   ```html
      <svg width="1500" height="5">
      <rect width="1500" height="5" style="fill:#393939"/>
      </svg>
   ```
- Text
   - [x] color
   - [x] text-decoration -- Table of Contents (in nav)
   - [x] text-align
- [x] Fonts: Include and use a **3rd party** font (https://fonts.google.com/ (Links to an external site.)). You can load the font in either your HTML or your CSS.
  ```html 
      <link rel="preconnect" href="https://fonts.gstatic.com">
      <link href="https://fonts.googleapis.com/css2?family=Overpass:ital,wght@0,300;0,600;0,700;0,800;1,800;1,900&display=swap" rel="stylesheet">
  ```
- Display: Experiment with these types and include at least **two** of them in your page.
   - [x] none
   ```css
      h1 {
         color: #dac529;
         font-size: 10px;
         display: none;
      }
   ```
   - [ ] block
   - [ ] inline-block
   - [x] inline
   ```css
      nav {
         text-align: left;
         font-size: 14px;
         color: white;
         .
         .
         .
         display: inline;
      }
   ```
- Max-width / Min-width
   - [x] Width has to be variable (like a percentage)
   ```html
       <footer>
         <img src="footer.jpeg" alt="Footer Image" style="width: 100%">
      </footer>
   ```
- Position: Experiment with these attributes and include at least **two** of them in your page.
   - [x] static
  ```css
   /* style of table */
   table {
      font-family: ibm plex sans;
      border-collapse: collapse;
      position: static;
      width: 100px;
      height: 20px;
   }
  ```
   - [x] relative
   ```css
      header {
         position: relative;
         bottom: 30px;
      }
   ```
   - [x] fixed -- Table of Contents
   - [x] absolute
   ```css
      header {
         position: absolute;
         top: -10px;
      }
   ```
   - [x] sticky 
   ```css
      footer {
         position: -webkit-sticky;
         position: sticky;   /* once scrolled over, will stay at top of screen */
      }

   ```
   - [x] :hover (Pseudo-class) 
  ```css
   /* Hover over Table of Contents */
   a:hover[class~="contents"] {
      color: white;
      font-weight: bold;
   }
   ```
   - [x] :active (Pseudo-class)
   ```css
   /* Clicked element of Table of Contents */
   a:active[class~="contents"] {
      color: #30C886;
      font-weight: bold;
   }
   ```
- Flexbox (Links to an external site.)
   - [ ] Must have more than two children within the element that is using flexbox. Must use minimum **three** of the flexbox related attributes.
- Grid (Links to an external site.)
   - [ ] Must have more than two children within the element that is using grid. Must use minimum **three** of the flexbox related attributes.
- [ ] Media Query. At least **one query** based on the screen width
