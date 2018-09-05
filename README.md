# All changes to bootstrap css
Make changes to json file and recompile here (seems easier than huntingn and pecking on this screen?):
or modify here. Whichever is easiest: https://getbootstrap.com/docs/3.3/customize/?id=00380e1d5d6465adebd7ddb902e7989b

## following needs to be changed if you use the above link!
* @link-color color to #3367d6
* @headings-small-color to "#999"
* @blockquote-small-color to "#999"
* "Form states and alerts"
  * @state-success-text is now @text-color
  * all other @state-xxx-text is now white [old: @text-color (changed from @brand-xxxx)]
  * @state-xxx-bg (changed from white to @brand-xxx)
* increase radius 
  * @border-radius-base from 2px to 4px
  * @border-radius-large from 3px to 4px
* @badge-bg from @gray-light to @gray

# To Do

create template for devs to get started
* header/footer script
* proper css/js files

Break up bootstrap-overides.css into separate css files
* buttons
* etc.

## Discuss

### Links
* ~~Review link colour - hard to read?~~
* changed @link-color color to #3367d6

### Headings (h1-h6)
* ~~Are these headings correct? Not very bold. And secondary text isn't very readable. Grey is very light~~
* changed @headings-small-color to "gray" (lighten(@gray-base, 40%)) where gray-base is #000

### Blockquote
* ~~Blockquote <footer> color too light?~~
* changed @blockquote-small-color to "gray" (lighten(@gray-base, 40%)) where gray-base is #000	

### Tables
* ~~Why are table headings blue and cursor: pointer?~~
* Removed the following from bootstrap-overrides.css (lines 79-85)
```
.table thead tr th {
  color: #0A568A;
  font-weight: 400;
  cursor: pointer;
}
```
* ~~Why are success, info, warning, and danger set to white (not just here, but in several places?)~~
* Changed globally under "Form states and alerts": @state-xxx-text is now @text-color(changed from @brand-xxxx); background (@state-xxx-bg) changed from white to @brand-xxx
* Should active be same colour as hover state?

### Forms
* ~~Why does checkbox label have left hand padding? Doesn't line up...~~
* Removed the following from bootstrap-overrides.css (lines 329-339)
```
.block-label input[type="radio"],
.block-label input[type="checkbox"],
.radio input[type="radio"],
.radio-inline input[type="radio"],
.checkbox input[type="checkbox"],
.checkbox-inline input[type="checkbox"] {
    position: relative !important;
    margin-left: 0 !important;
    margin-right: 5px !important;
}
```

* ~~Why are buttons spaced oddly? Lots of space above/below, but tight left/right~~
* moved .btn-lg style to default btn. Made large, larger.

### Buttons
* ~~Except for spacing, large looks same size as default.~~
* Fixed: added darker outline color to bootstrap-overrides.css (line 121); increased radius in bootstrap (@border-radius-base from 2px to 4px; @border-radius-large from 3px to 7px)

### List group
* ~~.badge colour is too light?~~
* changed @badge-bg from @gray-lighter to @gray
* ~~Why are success, info, warning, and danger set to white (not just here, but in several places?)~~
* changed globally - see above (tables)

### Overall
* The light grey is too light. Maybe just darken it overall

# teststyle

[sitepoint tutorial](https://www.sitepoint.com/introduction-gulp-js/)

Note for Git users: Node.js installs modules to a node_modules folder. You should add this to your .gitignore file to ensure they’re not committed to your repository. *When deploying the project to another PC, you can run npm install to restore them.*

https://github.com/anvoz/bootstrap-tldr