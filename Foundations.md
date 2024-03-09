- make notes that can serve as prompts for further research

## Asking for Help

- Describe the “XY Problem”.
	- Person is trying to solve the problem X. Person thinks that the solution to X can be achieved through Y. Person doesn't know how to do Y. Person asks community how to do Y. Community helps the person but doesn't understand the full context of why Y would be a problem to solve. 
	- Person implements Y to solve X. It doesn't work. 
	- Person gets back to community and reveals that Y doesn't solve X. 
	- Community now understands the full picture and helps solve X
 - Name the 5 things your question should include.
	 - Detailed Problem Description
	 - What I have tried
	 - What do I want to achieve and why
	 - Code/Pseudo-code or whether it is a conceptual question
	 - Link to lesson/project to indicate where I am

## How Does the Web Work?
- Internet is the technical infrastructure which makes the web possible. Internet is a large network of computers which communicate together
- Summary
	- Internet is a wire. 2 computers connected to this can communicate. 
	- Server is a computer that is connected directly to the internet. Web pages are files on that computer's hard drive. Every server has a unique IP address like postal address. (Gmail, Google)
	- Your computer is not a server since it is not connected directly to the internet. Our computers are called clients because they are connected to internet via ISP
	- Whenever an email/picture travels across the internet, computer breaks the information into smaller pieces called packets. Whenever the information reaches its destination, the packets are reassembled into their original order to make a picture/email
	- Every thing directly or indirectly connected has an IP address (Your computer, Servers and all the equipment in between)
	- Anywhere 2 or more parts of the internet intersect, there is a piece of equipment called a router. They direct your packets around the internet. Whenever a packet reaches a router, its IP address is added (as a wrapper on a candy) to the packet. This happens until it reaches the destination. When the serves sent back packets, it creates a packets with identical wrapping. As it reaches a router, it unwraps a layer to discover where to send the packet next. 
- Summary
	- Data reaches us via a complicated network of Optical Fibre cable (between data centre and your device)
	- Video is stored in data center's computer called server
	- How to transfer the data stored in the data center specifically to your device via the optical fibre cables?
		- IP address: every device is identified uniquely by IP address
			- Your ISP will device IP address of your device
			- Server also has an IP address
			- Since we can't remember all the IP address and A server can store several websites and it's not possible to access all the websites using server's IP address
			- DNS: Internet gets IP address for Domain names (ISP or other organizations can manage the DNS)
		- data is transferred as light pulses via optical fibre cable
		- router converts these light signals to electrical signals
	- Since internet is a global network, there needs to be an organization to manage ip address assignment, domain name registration etc: ICANN
	- Protocols for the management of complex flow of data packets. Rules for data packet conversion. 
- Router only a special type of computer
- Modem to connect our network to telephone infrastructure
- ISP is a company that manages some special routers and can also connect to other ISP's routers
- Internet is this whole infrastructure of networks: 
	- Computer > Router > Modem > Our ISP > Network of Routers of ISP > Other ISP > Modem > Router > Computer
- Internet is the technical infrastructure that allows billions of devices to connect and stay connected. Among these computers, some (web servers) can send messages to web browsers. Web is a service built on top of the internet. There are other services as well. 
- Browser = infrastructure and Search Engine = Service
	- Browser is a program which fetches and displays web pages from the web server
	- Windows/Mac: Systems that allow you to manage files and programs
- TCP/IP communication protocols that describe how data should travel across the internet 
- DNS (Domain name system) is like an address book where browsers looks up the IP address corresponding to the domain name
- HTTP is an application protocol which defines the language using which client and server can interact. Client send http messages to server.
- Order in which component files are parsed: 
	- HTML > CSS and JS  are requested from the server
	- DOM tree from parsed HTML and CSSOM structure from parsed CSS
	- Browser builds DOM tree, applies visual style, execute JS, a visual picture of the page is painted
- Local DNS cache

### Questions
- What is a web server?
	- Web Server is a computer that hosts and ultimately serves a collection of web pages. It may store multiple websites. By hosting, it stores all the files related to the page on its hard drive.
- What is a network?
	- When 2 or more devices are connected by any means i.e. they are transfer or share data with one another then we call that a network
- What is the internet?
	- Internet is the technical infrastructure / largest network of computers which communicate together
- What is an IP address?
	- A unique address given to a each and every device on the internet by the ISP. This is where they are located on the network. 
- What is a router?
	- A special type of computer which makes sure information goes where it is intended to go. 
- What is an ISP?
	- Internet Service Provider. They provide us the access to the internet. It has a network of special kind of routers that can also connect with other ISP's routers to transmit data.
- What are packets and how are they used to transfer data?
	- Packets are chunks of data (image, web page). Data is split up by the server into chunks for ease of transfer and routing via the network. and are reassembled by the browser to show the content. 
- What is a client?
	- Client is any device connected to the internet via the ISP
- What is a server?
	- Server is web server. It is connected directly to the internet. It hosts web pages, web sites, apps
- What is a web page?
	- Web page is a document hosted on the web server usually written in html, containing hyperlinks and handled by web browser
- What is a web browser?
	- program that fetches and serves the web pages
- What is a search engine?
	- Search engine is a service which lets us find the web pages on the internet
- What is a DNS request?
	- DNS request is a request made by the web browser to the DNS server to find out the corresponding IP address of a domain name
- Which browser are you currently using?
	- Google Chrome
- In your own words, describe the process that takes place when you initiate a search on google.com in terms of what we discussed on this section.
	- Our browser sends a dns request to figure out the ip address of google.com if it is not already there in local dns cache
	- It then sends http messages (language) via TCP/IP (vehicle) to Server sitting at IP address. This request goes through routers in the form of packets 
	- Server receives the request, processes it and serves the data back in the form of packets. These packets are again transmitted back via efficient routing and reassembled to view it in the browser

## Command Line Basics
- $ on linux and older macs is called prompt
- Shell or Command Line or Terminal is a program that enable to send commands to the computer and receive output
- Unix shell is both a CLI and a scripting language
- most popular unix shell is bash (bourne again SHell)
- part of the os responsible for managing files and directories on the disk is called file system
- / is the root directory
- Commands
	- ls -F to get details on type of contents
	- ls -t to find the most recent edit
	- cd is to change current working directory
	- .. parent of the current directory
	- . is the current working directory
	- ls -a to see all files
	- absolute path starts with / i.e. the root directory
	- ~ refers to the home directory
	- cd - takes you back to previous directory
- options change the behavior of the command and argument tells the command what to operate on
- More Commands
	- mkdir -p to create parent and child together parent/child
	- nano file.txt to create text files using nano
- extension of the file indicates at what kind of data the file holds
- Commands
	- mv -i (interactive) to get a confirmation before overwriting a file (while renaming)
	- cp multiple file names destination: last argument must be a directory
- wildcard: 
	*  * zero or more characters
	- ? single character
	- when shell sees a wildcard, it expands it to create a list of matching names before running the command
		- if there is no matching file, it will send it as it is
- Command
	- wc for word count
	- ctrl + c to exit expected input mode
	- cat file.name 
		- cat is concatenate
		- prints contents of the file one after another
		- problem: it dumps the whole file on to screen. less is alternative
	- sort -n
		- this does not change the file to numeric but changes the output
	- echo 
		- prints text
	- > text gets overwritten
	- >> text is appended

### Questions
- What is the command line?
	- Command Line or terminal or Shell is a program where you can input instructions to the computer and get output
- How do you open the command line on your computer?
	- Ctrl + Alt + T
- How can you navigate to a particular directory?
	- cd directory/name
	- change current working directory
- Where will cd on its own navigate you to?
	- home directory
- Where will cd .. navigate you to?
	- parent directory
- How do you display the name of the directory you are currently in?
	- pwd
	- print working directory
- How do you display the contents of the directory you are currently in?
	- ls 
- How do you create a new directory?
	- mkdir
- How do you create a new file?
	- touch file.name
	- nano file.name
- How do you destroy a directory or file?
	- rm -r directory
	- rm file.name
- How do you rename a directory or file?
	- mv old.name new.name

## Git and Github
- Git is a version control system
	- local
- Github is a service that allows you to upload,host and manage your code with a web interface
	- remote storage facility
- local and centralized vcs: differences in files and folders. there is a historical record for each save.
- local vs centralized vs distributed version control system
- DVCS: every clone is the full backup of the data
- Other DVCS: delta based version control: set of files and changes made to files
- Git thinks of its data differently: snapshots and not differences. In that sense, git is like a mini-file system.
- All of the history is on local. We can work offline
- It is impossible to make changes to a file without git knowing about it

### Questions

- What kind of program is Git?
	- Distributed Version Control System which helps users track the history of their projects as well as collaborate with other 
- What are the differences between Git and a text editor in terms of what they save and their record keeping?
	- Git captures the snapshots of each version of the project and if there are no changes then it links to the previous version
	- Text Editor saves the latest version of a file
- Does Git work at a local or remote level?
	- It works at a local level
- Does GitHub work at a local or remote level?
	- It is a remote service that allows you to upload, host and manage your code
