## HTML Concepts

### Emmet
- html boilerplate using !
- Wrap with abbreviation: Ctrl + P > Wrap with abbreviation > emmet command without spaces
	- You don't need to specify the number with the * operator
	- |t to remove list markers from wrapped content
		- Eg: nav>ul.nav>li.nav-item$*>a|t
	- Controlling output position using $#
		- as attribute value or as text node
- Tag Balancing
	- Ctrl + D = outward
	- Ctrl + Shift + D = inward
	- Ctrl + K = remove tag by balacing
- Attribute
	- button[type='button']
		- button tag with attribute button
	- [data='data']
		- div tag with attribute data with value data
- Create children elements
	- >
- Sibling +
- Caret ^ to climb up from from children to sibling
- Grouping using ( )
-  CSS
	- m10 will give you margin: 10px;
	- m10-20 will give you margin: 10px 20px;
	- use tab to complete

### Questions

- Why should you use Emmet?
	- to speed up your work flow
	- to create html structure faster
	- to write css properties faster along with values
- What are some useful Emmet abbreviations?
	- ! to create html boilerplate
	- . # to write classes
	- > to write nested html structures
	- + to write sibling
	- () for groupings
	- {for text}
	- $ for numbers
	- @ for defining numbers
	- [] for including attributes
- What syntax would you use to create this element `<p class="text"></p>`?
	- p.text
- What syntax expands to an element with a child element inside of it? For example: `<div><p></p></div>`
	- div>p
- What syntax would you use to create three elements that have the same class name?
	- element.class*3


### SVG
- they are easily able to scale and retain their quality without increasing their filesize
- useful when you need to change the image programmitically using css or js
- useful for 
	- icons
	- graphs/charts
	- large simple images
	- patterned backgrounds
	- applying effects to other elements using SVG filters
- svg: scalable vector graphics. graphics defined by maths instead of raster graphics - img is defined by grid of pixels
- there is no grid of pixels, there are formulas for different shapes and sizes. scale to any size, it will have no impact on quality and size of the file. 
- defined using xml (extensible markup language) - API, RSS, spreadsheet, word editor software
	- human readable
- good for simple images, not for complex images (eg. grunge texture)
- drawbacks
	- makes code harder to read
	- page less cacheable
	- large svg might delay the rest of your page from loading

### Questions
- What is the xmlns attribute?
	- xml namespace
	- it defines the dialect of the xml, in the case of the svg it is the svg language spec
	- Without it, some browser won't render your image or will render it incorrectly
- What are some situations where you wouldn’t want to use SVG?
	- where the images are complex and have lots of fine details
- What are the benefits of “inlining” your SVGs? What are the drawbacks?
	- benefits: it can be customized with CSS and JS
	- drawbacks: hard to cache, code is difficult to read, might slow down the page

### Tables
- td: table cells
- tr: table rows
- th: table headers
- table tag
- colspan and rowspan attributes for cols or rows to span multiple cells
- colgroup and col elements for styling columns
	- span attribute if the styling for 2 or more columns is same, so you don't have to repeat the col element
- table caption using caption element to give a brief about the table. For accessibility reasons. added just below the table opening tag
- Structure the tables with thead, tbody, tfoot
	- no usefulness in accessibility or visual enhancement
	- 