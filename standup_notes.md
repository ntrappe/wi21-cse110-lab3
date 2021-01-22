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
- Comfort Level — How close are we to hitting our sprint goals?

---

### Work Log

##### Selectors
- [ ] Class Selector (.class)
- [ ] ID Selector (#id)
- [ ] Universal Selector (*)
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
- [ ] Pseudo-class Selectors (e.g. p::hover)
- [ ] Grouping / Combinators
- [ ] Selector List (element, element)
- [ ] Descendant Combinator (element element)
- [ ] Child Combinator (element > element)
- [ ] General sibling combinator (element ~ element)
- [ ] Adjacent sibling combinator (element + element)
- [ ] Combining Two Selectors (element.class)

##### CSS Topics       
- [ ] Comments
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
   - [ ] border-style
   - [ ] border-color
   - [ ] border-width
   - [ ] border-radius
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
   - [ ] Short (margin: top right bottom left)
   - [ ] auto
- Padding
   - [x] Long (padding-top, padding-bottom, padding-left, padding-right)
   - [x] Shorthand (padding: top right bottom left)
   - [ ] Height / Width
   - [ ] Set the height and width for an element
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
   - [ ] none
   - [ ] block
   - [ ] inline-block
   - [ ] inline
- Max-width / Min-width
   - [ ] Width has to be variable (like a percentage)
- Position: Experiment with these attributes and include at least **two** of them in your page.
   - [ ] static
   - [ ] relative
   - [x] fixed -- Table of Contents
   - [ ] absolute
   - [ ] sticky 
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