- Why is Git useful for developers?
	- to track their project history
	- to work with others in collaboration
- Why are Git and GitHub useful for a team of developers?
	- Git is DVCS and with it users are able to get the entire history of the project (from a remote service like Github) on their system. They can then work independently, offline, track project history, collaborate with other by uploading (pushing their changes back to the remote repository at Github)

* origin is the name of the remote connection
* git clone (ssh link)
* git remote -v (to get the url for the remote repo)
* git status
* git add file.name (to add file to the staging area)
* git commit -m "message"
* Ctrl + \` 
	* to open terminal in VS code
* git add . 
* git log 
* git push origin main or just git push
* Best practices
	* Atomic Commits
		* commit that include changes to just one feature or task of a program
		* Why?
			* Easy to revert if something goes wrong
			* Better commit messages
	* and leveraging those atomic commits to make your commit messages more useful to future collaborators

### Questions 2


- How do you create a new repository on GitHub?
	- Using the Green button
- How do you copy a repository onto your local machine from GitHub?
	- git clone SSH link
- What is the default name of your remote connection?
	- origin
- Explain what origin is in git push origin main.
	- default name of the remote repository (connection)
- Explain what main is in git push origin main.
	- default branch
- Explain the two-stage system that Git uses to save files.
	- Modified: if a change is made to a file, it is said to be modified
	- Staging area: if that change needs to be captured in that upcoming snapshot, it needs to be staged
	- Committed: Staged changes are then committed or captured in the snapshot
- How do you check the status of your current repository?
	- git status
- How do you add files to the staging area in git?
	- git add name of file or git add . to add all
- How do you commit the files in the staging area and add a descriptive message?
	- git commit -m "message"
	- atomic changes and messages
- How do you push your changes to your repository on GitHub?
	-  git push origin main
- How do you look at the history of your previous commits?
	- git log

## HTML

- coding language

### Questions

- What do HTML and CSS stand for?
	- Hypertext Markup Language
	- Cascading Style Sheet
- Between HTML and CSS, which would you use for putting paragraphs of text on a webpage?
	- HTML
- Between HTML and CSS, which would you use for changing the font and background color of a button?
	- CSS
- What is the difference between HTML, CSS and JavaScript?
	- HTML provided the structure to the page. Markup Language. 
	- CSS provides the style and layout. Styling Language
	- JS provides interactivity. Programming Language
- self closing tags and void elements:
	- (historical) self closing tags: `<br/>`
	- (correct) void elements: `<br>` 
- Hypertext (text that can link to other pages or things)

### Questions 2

- What is an HTML tag?
	- It is what HTML uses to mark up the content. HTML elements are sort of like containers where tags (opening and closing tags) describe the meaning with their label between `<>`. The browser then uses this information to interpret and format the content.  
- What are the three parts of an HTML element?
	- opening tag. marks the start of the content while also conveying what it is
	- content. actual content
	- closing tag. marks where the content ends


### HTML boilerplate
- index.html: every web server looks for this file to load whenever a user lands on our website
- doctype declaration: which version of html should be used to render the page
- root element: `<html></html>`
- attributes provide additional information about the elements
	- lang attribute: to improve accessibility 
	- specifies the language of the text content within the element
- title tag: tab and google search results
- Open file via terminal: google-chrome index.html

### Questions


- What is the purpose of the doctype declaration?
	- To convey to the browser what version of html to use to render the page 
- What is the HTML element?
	- it is the root element which contains everything about and on the page
- What is the purpose of the head element?
	- it contains all the meta information about the page so that everything renders correctly
- What is the purpose of the body element?
	- It contains all the content on the page that is displayed to the user

### text elements

- html compress new lines into single white space
	- Browsers ignore empty spaces. They only care about the first one
- real meaning behind headings, it is not just visual representations
- em - where you put emphasis on a piece of text when you speaking it
- strong - emphasis plus marking key words as important as well for people who are skimming the document
- i and b don't are for visual representation

### Questions

- How do you create a paragraph in HTML?
	- `<p></p>`
- How do you create a heading in HTML?
	- `<h1></h1>`
- How many different levels of headings are there and what is the difference between them?
	- h1 to h6. There are 6 levels of headings. There is difference in hierarchy. h1 is more important and higher up in the hierarchy of the document than h2 and so on
- What element should you use to make text bold and important?
	- `<strong></strong>`
- What element should you use to make text italicized to add emphasis to it?
	- `<em></em>`
- What relationship does an element have with any nested elements within it?
	- Parent element nests its children elements
- What relationship do two elements have if they are at the same level of nesting?
	- They are siblings
- How do you create HTML comments?
	- `<!-- -->`

### Lists

### Questions

- What HTML element is used to create an unordered list?
	- `<ul><li></li></ul>`
- What HTML element is used to create an ordered list?
	- `<ol><li></li></ol>`
- What HTML element is used to create list items within both unordered and ordered lists?
	- `<li></li>`


### Links
- absolute links: protocol://domain/path
	- if you don't specify the protocol, then the browser will look for domain in the current directory as a file
- ./ 
	- for relative paths
	- start looking for the file or directory relative to the current directory
- Spaces
	- %20
	- on a server this could cause some problems
- Images
	- JPGs are good for photos
	- GIFs are good for animation
	- PNG are good for diagrams and icons and logos
	- SVG are good for everything. But issue is size when it comes to ones that include some text

### Questions


- What element is used to create a link?
	- `<a href=""></a>`
- What is an attribute?
	- It provides additional information to the element. They are usually in the name and value format but they can be without value as well like a flag
- What attribute tells links where to go to?
	- href in case of links
- What security considerations must be taken if you wish to use the target attribute to open links in a new tab/window?
	- using the attribute `rel="noopener noreferrer"`
	- noopener prevents destination page from gaining  access to the source page
	- noreferrer prevents passing on the information about the source page to the destination page. It also prevents the access and can be used by itself
- What is the difference between an absolute and relative link?
	- Absolute link is the absolute path of an asset and is in the format protocol://domain/path
	- Relative link is the relative path of a document/asset on the same server
- Which element is used to display an image?
	- `<img src="" alt="">`
- What two attributes do images always need to have?
	- src (destination path) and alt (alternative text) - incase of screen readers and in case someone has disabled images or if image fails to load
- How do you access a parent directory in a filepath?
	- ../
- What are the four main image formats that you can use for images on the web?
	- JPG for photos
	- GIF for animations
	- PNG for diagrams and icons
	- SVG for almost anything PNG is used for but being wary of the size


### Commit Messages
- Commit message
	- for fellow developers and your future self
	- context
	- (what) changes were made and why
	- (why) what problems your commit solves and (how) it solves them - code explains how
	- a subject and a body
		- subject (what): a brief summary of the change you made to the project: `this is the change I made to the codebase`
		- body: (why) Describe the problem your commit solves and how
		- separate subject from body with line break
- When
	- meaningful change in code
- Commands
	- git log --shortline
	- git shortlog
- 7 Rules
	- Separate subject from body with a blank line
	- Limit the subject line to 50 characters
	- Capitalize the subject line
	- Do not end the subject line with a period
	- Imperative Mood
		- as opposed to indicative mood
		- If applied, this commit will 'your subject line here'
		- Only for subject line, you can relax this for the body
	- Wrap the body at 72 characters
	- Just focus on making clear the reasons **why** you made the change in the first place. 2 Parts to it. 
		- (The problem - The Why) The way things worked before the change was made-What was wrong with that
		- The way they work now and why you decided to solve it this way

### Questions

- What are two benefits of having well-written commit messages and a good commit history?
	- You make it easy for fellow developers and yourself to view the project history and understand what was changed and why
	- a good commit history shows you are a good collaborator to prospective employers
- How many characters should the subject line of your commit message be?
	- 50 characters or less with first word capital with no period and in an imperative mood as opposed to indicative mood

## CSS

### Selectors
- Class is just an attribute you place on the html element
	- multi-worded class names should be separated by hyphen
- Grouping selectors using comma
- Chaining selectors
	- .class1.class2 : has both class1 and class2
	- we can't chain more than 1 type selectors as an element can only be one type at once
- Descendant combinator

### Properties
- color: transparent

### Questions


- What is the syntax for class and ID selectors?
	- `.class-selector`
	- `#id-selector`
- How would you apply a single rule to two different selectors?
	- grouping them using ,
- Given an element that has an id of title and a class of primary, how would you use both attributes for a single rule?
	- `#title.primary`
- What does the descendant combinator do?
	- select the descendant of the parent
- What are the names of the three ways to add CSS to HTML?
	- inline
	- internal
	- external
- What are the main differences between the three ways of adding CSS to HTML?
	- inline css is added directly in the html element. There will be lot of duplication in case a style needs to be replicated across the page
	- internal css is added in the head of the html element inside style attribute. There will be lot of replication in case similar styles need to be applied across pages
	- External css is added in a different file without having to bloat the html file itself. this is then linked to the html file

