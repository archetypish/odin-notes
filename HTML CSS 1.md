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
	- thead is usually first element in the table but it will come after colgroup if they are used
	- tfoot - the browser always render it at the end of the table
- in the absence of tbody, and tfoot, you would have to write much more complicated CSS
- nested table: table inside a table. Sometimes it is better to just include more cells or rows
- accessible tables
	- screen readers identify all headers and make associations between headers and cell
	- scope: col or row: header for a row or column
		- rowgroup or colgroup: heading that sits on top of other subheadings but are also headers

### Questions

- What is a table?
	- Table is a type 2 dimensional data structure to organize information related to a set of variables
- Why is it a bad idea to use HTML Tables for page layout?
	- semantically wrong
	- wrong for accessibility reasons
	- non-responsive
	- hard to write and maintain
- What are caption elements useful for?
	- to give a context about what the data is about without reading the data
	- accessible for screen readers
- What is the scope attribute?
	- defines the associative relationship between the row or column headings with the cells


## CSS Concepts

### Default Styles
- Browsers have their own default styles. There is no guarantee that different browsers will apply the same style. Inconsistencies can be minor but they do exist
- the whole idea of a CSS reset is to deal with styling inconsistencies across browsers

### Questions
- Why would you want to use a CSS reset?
	- To remove or reset browser default styles. Since they are different across different browsers, it may introduce some unwanted effects, therefore it is best to reset or normalize them

### CSS Units
- Absolute units: units that are always the same in any context.
	- eg: px. only unit that you should be using for web projects. The rest of the units make sense in print settings because they related to physical units (inches or cm)
- Relative units change based on their context.
	- rem and em: always use rem
		- 1em = font size of the element (font size of the parent if setting the font of element itself)
		- 1rem = font size of the root element (:root or html)
	- using rem to set font size is recommended
	- Viewport units
		- size something relative to the viewport
		- eg: full height heroes, full screen app like interfaces
		- 