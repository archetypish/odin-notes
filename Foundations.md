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