### The Cascade
- the cascade is what determines which rules do get apply to the the html
- three factors that the cascade uses to determine this
	- specificity
		- only taken into account when an element is targeted with multiple, conflicting declarations
		- when there are no declarations with a selector of higher specificity, then the rule with the higher number of selectors of the same type is more specific
		- symbols in combinators and universal selectors does not add to specificity
	- Inheritance
		- certain css properties when applied to elements are inherited to descendants even if we don't explicitly write a rule for those descendents
		- Exception to this is when we target the element directly
	- Rule Order
		- whichever rule is last defined is the winner

### Questions
- Between a rule that uses one class selector and a rule that uses three type selectors, which rule has the higher specificity?
	- class selector is more specific than type selector
	- 3 type selector will be more specific than 1 type selector

### Devtools
- Elements Pane
	- Ctrl + Shift + C
- Ctrl + Shift + P: Command Menu 
- Devtools can be undocked as well
- CSS
	- Computed pane, what declarations are being applied
	- Search the DOM tree:  Ctrl + F
- Last Panel
	- Ctrl + Shift + I
		- to open the last open panel
		- Close and open - Refresh
	- F12 
- Panel Layout Customization
- Edit Keyboard shortcuts
- DOM
	- browser parses the html to create a tree of objects. Each object of the tree is a node. Entire tree representing the page's content is the DOM
	- html represents initial page content. dom represents current page content. When JS adds, removes, changes nodes, the dom becomes different from html
- Scroll into view using 3 dot menu
- $0 to view the current node
- jump between attributes using tab 

### Questions

- How do you select a specific element on your page with your browser’s developer tools?
	- hover over it and right click and inspect
	- Use inspector mode and hover and the element is highlighted in the DOM
- What does a strikethrough in a CSS declaration mean in your browser’s developer tools?
	- That specific declaration is being overwritten
- How do you change CSS in real time on specific elements of a web page with your browser’s developer tools?
	- In the styles pane. Add new declarations in elements.style as inline style or edit existing declarations by double clicking them

### Box Model

- height and width by default is set for the content
- margin collapses between 2 elements that are next to each other. Whichever one that is the largest is the one that will be used
- box-sizing: border-box
	- height and width includes the padding and border
- inner display type and outer display type
	- setting the inner display type to flex does not change the outer display type of block
	- This can be changed via the display property
- The box's area does not extend to margin. it stops at border.
- `html { box-sizing: border-box`}
- `*, *:before, *:after {box-sizing: inherit;}`
- no negative padding
- standard and alternative box model
- inline boxes
	- height and width are ignored
	- top and bottom margin, padding and border are respected but it doesn't change their relationship with the content around it. The left and right padding, border and margin move away other content from the box
- inline-block boxes
	- height and width are respected
	- padding, border, margin move other content away from the box
- shorthand for margin
	- margin-top margin-right margin-bottom margin-left
- collapsing margins: only top and bottom

### Questions
- From inside to outside, what is the order of box-model properties?
	- padding > border > margin
- What does the box-sizing CSS property do?
	- changes how the size of the box is computed
	- if it is context-box then width and height defines the size of the content box
	- if it is border-box then width and height defines the visible part of the box (until the border)
- What is the difference between the standard and alternative box model?
	- standard box model 
		- box-sizing: content-box (default). width and height defines the size of the content box. To calculate the actual covered area of the box, we need to add 2xpadding and 2 times border width
	- alternative box model
		- this is box-sizing: border-box. Width and height includes the size of padding and border already
- Would you use margin or padding to create more space between 2 elements?
	- margin
- Would you use margin or padding to create more space between the contents of an element and its border?
	- padding
- Would you use margin or padding if you wanted two elements to overlap each other?
	- margin. Negative margin.
- How do you set the alternative box model for all of your elements?
	- `html {box-sizing: border-box;}`
	- `*, *:before, *:after {box-sizing: inherit}`
- How do you center an element horizontally?
	- `element {width: 100px; margin: 0 auto;}`


### Block and inline elements
- padding and margin behave differently on inline elements
- divs and span are good for grouping elements if no other semantic element can be used
- how elements lay themselves out if you haven't changed their layout
- display: inline
	- we can't set width and heights except in img
- using margin to align items

### Questions
- What is the difference between a block element and an inline element?
	- block element occupies 100% of the width of the parent container all the way from left to right. They stack on top of one another i.e. a new block element starts from a new line going from top to bottom in English.
	- an inline element takes as much space as it is needed to occupy the content. They start where the previous inline element ends.
	- block can contain an inline element but inline cannot contain an block element
	- height, width, top and bottom margin, padding are not respected in inline lement
- What is the difference between an inline element and an inline-block element?
	- inline-block combines both block and inline in the sense that width and height are now respected as well as top and bottom padding, margin
	- They don't start from the new line
- Is an h1 block or inline?
	- block
- Is button block or inline?
	- inline
- Is div block or inline?
	- block
- Is span block or inline?
	- inline

## Flexbox

### Introduction
- Flexbox is a way to arrange items into rows and columns
- not just one property, but a whole toolbox of properties
- flex-container: container that has display: flex on it
	- flex items: element that lives directly inside of flex-container


### Questions

- What’s the difference between a flex container and a flex item?
	- flex-container is any element that has `display: flex;` applied to it. flex-items are elements that live directly inside of flex-container
- How do you create a flex item?
	- do `display: flex;` on any element and its direct children are then flex-items

