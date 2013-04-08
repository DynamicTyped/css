# DynamicTyped CSS/LESS Style Guide(){
//heavily influenced by other style guides across the web *(see [references](#references) below)*.

## <a name='toc'>Table of Contents</a>

  1. [Whitespace](#whitespace)
  1. [Capitalization](#capitalization)
  1. [Colors](#colors)
  1. [Classes / IDs](#classes-ids)
  1. [Rule Declaration](#rule-declaration)
  1. [General Rule Formatting](#formatting)
  1. [Comments](#comments)
  1. [LESS](#less)
  1. [References](#references)
  1. [License](#license)

## <a name='whitespace'>Whitespace</a>

  + Use tabs for indentation
  + One blank line between rule definitions

## <a name='capitalization'>Capitalization</a>

  + Lowercase for html elements, classes and IDs
  + Upper case for hex colors
  
## <a name='colors'>Colors</a>

  + Use hex or argb color codes
  + If a color is used multiple times make a new class -- or better yet a LESS variable

   Correct:
   ```css
   /* we want the color to be used on all main buttons and heading text*/
   @main-color: #0000FF;

   h1,
   h2,
   h3 { 
     	color: @main-color; 
   }

   .main-button {
   		backgrounds: @main-color; 
   } 
   ```

   Incorrect:
   ```
   h1,
   h2,
   h3 {
   		color: #0000FF;
   }

   .main-button {
   		color: #0000FF;
   }

## <a name='classes-ids'>Classes / IDs</a>

  + Do not use abbreviated names
  + IDs should only be used for elements that will be unique to a page (aka use a class if you are going to target multiple elements with this selector)
  + Use dashes for spaces in names *(no camelCase/underscores)*
  + Do not use names that are overly specific.

   Correct:
   ```css
   .main-button{

   }

   .secondary-button{

   }
   ```

   Incorrect: 
   ```css
   .btnMain{

   }

   .topRightBtnOnSomePage{
		
   }
   ```

## <a name='rule-declaration'>Rule Declaration</a>
  + Use standard class, id, html selectors where possible
  + Do not use overly specific selector hierarchy (e.g. `body .navigation#ul li .someText a:visited{`)
  + Avoid selecting items by attribute values
  + When using a grid system, do not add styles to an element by gridsystem class name (unless you are modifying the behavior of the grid system item). Instead, create a more descriptive class name for the element.
  + When using attribute values, use single quotes `.class[href='somepage.html']`
  + Newline between comma separated selectors (no space after comma)
  + Opening brace should be on same line as selector (or last selector)	
  + Use a space between selector (or last selector if it's part of a list) and opening brace
  + Closing brace should match up with the first character of the last selector (or only selector if it's not part of a list).

   Correct:
   ```css
   h1,
   h2, 
   h3 {
   		/*some style*/
   }
   ```

   Incorrect:
   ```css
	h1, h2, h3{
   			  }

   ```

## <a name='formatting'>General Rule Format</a>

  + Do not use single line rules
  + Break-up longer rules with line-breaks and comments
  + One indent for property/values inside a rule
  + Give each property its own line
  + Do not use a space between property and : -- use a space between : and value (e.g. `background: #FF0000;`)
  + Sort property declarations by like properties in alphabetical order (aka not strict alphabetical)
  + Use spaces after commas
  + Spread longer, comma separated, property values across multiple lines 

   Correct: 
	```css
    .row {
    	background: #EDEDED;
    }
    
    .grey-text {
    	color: #777;
    }
	```

   Incorrect:
	```css
    .someStyle{background:blue; } 
	.someOtherStyle
    { 
	   background:red;
	} 
	```

## <a name='comments'>Comments</a>
  
  + Use /* comments rather than //
  + Put comments on separate line
  + Put comments above the code you are commenting

   Correct:  
   ```css
   /* set the background color of this thing to blue */ 
   background: #0000FF; 
   ```  

   Incorrect:
   ```css
   background:blue; //set up the background color to blue
   ```

## <a name='less'>LESS</a>

*Coming soon*

## <a name='references'>References</a>

  Partially Based on a work at [github.com/necolas/idiomatic-css](github.com/necolas/idiomatic-css)
  + [Github's Styleguide](https://github.com/styleguide/css)
  + [Google's HTML/CSS Style Guide](http://google-styleguide.googlecode.com/svn/trunk/htmlcssguide.xml)
  + [ThinkUp's CSS Style Guide](https://github.com/ginatrapani/ThinkUp/wiki/Code-Style-Guide:-CSS)

## <a name='license'>License</a>
DynamicTyped's CSS/LESS styleguide is licensed under the [Creative Commons Attribution 3.0 Unported License](http://creativecommons.org/licenses/by/3.0/). Original references must be kept in any derivatives.