### Growing and Shrinking
- `flex` is a shortland for 3 properties that you add to a flex-item. This will affect how flex-item will size itself within their container
- flex: flex-grow flex-shrink flex-basis
	- `flex: 1/any other positive number`
		- `flex-grow: 1; flex-shrink: 1; flex-basis: 0;`
		- `1 1 0`
		- when defined with 1 value, value is put to flex-grow
			- any other positive number
		- flex-basis: 0;
	- `flex: auto or any number with unit
		- `flex-grow: 1; flex-shrink: 1; flex-basis: auto;`
		- auto is flex-basis default value. sizes based on width/height
		- `1 1 auto`
	- `flex: initial`
		- `0 1 auto`
		- Sizes based on width and height
	- `flex: none`
		- `0 0 auto`
		- Sizes based on width and height
	- 
- flex-grow:
	- flex items growth factor
	- flex-grow: 1;
		- every child should grow the same amount
	- flex-grow: 2;
		- to just one child. that child will grow 2x the other items
	- defaults to 1 when omitted
- flex-shrink
	- flex items shrink factor
	- it only ends up getting applied if the size of all flex items is larger than their parent container (flex container)
	- default is 1
	- defaults to 1 when omitted
- width is not respected with flex-grow or flex-shrink
	- even if you have specified a width to a flex-item
	- when there is empty space, flex items will grow to fill that space
	- when they are larger than their parent, they would then shrink
- flex-basis
	- initial size of a flex-item so any sort of flex-growing or flex-shrinking will start from that size
	- default is auto but flex: 1 is (1 1 0)
	- with flex-basis set to 0, width is ignored
	- flex-basis: auto
		- check for width declaration
	- defaults to 0 when omitted
- Common use cases
	- flex: 1; 
		- to make divs grow evenly
	- flex-shrink: 0;
		- to prevent certain divs to shrink
- by default flex-items don't shrink below their content size

### Questions

- What are the 3 values defined in the shorthand flex property (e.g. flex: 1 1 auto)?
	- flex: auto is flex: 1 1 auto;
	- flex-grow: 1
	- flex-shrink: 1
	- flex-basis: auto; (look for width)
- What are the 3 defined values for the flex shorthand flex:auto?
	- flex-grow: 1;
	- flex-shrink: 1;
	- flex-basis: auto
- for flex: initial
	- flex: 0 1 auto;
- flex: none
	- flex: 0 0 auto;
- flex: 1;
	- flex: 1 1 0;

### Axis
- flex-direction: column;
- direction of axes - main axis and cross axis - that changes when flex-direction is changed

### Questions
- How do you make flex items arrange themselves vertically instead of horizontally?
	- flex-direction: column;
- In a column flex-container, what does flex-basis refer to?
	- height of a flex-item
- In a row flex-container, what does flex-basis refer to?
	- width of a flex-item
- Why do the previous two questions have different answers?
	- because direction of the main axis is changed from horizontal to vertical

### Alignment
- justify-content aligns the items across the main axis
- align-items: across cross axis
- when we change the direction of main axis to vertical and cross axis to horizontal, we change their behavior as well
- gap
- flexbox
	- what problem does it solve? all about arranging a group of items in a row or column. css grid solves a different problem
	- primary axis: distribution of the group: justify-content
	- cross-axis: align-items
	- align-self: this is applied to the items instead of the container. align-items is syntactic sugar for align-self for all items at once. 
	- There is no justify-self
	- content vs items:
		- on cross-axis: each of the item can move without interfering with any other item
		- on main-axis/primary axis: this is not the case. each item can not move without interfering with other items
		- Therefore we can think on an item level when it comes to cross axis while on the primary axis, it is only as a group
	- def
		- justify: to position something on the primary axis
		- align: to position something along the cross axis
		- content: a group of stuff that can be distributed
		- items: single items that can be positioned individually
	- in flexbox, width is like a suggestion than a hard constraint. It's called a hypothetical size
	- flex-basis is also like a suggestion than a hard-constraint
	- hard minimum limit - flex-basis or width
	- the flexbox refuses to shrink below the minimum size. For input text container, it is around 200px and for text, it is the size of the longest unbreakable string of characters
		- we can redefine this minimum size with min-width property
		- eg min-width: 0;
	- auto margins in the navigation menu to separate the logo and the navigation links
- Use cases
	- any width or max-width applied to an image will become flex-basis
	- flex: auto; (items grow or shrink from the size of the content or any other size directly applied to the content)
	- **part of the media object (box that contains the image) takes the sizing information from the image** and the body of the media object can take up rest of the space
		- constrain the image to its original size by using img width of max-width: 100%;
- gap, row-gap, column-gap
	- gap: 1px 2px;

### Questions
- What is the difference between justify-content and align-items?
	- justify-content is a way to distribute the space on the primary or main axis. The content as a group is arranged along the primary or the main axis. Each move impacts others so the move is as per the group
	- align-items is a way to move multiple items at once along the cross axis. Each item move is independent of the other
- How do you use flexbox to completely center a div inside a flex container?
	- add justify content as center, and align-items/align-self as center
- What’s the difference between justify-content: space-between and justify-content: space-around?
	- space between: the space is distributed evenly between all items such that the items on the far left and far right are pushed all the way towards left and right respectively
	- space-around: the space around each item looked in isolation is equal such that space between 2 items is twice the space as it adds up


## JavaScript

### Fundamentals 1
- Variables - named storage for data
	- let keyword to create or declare a variable
	- the assigned value is then stored in the memory area associated with the variable
	- a variable should be declared only once
	- functional languages like Haskell doesn't allow changing variable values
	- $ and _ can be used in names of the variables. First letter can't be digits (numbers).
	- reserved names not to be used
	- to declare constants use const
	- use constants for difficult to remember values that are known prior to execution. capital letters and _
		- There are constants whose value is known prior to execution and there are constants who value is calculated in runtime during execution whose value do not change after the initial assignment
		- capital named constants are aliases for hard coded values
	- variables should be named such that it is obvious what's inside them
- Numbers
	- operands and operators
	- literals: 10, 20
	- variables
	- expression: (10 + 20) * a
	- % modulus operator returns remainder
	- x ** 2 exponent  = Math.pow(x,2)
	- multiplication and division have same precedence. subtraction and addition have same precedence. When there is same precedence, the operations are done from left to right
	- only one type for both decimals and integers
	- scientific notation using e5 or e-5 like 10^5 or 10^-5
	- floating point arithmetic is not 100% accurate. solve it by multiplying and dividing by 10
	- adding a string and a number is always  a string
	- JS converts strings to numbers for all arithmetic operations
	- NaN : js reserved keyword telling that a number is not a legal number
		- typeof NaN is number
	- typeof Inifinity
	- normally, numbers are js primitive values created with literals but they can also be created as objects using new keyword
	- typeof is an operator
	- increment and decrement can't be applied directly to a value: since we are assigning the variable an updated value and not operating on the value itself
	- === and == 
		- === values are same and datatypes are same (recommended)
		- == only values are same
	- booleans allow to make decision in our code
- + only works with strings for concatenation while other operators convert them to numbers and carry out the operation
- + unary converts non-numbers to numbers when put in front of them
	- does the same thing as Number but shorter
	- unary plus is applied first, then binary plus (higher operator precedence)
- = assignment is also an operator
	- think of it as an operator
		- x = 2 * 2 + 2
	- all operators return a value
	- x = value. This call writes value into x then returns it
	- so assignment can also be used in an expression
- modify and assign operator += -= *= /=
	- they have the same precedence as assignment operator
- increment and decrement operator
	- postfix or prefix
	- we can only see the difference if we used the returned value
	- can be used inside expressions. The precedence is higher than most operations.
- code readability: 
	- one line does multiple things - not good
	- one line - one action
- comma operator 
	- lowest operator precedence
- let x = 10
	- returns undefined in the console
	- you cannot declare, assign and read x's value in the same line

### Questions
- Name the three ways to declare a variable
	- let, const, var
- Which of the three variable declarations should you avoid and why?
	- var should be avoided since it is the old way and can cause issues. let and const are the modern way of declaring the variable
- What rules should you follow when naming variables?
	- should not start with digits
	- can include symbols like $ and _
	- should be camel case likeThis
	- should be descriptive enough to tell what's in it
	- should not be reserved keywords like return, let
- What happens when you add numbers and strings together?
	- numbers are converted to strings and they concatenate. usually.
- How does the Modulo (%), or Remainder, operator work?
	- does integer division and returns the remainder
- Explain the difference between `==` and `===`.
	- `==` tests only the value
	- `===` checks on both value and type. this is stricter
- When would you receive a NaN result?
	- when you try to perform a numerical operation where it isn't valid
- How do you increment and decrement a number?
	- a++ or ++a
	- a-- or --a
- Explain the difference between prefixing and postfixing increment/decrement operators.
	- incrementing or decrementing the number and then returning the result
	- incrementing and decrementing after returning the number as is
- What is operator precedence and how is it handled in JS?
	- to decide which operation to perform first in case of a conflict
	- There is a priority list for all operator types including assignment which has the least priority and unary operator like + and - which has the highest priority
- How do you access developer tools and the console?
	- ctrl shift j
- How do you log information to the console?
	- console.log
	- alert
- What does unary plus operator do to string representations of integers? eg. +”10”
	- converts it to a number

### Fundamentals 2

- a variable can be initialised with a number but then later can store a string. the type of data a variable stores can be changed and that a variable is not bound by data type. Such type of programming languages that do this are called dynamically typed
- Special numeric values
	- NaN represents computational error. result of undefined or incorrect mathematical operation. It is sticky except for raised to the power 0.
	- Infinity as it is or 1/0 or
- BigInt for integers of arbitrary length
- null value is a separate type which contains only null value
	- special value which means nothing, empty or value unknown
- undefined
	- value is not assigned
	- variable is declared and its value is not assigned
	- initial value
- object
	- all other stuff like numbers, strings are primitive data types because they contain single thing
	- objects are different. they can contain collections or complex things
	- symbol: to create unique identifiers for objects
- typeof operator
	- returns string of type
	- typeof() - not a function, only mathematical grouping
- Primitive (number, bigint, boolean, string, null, undefined, symbol) , Complex DataStructures (object)
- Strings
	- use single quote or double but stick to one
	- template literal: strings with back ticks
		- embed js
		- span multiple lines
	- use \n to jump new lines in normal strings but keep all text in the same line
	- use backslash \ to escapte characters
		- escaping means we do something to them so they behave like text and not code
	- strings are primitive and immutable. all string methods produce a new string without altering the existing string
	- .at .charAt and []
		- .at can use negative numbers other can't
		- charAt returned empty string if a char isn't found while [] returns undefined
		- we can't update any character
	- slice, substring, substr
		- slice (start, end) takes negative numbers as inputs
		- substring - same but converts negative numbers to 0
		- substr - same as slice but the second part is length. can take negative starting position
	- str.concat(newstr, newstring2)
		- str is not modified but a new string is returned
	- convert a num to string using .toString() method
	- method: a bit of a functionality built into the language or the datatype
- Comparison Operators
	- comparing strings. unicode ordering.. a> A (as per the internal encoding js uses)
	- when comparing values of different types, js converts them to numbers
		- this is the case with ==
		- while a strict equality checks equality without type conversion i.e. if a and b are of different types then a false is returned without an attempt to convert them
		- **for == , null and undefined are equal except for any other value. for other comparison operators, null is converted to 0 while undefined is converted to NaN**
			- compare null and 0 with all comparison operators
		- NaN returns false for all comparisons. undefined gets converted to NaN with comparison operators
- Conditional Statements: if , if else, else
- Logical operators: test multiple conditions without writing nested if and else
	- can be applied to any data type and the return can be of any type
	- when applied, they convert the operand to boolean type and return the original value
	- OR || if the operand is not boolean it is converted to boolean for the operation
	- most of the time or is used in the if statement to test multiple conditions
	- a chain of || returns the first truthy value or the last value in case all of them turns out to be falsy
	- a chain of && returns the first falsy value or the last value in case all of them are found to be truthy
	- precedence of && is higher than ||
	- don't replace if with &&
	- ! converts to boolean type and returns the inverse value
		- therefore !! is used to convert to boolean type
		- Boolean function can also be used in its place
- Any value that is not false, undefined, null, 0, NaN, "" returns true if used by itself as a conditional statement
- Switch statement:
	- large number of choices with simple condition and a simple task against each condition
- Ternary operator
	- condition ? code to run if it is true : code to run if it is false
- an if statement evaluates the expression in the parenthesis and converts it into a boolean value
	- 0, "", false, undefined, NaN, null - false because they are falsy values and all other values are truthy values
- the else clause
- the ? question mark operator is called ternary operator because it has 3 operands
	- ? has low precedence so it is usually executes last so there is no need for parenthesis (for the condition) but it makes the code more readable
- ? is mostly used for variable assignment and it shall not be used in place of if else to run a piece of code
- switch statement: strict equality check
	- all cases are evaluated without check in case case break isn't used
		- therefore several variants of case which share the same code can be grouped (without break)
	- no need to use break for default

### Questions

- What are the eight data types in JavaScript?
	- Primitive data types
		- number (Infinity, NaN)
		- strings
		- boolean
		- undefined
		- null
		- BigInt
		- Symbol
	- Objects
- Which data type is NOT primitive?
	- Object data type
- What is the relationship between null and undefined?
	- They are equal to one another using == (non strict equality) and nothing else
	- They form their own type
	- undefined is something whose value is not yet assigned
	- null is empty or value unknown
- What is the difference between single, double, and backtick quotes for strings?
	- There is virtually no difference between three except for the fact that backtick strings are somewhat special and they are called template literals and they can accomodate variables using ${variable} notation
- What is the term for joining strings together?
	- concatenation
- Which type of quote lets you embed variables/expressions in a string?
	- backticks
- How do you embed variables/expressions in a string?
	- ${variable} notation inside backticks
- How do you use escape characters in a string?
	- using backward slash \' or \"
- What is the difference between the slice/substring/substr string methods?
	- slice starting and ending point. Can use negative values
	- substring can't use negative values. convert them to 0.
	- subtr using starting point and length
- What are the three logical operators, and what do they stand for?
	- they are used when we want to check multiple conditions
	- OR - at least one of them conditions needs to be true. seeks first truthy value and then returns the original value
	- AND - all of the conditions needs to be true. seeks first falsy value and then returns the original value
	- NOT - negates a value. double negation is used to convert any value to boolean value
- What are the comparison operators?
	- they are used to compare 2 values. They do so by converting them first to numbers and then returning a boolean value
- What are truthy and falsy values?
	- truthy value are values which are converted to true when evaluating conditional statements
	- falsy values are values which are converted to false when evaluating conditional/logical statements
		- 0, false, "", undefined, null, NaN
- What are the falsy values in JavaScript?
	- already specified
- What are conditionals?
	- they are used to make decision in code based on some condition and carry out a specific action
		- if else if else
		- switch
		- ? ternary operator
- What is the syntax for an if/else conditional?
	- if (condition){} else if (condition two){} else {} 
- What is the syntax for a switch statement?
	- switch (expression) { case expression: code break;}
	- strict equality
	- default option
- What is the syntax for a ternary operator?
	- let a = condition ? option 1 if condition true: option 2 if condition false
- What is nesting?
	- nesting is when adding another layer of decision making if the specified condition is not met
		- if (condition) {} else { if () {}}
		- condition ? option1 : condition2 ? option 2: option 3
### DevTools
- DOM
	- html is a page with instructions on structure of the document. The browser needs to parse and process html to form a tree of objects. Each object of the tree is a node. and the entire tree representing the page's content is the dom (document object model)
	- html can be different from its dom (js runs and changes an element)
		- html represents initial page content
		- dom represents current page content
	- ctrl + f to search through the DOM
	- scroll into view
- Mobile view
	- Ctrl + Shift + M
	- DPR: Device Pixel Ratio : ratio between physical pixel on the device and logical pixel in css
		- DPR tells chrome how many screen pixels to use to draw a CSS pixel
- Debugging JS
	- file navigator, code editor and js debugger (the Sources panel)
	- console.log will always solve the problem but breakpoints will solve it faster
	- Breakpoints
		- line of code breakpoint
			- use this when you exact region of code that you need to investigate
			- devtools pauses before this line is executed
			- it can be set in the code using code, `debugger;`
		- Conditional line of code breakpoint
			- use this when you want to stop the execution of code at a line only when a condition is being met
				- loop
		- Log Line of code breakpoint
			- use this to log messages to the console without stopping the execution of the code and without cluttering up the code with console.logs
		- DOM Change breakpoint
			- use this when you want to pause on code that changes a DOM node and its children
			- DOM breakpoints in Elements and Sources panel
		- XHR/fetch breakpoints
		- Event Listener Breakpoint
			- click breakpoint mouse
			- use it when you want to pause on code that runs after an event is fired
		- Exception breakpoints
			- use when you want to pause on line of code that throwing a caught or uncaught exception
		- Function breakpoints
				- call `debug(functionName)` when you want to pause whenever a function `functionName` is called
	- Console API
		- Info warning error
			- console.log to log message the info level
			- console.warn to log message at the warning level
			- console.error to log message at the error level
		- by default we can see messages at all levels
		- console sidebar
		- console.clear() to clear the console 
		- console.table() to log array as table
		- console.dir() to log as json
		- console.group()
			- to group console messages until console.groupEnd() is called
			- console.groupCollapsed() - group nesting
		- console.count()
		- console.countReset()

### Questions
- How do you open developer tools?
	- Ctrl + Shift + J to open console
	- Ctrl + Shift + C to open elements tab
	- Right click and element and inspect
	- Ctrl + Shift + I to open last open tab
- How do you change screen size of a website using developer tools?
	- By switching to Device simulation mode or responsive mode, and entering the screen size in the device toolbar option
- What is a breakpoint?
	- breakpoint is when your code is paused during execution at a particular point based on your selection
		- line of code, log line of code, conditional line of code etc
- How do you set a breakpoint?
	- Using the Sources panel
		- JS Debugger
		- Code Editor - Line of code breakpoint
	- Elements panel for DOM breakpoint
	- in the code
		- using debugger; command

### Functions
- functions: they allow you to store a piece of code that allow you to do a single task inside a defined block and then allow us to call that code whenever you need to do that with a single short command
- invoke - fancy word for running or executing a function
- built in browser function are written in lower level languages like C++ and not in web language like JS. 
- functions that are part of objects are called methods. 
- you can call other function inside the functions
- function expression: anonymous functions
- function declaration: standard functions
- scope
	- conflict with global variable declaration when there are 2 or more scripts being loaded
	- keeping parts of your code locked away in functions avoids this and is considered a best practice
	- the same scoping rules do not apply to loops or conditions
- return values
- parameters and arguments
	- we declare functions listing their parameters and we call them passing their arguments
- local variables: variables declared inside the function are available only inside the function
	- if the same named outer variable function is declared inside the function then it shadows the outer one
	- it's a good practice to avoid use of global variables. Most variables reside in their functions.
- parameters: when the function is called, the values passed to function parameters are copied to local variables
	- so if a parameter is not passed and the same values exist in the global scope then that value will be passed to function as a copy
	- such that the value is changed then it would not impact the global value
- default value is still used if we pass undefined as an argument to the function
- return directive can be anywhere and can have multiple instances
- no return is same as just return; is just same as return undefined
- functions are actions so their name is usually a verb
	- a glance at a function name should tell what kind of work it does and what kind of value it returns
- one function - one action
- a separate function is not only easy to test and debug but is also a great comment
- functions can be created even if we don't have any intention of using them again. It makes the code more readable. 
- known prefix:
	- get...
	- show...
	- check...
	- create...
- function declaration and function expression
	- both are values
	- using it without parenthesis - string representation - source code
	- copy the function code to another function
	- semicolor at the end of function expressions
- callback functions
	- we pass functions as arguments and expect them to be called back later if necessary
- functions are value representing actions
- Function expressions and Function Declarations
	- When
		- Functions expressions create functions when the execution reaches it and from then only they are available to be used
		- Function declaration create functions and can be used before the execution reaches them
	- Block
		- in strict mode, the function declaration has block scope so conditionally declaring the function won't make it available outside the block
		- we can use expressions and declare the variable in the global scope
- Arrow function with and without {} braces
- JS Call Stack
	- mechanism to keep track of function calls
	- js engine uses a call stack to manage execution context: global or function
	- LIFO

### Questions

- What are functions useful for?
	- wrap a piece of code that performs one action into a reusable block of code which can be called whenever required to perform the same task
	- improve readability by making function describing the code like comments do
	- declaring local variables to be used by function rather than global variables
- How do you invoke a function?
	- function()
- What are anonymous functions?
	- function which cannot be used later but are called by another function on the spot and serve their purpose
- What is function scope?
	- function looks for stuff in the function scope during execution, and if not found then go outside its scope to look for stuff in global scope
	- function scope is defined as such that local variables declared inside a function (like parameters) are not accessible outside the function scope. This helps with scenarios when you load outside scripts and there are similarly named variables or even functions so there is no conflict. 
	- functions can still access variables in the global scope but not the values in another functions local scope
- What are return values?
	- whatever the function returns once it finishes execution of input data
- What are arrow functions?
	- modern way to represent functions with a fewer key strokes


### Problem Solving
- core thing software developers do. The programming languages and tools they use are secondary to this fundamental skill
- problem solving is writing an original program that performs a particular set of tasks and meet all stated constraints
- the best way to improve on problem solving skills is by building experience by making lots and lots of programs. the more practice you have the better you will be prepared to solve real world problems
- Understand the problem
	- when you can explain the problem to someone in plain English, you understand it
	- if you don't understand the problem you won't know when you have solved it or may work towards the wrong solution
- Plan
	- don't jump into coding. plan out how you are going to solve it
	- questions to ask yourself
		- Does your program have a ui? how does it look like? what functionality does it have? draw it on paper
		- inputs: how will you get the data? user or somewhere else
		- desired output
		- steps that you need to take to get from input to output
			- write an algorithm to solve the problem. algorithm is like a recipe to solve a problem. It defines the steps need to be taken by the computer to solve the problem in pseudocode 
			- what is pseudocode?
				- logic for the program in natural language instead of code
			- Divide and conquer
				- subproblems - each of the steps you wrote out in pseudocode is a sub problem. pick the smallest and simplest and then start with code from there. 
				- the algorithm might be incomplete in the beginning
				- solve each of the small problems until you solve the problem
- the best way to solve problems is by having a framework and practising it
- Video
	- Coding has 8 main concepts that are consistent across languages
	- Learn how to use these concepts in English
	- Write out these concepts first in english and convert them to code later
	- code is there to explain comments to the computer
	- new variable 
		- algorithm: create a variable `name` of type `type` with initial value `initValue`
	- output: console.log
	- input

### Question

- What are the three stages in the problem solving process?
	- Understanding the problem
	- Planning the solution
	- Divide and Conquer
- Why is it important to clearly understand the problem first?
	- If you don't understand it well then you won't know when you have solved it. and you may work towards a wrong solution
- What can you do to help get a clearer understanding of the problem?
	- write down the problem again in plain english and even explain the problem to someone else in plain english
- What are some of the things you should do in the planning stage of the problem solving process?
	- You should ask yourself the following questions:
		- Does it have a ui? If yes, what does it look like? Draw it on paper. And what functionality does it have?
		- Input: what is the input? how does it get the input? does the user provide or does it get it from somewhere else?
		- Desired Output: what is the desired output
		- What are the steps that you need to take to go from inputs to desired out?
			- Write these steps in plain english
			- This is the pseudocode: sub problems that you need to solve to solve the bigger problem
- What is an algorithm?
	- this are the series of steps that you need to take solve the problem using the inputs and producing the desired output
	- This is kind of like the recipe for solving the bigger problem
- What is pseudocode?
	- series of steps written in plain english using programming constructs
- What are the advantages of breaking a problem down and solving the smaller problems?
	- because one may not know how to solve the big problem in one go but one may know a smaller problem on a smaller scale. solving one problem may reveal more information like next steps, more data etc.

### Understanding Errors
- error is a kind of object built into JS consisting of a name/type and a message
- ReferenceError is thrown when one refers to a variable that is not yet defined or initialized in the current scope
- stack trace: lets you trace the evolution of the error back to its origin
- Syntax Errors
	- code is not written correctly i.e. not in accordance with the grammatical rules of JS
- Type Error
	- consider the data type of the operand or argument to which you are applying the operator or method or function to
	- Mostly likely, it might not be what you thought it was or the operations or method might not be compatible there
- Errors vs warning
	- errors will stop the program or whatever process you are attempting to run
	- warnings are messages that provide you insight on potential problems that may not necessarily crash your program in runtime or at all
- syntax errors vs logic errors
	- syntax errors are spelling or grammatical errors in code which may prevent your program from running at all or stop your program part way through. You will get a message on what the issue is and where it is. 
	- Logic errors are issues in the logic of the program such that the program doesn't do what you intended to do. This program runs without any errors. 

### Questions
- What are three reasons why you may see a TypeError?
	- when you are attempting to modify a value that cannot be changed
	- when you are using a value in an inappropriate way
	- when you are using the method/function/operator to an argument/operand to which they are incompatible with
- What is the key difference between an error and a warning?
	- Errors are issues that stop your program from running or do a different thing than you intended it to
	- warnings are messages give you an insight on potential issue that may not necessarily stop your program in runtime or at all
- What is one method you can use to resolve an error?
	- reading the messages and see what and where the error is occuring
	- we can use debugging tools or console.log()

### Clean Code
- Single letter variables can be used in loops and callback functions but avoid them elsewhere
- Variable names should start with a noun or an adjective and function with a verb
	- isSelected is bad variable name
- when the programmer is absolutely sure that the variable is truly constant, then we can use THIS_NOTATION
- break line immediately after operator or comma
- good comments explain the reason behind the code: why it works instead of how it works
- write your code as if your comments didn't exist: This will force you to write code in self-documenting way. Don't rely them as a crutch. Only at the point when the code cannot be made easier then you should resort to comments. 
- Refactor, Rewrite your code until it doesn't need comments any more
- Write code to be consumed by other programmers and by the computers second
- Sometimes fewer comments make the code more readable: by using meaningful symbol names
- Code tells you how, comments tells you why

### Questions
- Why is it important to write clean code?
	- For yourself, when you come back to it
	- For your fellow developers, as most of the software is developed by building on already written code. So, SWD spend most of their time reading code written by others or themselves
	- Easier to maintain
- Name 5 clean code principles previously mentioned
	- Names: 
		- Variable names should start with noun or adjectives and function names should start with verbs. 
		- Use a consistent vocabulary (user or customer)
		- Descriptive variable names and function names
	- Indentation: Spaces or tabs. consistency is the key
	- Line length of 80
	- Comments: 
		- explain why not how
	- Semicolons
 - What is the difference between good comments and bad comments?
	 - Bad comments explain how the code is doing what the code is doing. Good comments explain the why
	 - Bad comments are there as a crutch to compensate the badly written code
	 - Good code doesn't require comments at all to explain what is happening. 

### Node.js
- js runtime environment that allow you to run js code outside of the browser
- nvm: node version manager. it makes easy to change node version and upgrade node.
- npm: node package manager. that you will later use to install various libraries and tools used in js environments. 
- lts version: long term support version of node
- to open: node
- to exit: .exit

### Arrays and Loops
- arrays: data structures that can store multiple values in a single variable
- loops are control structures which allow you to execute a block of code repeatedly
- TDD: test driven development (practice for writing tests before writing the code itself)
- array: 
	- ordered collection of items
	- using array literal to create an array: const arr = [a, b, c]
	- common to use const for arrays
	- declare first and then add values (to const only)
	- no need to use the new Array(). instead use array literal
	- typeof is object but they are best described as arrays
		- objects use names to access values, arrays use numbers
		- objects are dictionaries in python
	- arrays are special kind of objects. There can be objects, function, arrays in arrays. 
	- associative arrays: named indices (hashes). JS does not support this. If you use named indexes, JS will redefine the array into object and some properties and methods will not work as expected
		- use arrays when you want element names to be numbers
		- use arrays when you want element names to be strings
	- built-in constructor: new Array()
		- new Array(10) - create an empty array with 10 elements
		- [10] - create a array with one element
	- how to know if an object is array
		- Array.isArray(test)
		- test instanceof Array
	- .at() method and [ ]
		- many languages support use of -1 to access the last element
		- JS can't do that since objects and arrays both use [] notation. -1 would mean a key called -1. 
		- .at() solves this problem
	- .join vs .toString()
		- .join can specify the separator
	- .pop
		- removes the last element from the array and returns it
	- .push method
		- adds a new element to the array and returns the length
	- shift is same as pop but it removes and returns first element
	- unshift is opposite of push
	- using length to append elements
	- delete()
		- leaves undefined holes. use pop and shift instead
	- concat creates a new array. does not alter.
		- can take any number of arrays
	- copyWithin
		- overwrites, does not increase length
	- flattening an array
		- reducing its dimensionality. convert multi-dimensional array to one dimensional array
		- .flat() doesn't update. returns a new array
	- splice(position, how many to remove, items to be added comma separated)
		- returns what was removed
		- returns length 0 if nothing is removed
	- toSpliced() doesn't alter the original array
	- slice creates a new array. doesn't alter the existing array. 
	- js automatically converts an array into string when a primitive type is expected
- Loops
	- for of construct
	- filter - return array after applying function to each element and filtering based on which returns true
	- map - return array after applying the function to each element
		- both filter and map are most often used with function expressions - anonymous functions or arrow functions
	- running a code like 100 times - for loop
		- for (intializer; condition; final-expression)
			- initializer - variable set to a number which is incremented to count the number of times a loop is run. counter variable
			- condition: expression using comparison operator to check when the loop should stop looping
			- increment or decrement to bring the initialized variable closer to the condition. run once the loop has gone through a full iteration
		- we have to use let for counter variable as we are reassigning it each iteration
	- best to loop over a collection using for...of loop
	- break: break out of the loop
	- continue: skips to next iteration of the loop
	- while 
		- initilizer
		- while(condition) {
		- // code
		- final expression
		- }
	- and do...while
		- initializer
		- do {
		- // code
		- final expression
		- } while ()
	- do...while will run at least once
		- in while and for loop, the check comes first so we might never run them based on the conditon
	- infinite loop if the while loop doesn't increment or decrement the counter
	- a single execution of the loop is called iteration
	- any expression or variable can be a loop condition, not just comparisons: the condition is evaluated and converted to boolean by while
	- inline variable declaration: in for loop
		- the variable is visible only inside the loop
	- the combination of infinite loop + break is great for situations where a loop's condition needs to be checked not in the beginning or end of the loop but in the middle or several places of its body
	- continue decreases the level of nesting
	- syntax constructs that are not expressions cannot be used to the right side of ?
		- no break or continue to be used with ? operator
		- another reason to not use ternary operator in place of if else construct
	- label (an identifier with a colon before the loop.)
		- to break or continue from any level of the loop not just the inner most one
	- break and continue are mostly used inside the loops. and labels do not allow us to jump to arbitrary places
		- a way to break or continue in the nested loops
- Test Driven Development (TDD)

### Questions
- What is an array?
	- array is a ordered collection of items or a list of items. items can be of same or different types
- What are arrays useful for?
	- for storing a variety of information about an entity or one kind of information for various entities without creating large number of variables
- How do you access an array element?
	- array[index starting from 0 upto length of array-1]
	- array.at(index starting from 0 upto length of array - 1 or negative indices which start from end)
- How do you change an array element?
	- array[index] = new value
- What are some useful array properties?
	- array.length
	- 
- What are some useful array methods?
	- array.includes()
	- array.at()
	- array.filter()
	- array.map()
	- array.forEach()
- What are loops useful for?
	- loops are useful for iterating over an iterable object
	- for repeating an action n number of times
	- for repeating an action until a condition is being met
	- for running an infinite loop
- What is the break statement?
	- break out of a loop block usually an infinite loop when a condition is met
- What is the continue statement?
	- continue to next iteration of loop once a condition is met
- What is the advantage of writing automated tests?
	- so you need not to run your function multiple times manually once you finish writing it

### DOM Manipulation and Events

- DOM
	- tree like representation of the webpage - tree of nodes with different relationship depending upon how they are arranged in the html document
		- parent, child, sibling
	- targeting nodes with selectors
		- when working with the dom, you use selectors to target the node you want to work with - combination of css style selector and relationship properties (identify the node based on its relationship to the nodes around it)
- DOM Methods
	- when you html code is parsed by the browser, this is converted to DOM (tree of nodes). These nodes are objects with many methods and properties attached to them
		- these properties and methods are the primary tools we are going to use to manipulate our page.
	- query selector
		- element.querySelector(selector) - returns a reference to first match of selector
		- element.querySelectorAll(selectors) - returns a nodelist containing all the matches  of the selectors
- textContent over innerHTML
- JS changes what the browser renders and not the html
- script tag in head of html file to load js once html is parsed or DOM nodes are created
- Events are actions that occur on our webpages and using JS we can make our web page listen to these events and react to these events
- 3 ways to do that
	- inside html eg. onclick attribute
		- not ideal as we are cluttering our html with js
		- one onclick attribute per dom, so we are unable to run multiple separate functions in response to a click using this method
	- move the js out of the html but other problem remains
	- multiple event listeners if the need arises
- DOM: 
	- API to manipulate html documents. DOM represents html document as a tree of nodes.
	- in the dom tree, the document is the root node. one child, html element. it is called the document element. each document can have only one document element. 
		- each markup is represented by a node in a tree
		- node is identified by node type.
			-  node.nodeType
		- nodeName and nodeValue - specific info about the node. it depends upon nodeType
	- node and element: 
		- generic name for any object in the DOM tree
			- built-in DOM element like the document or html tag
		- an element is a specific node of node.ELEMENT_NODE type
		- getElementById and querySelector returns an object with Element type while getElementsByTagName and querySelectorAll returns nodelist which is a collection of nodes
	- each markup can be represented as a node with a specific node type
	- in a dom tree, node has relationship with other nodes like a family tree
	- getElementById() to select an element with a specific id
		- document.getElementById() returns an element object that represents an html element with the matched id
		- it is only available on the document object and not on other elements
	- getElementsByName()
		- name attribute. multiple elements can share value and name attribute unlike id attribute
		- document.getElementsByName
		- returns a nodeList of elements, return collection is live. That is this collection is automatically updated when  elements are added with the same name or removed.
	- getElementsByTagName()
		- method of document object or specific DOM element
		- takes the tag, returns an html collection of matching tag names in the order in which they appear in the document
			- live collection
	- querySelectorAll 
		- returns a static nodelist
		- Array.from to convert nodelist to array
		- methods forEach and constructs like for of are valid on nodelist
- JS Events
	- event handler - function
	- register an event handler using addEventListener function
	- Event flow explains the order in which event is received on the page from the element where the event occurs and how it propagates through the DOM tree
	- 2 main event models: event bubbling and event capturing
	- Event Bubbling
		- event flows upwards through the DOM from most specific element to least specific element
		- modern web browsers bubble to event upto window object
	- Event Capturing
		- event flows downwards through the DOM from least specific element to the most specific element
	- DOM Level 2 Event Flow
		- event flow has 3 phases
			- event capturing occurs, which provides an opportunity to intercept the event
			- actual target receives the event
			- event bubbling occurs, which provides final response to the event
	- Event Object
		- when the event occurs, the browser passes event object to the event handler
		- this is only accessible inside event handler
	- .preventDefault() to prevent the default behavior of an event but does not stop the event flow
	- if there are multiple event handlers, all the event handlers will be executed when the event is fired
	- load event for images
	- 3 ways to register an event handler
		- use .addEventListener event handler
		- assign event handler to onclick property of the element
		- assign event handler to element attribute in html (this is mostly done in legacy systems)
	- Mouse events
		- event object has button property to indicate which button was pressed
	- Scroll events on the window object to handle the scroll of the whole page
	- Event delegation
		- large no of event handlers impact the performance of the page
			- event handlers are functions which is also an object and which takes up memory. The more objects in the memory, slower the performance.
			- it takes time to assign event handlers, which causes delay in interactivity of the page.
		- it refers to the technique of using event bubbling to handle events at a higher level in the DOM than the element at which they are originated at
	- Generate Events from Code (programatically)
	- Custom Events: Instead of using callbacks, we can use custom events and then use those to trigger a function
	- Mutation Observer to watch for the changes made to the DOM API
- Digital Ocean
	- All the items in the DOM are defined as nodes
	- mostly work with: element nodes, text nodes, comment nodes
	- when an html element is an item in the DOM, it is referred to as Element Node, any lone text outside of the element is the text node, and comments are comment node
	- nodeType property
	- nodeValue and nodeName - tag name
	- document object is the root of every node in the DOM
		- this is actually a property of the top level window object which represents the tab in the browser
		- it has access to information such as toolbar, height and width of the window
		- the document consists of what is inside the inner window'
		- even a blank html will have these 3 nodes added and parsed into the DOM
			- document - # document
			- document.documentElement = html
			- document.head
			- document.body
		- parent
			- parentNode or parentElement
			- parent of almost any node is usually an element node as text/comments cannot be parents of other nodes. however parent of html is a document node, so parentElement returns null
			- parentNode is used more when traversing the DOM
		- Children
			- one level below
			- more than one: descendants 
			- childNodes  - live list, nodelist
				- indentation in html is considered as text nodes
				- this is not mentioned in the elements panel
			- even firstChild gives the first text node
			- so we resort to children, firstElementChild, lastElementChild - which only consider element nodes
			- eg: p element that has text and strong tag
				- p.childNodes gives text, strong, text
				- p.children only gives strong
			- eg: ul has li and there is indentation as well
				- p.childNodes gives indentation as text as well as li
				- p.children here is more suitable
		- Siblings
	- create nodes
		- createElement and createTextNode
	- inserting nodes into the DOM
		- appendChild, insertBefore, replaceChild methods
	- remove child node - removeChild()
	- remove the node itself - remove()
	- getElementsByTagName and getElementsByClassName are html collections and do not have methods like .forEach. You can use for loop to loop through these collections
	- properties and methods that are used to modify the attributes of the elements
	- Custom attributes that are not part of the html standard are to be prepended with data- or aria-
	- the styles property represents the inline styles on an element
	- setting style using setAttribute will remove the existing styles. To avoid this, we can update value of the style property
	- Event Handlers and Event Listeners
		- Event handlers is JS function that runs when an event is fired
		- Event Listener attaches an responsive interface to an element, which allows that particular element to wait and listen for the event to fire
	- 3 ways to assign events to elements
		- inline event handlers
		- event handler property
			- we only pass the function as a reference since we are not invoking the function
			- multiple onclick properties can't be set. 
		- event listener
			- it watches for an event on an element
			- method on the element which watches for an event on that element
			- we can set multiple event listeners on the same event
			- removeEventListener
	- Event Objects
		- event object consists of properties and methods that all events can access. In addition to the generic event object, each type of event has its own extension to the event object, MouseEvent, KeyboardEvent
		- Event object is passed through a listener function as a parameter
	- event.target: use one event listener and get the most deeply rooted element 
- MDN Events
	- Events are things that happen in the system in which you are programming, which the system tells you about so your code can react to them
	- to react to an event, you attach a event handler to it - block of code( that you as a programmer create) that runs when the event fires. When such a block of code is defined to run in response to an event, we say that we are registering an event handler. Event handlers are sometimes called event listeners. but they work together
		- listener watch out for the event and handler is the code that runs in response to it. 
	- Web events are not part of the core JS language. They are part of the APIs built into the browser. 
	- objects that can fire events have a addEventListener method
	- objects that can fire events have a property with on prefix like onclick. This is called event handler property.
		- to listen to the event, you can assign the handler function to the property.
		- handler function - named or anonymous
			- reference to the named function
	- we can't handle more than 1 event with event handler property as the last one will overwrite the property with the latest event handler function
	- Inline event handlers - never use these
		- call function defined in the script within html or just write js in html as attribute value
	- Event Objects
		- it is automatically passed to event handlers to provide extra information and features
		- target property of the event object is always a reference to the element where the event occurred
		- can be called anything, e, evt, event are most commonly used
		- specialized
			- keydown event fires when a key is pressed
			- its event object called KeyboardEvent has a key property which tells which key you pressed
	- Preventing default behavior
		- Eg: prevent form submission in case the user has not submitted the data correctly
			- submit event is fired on form element when the form is submitted
	- Event Bubbling
		- event bubbling describes how the browser handles events targeted at nested elements
		- events bubble up from the innermost element that was clicked
		- event object has a method on it called stopPropagation() which when called inside a event handler prevents the event from bubbling up to any other elements
	- an alternative form event propagation is called event capture
		- this is like event bubbling but the order is reversed
		- so instead of event firing on the innermost element targeted then successively on the less nested element, the event fires on the least nested element and successively on the more nested elements until the target is reached
		- event capture is disabled by default, To enable it you need to pass in an option to addEventListener
	- by default, almost all event handlers are registering in the bubbling phase
	- Event bubbling allows event delegation
		- when we want some code to run when the user interacts with any of the child elements, we set the event listener on the parent and have the events that happen on them bubble upto their parent rather than having to set eventListener on every child individually
		- target - innermost element
		- currentTarget - element which handled the event
	- Events are not unique to JS
	- Most programming languages have event model and the way the event model works differs from JS way

### Questions

- What is the DOM?
	- DOM is the document object model. In essence, it is a programming interface. Browser parses the html into a document object model (sort of like a tree with each element as node). Each part of the page starting from the document is an object and each object has methods and properties which allows JS to create, update, remove elements as well as introduce interactivity to web pages
- How do you target the nodes you want to work with?
	- using document object or any particular element object
	- There are methods available in each object such as querySelector, getElementById, getElementsByTagName, getElementsByClassName
	- using these methods we can target specific or list of nodes
- How do you create an element in the DOM?
	- document.createElement(type of element)
- How do you add an element to the DOM?
	- elementObject.appendChild()
	- or insertBefore
	- or replaceChild
- How do you remove an element from the DOM?
	- elementObject.removeChild()
	- or replaceChild()
	- elementObject.remove()
- How can you alter an element in the DOM?
	- you can add attributes using setAttribute
	- you can alter properties of element object
	- you can add classes classList.add remove toggle 
- When adding text to a DOM element, should you use textContent or innerHTML? Why?
	- you should use textContent
	- innerHTML has security issues
- Where should you include your JavaScript tag in your HTML file when working with DOM nodes?
	- at the end of the html as last element so that browser creates the DOM tree once it gets to js
- How do “events” and “listeners” work?
	- events are fired for things that occur in the browser or based on the user action
	- listener watch out for these events and then do something in response 
- What are three ways to use events in your code?
	- using event listener method
	- using event handler property like eventobject.onclick
	- using inline event handlers
- Why are event listeners the preferred way to handle events?
	- keep js and html separate
	- can add multiple event handlers to an event
- What are the benefits of using named functions in your listeners?
	- can utilize them in multiple places 
	- easier to remove
- How do you attach listeners to groups of nodes?
	- attach them to their parent
	- then the events that occur in the group of nodes, it bubbles up to their parent
	- or use querySelectorAll and then use forEach
- What is the difference between the return values of querySelector and querySelectorAll?
	- returns the first element that matches
	- returns the live list of node list (forEach supported)
- What does a “nodelist” contain?
	- list of nodes
	- slightly different from array
	- reference to all matches of selectors
- Explain the difference between “capture” and “bubbling”.
	- when event propagates from innermost element to the outermost - bubbling
	- when the event propagates from outermost element to the innermost element

### UI to Rock Paper Scissor
- Git Branching
	- Branches in git allow you to hold alternate reality versions of your files at the same time
	- default branch (main): branch that is created when you make your first commit to the project
	- like the branches in a tree, all the branches stem off from the trunk (main) or off other branches
	- when you make commits on a branch, those changes only exist on that branch, leaving all of other branches as they were when you branched off of them
	- main branch = finished features that you know are working properly and add each feature to your project using dedicated branches - feature branch
	- create - git branch branchname 
	- change - git checkout branchname
	- do both of above together - git checkout -b branchname
	- see all branches - git branch
	- current branch - * 
	- git checkout main to change to main branch
	- merge
		- git merge branchname
			- take the changes you have committed on branchname and add them to the branch you are currently on
		- same lines being changed by different branches = merge conflict
	- delete 
		- git branch -d branchname if the branch has been merged into main
		- git branch -D branchname if the branch has not been merged into main
	- Sharing code: sharing code with other that you might not want to commit to your main branch or feature branch

### Object Basics
- objects: collection of key value pairs
- 8 data types: 7 are called primitive data type because their value contain a single thing
- created with {...} with an optional list of properties. property : key-value pair where key is a string (property name) and value can be anything
- object literal syntax: newOb = { }
- object constructor syntax: new Object()
- dot notation to access values or add k-v pair and square bracket notation
	- square bracket allows expressions: this allows keys to be calculate at run time or can be user inputted
- trailing coma: it makes easy adding, moving k-v pairs around
- Computed properties
	- in the object literal, the property name should be taken from the notation [fruit]
- property value shorthand
- There are no limitations for property names. Like variable names cannot be equal to language reserved words (for, let, const, return). They can be strings or symbols. Other types are automatically converted to strings
- possible to test any property. there will be no error if it doesn't exist. Reading a non-existent property just returns undefined.
	- "key" in object
	- why does this operator exist? to account for the special case when the property stores undefined
	- this does happen rarely as undefined is rarely used. we use null for empty values
- for...in loop
	- to walk over all the keys in the object
- objects are ordered in a special fashion
	- integer properties are sorted, others appear in creation order
		- integer properties: string that can be converted to and from an integer without a change (that is it stays the same)
- MDN
	- objects: collection of related data and functionality. properties and methods when they are inside the object.
	- for methods instead of method: function(){}, we can write method(){}
	- object literal, obj = {...} vs object instantiated from class
	- an object property can itself be an object
	- objects are sometimes called associative arrays
	- using bracket notation, we can use variables to create new members
	- this keyword
		- current object the code is being written inside of
		- same method definition for every object you create
	- constructor
		- using object literal is fine when you need to create one object but when you need to create more than 1, they are inadequate
			- write same code again
			- and we want to update one property, then we need update it every object
		- way to define the shape of an object - the set of properties and methods it can have, and then create as many objects as we like, just updating the properties that are different.
			- using function (declare empty object, initialise it, return it)
			- constructor is better - function called with a new keyword
		- definition is like function with this keyword but for creating an instance of that object, we will use new
- Fancy array functions
	- map
		- it expects callback as an argument, which is a fancy way to say pass another function as an argument to my function
		- apply the passed function to each item of array and returns a new array. it doesn't modify the original array
	- filter
		- apply the callback function to each item of the array and returns the original item only the callback returns true
		- callback must return true or false
	- reduce
		- array.reduce((accumulator, currentItem) => return, initialAccumulator (specific or first item of array))
		- array.reduce(callback, initialValueOfAccumulator)
		- apply the callback to each element of array and return accumulator
	- Filter > Map > Reduce (Think of it like for making a sandwich, filtering ingredients, transforming ingredients, reducing them to one thing)
	- sort
		- this take two values a and b. run a function over these 2. if the function returns 1 then a is moved after b. if it returns 0, they are kept as it is. if -1 then a is moved before b
	- slice: to cut and copy, to copy the original array
	- splice: to add, remove, replace
	- includes vs indexOf
		- includes handles NaN correctly
	- sort
		- the items are sorted as strings by default


### Questions

- What is the difference between objects and arrays?
	- arrays are a form of an object with some special features such as they have integers as properties and have special methods
- How do you access object properties?
	- object.property
	- object [ property ]
- What is Array.prototype.map() useful for?
	- to create a new array by looping over an existing one and mapping the items of the array into something else
- What is Array.prototype.filter() useful for?
	- to filter the items of an array by looping over an array and checking for a condition. If the conditions turns out to be true then that item is included in the array
- What is Array.prototype.reduce() useful for?
	- it is used to loop over an array and reduce the items of the array to a single value



