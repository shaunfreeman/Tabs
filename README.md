Tabs - A Simple Tab Swapper
===========================

Tabs is a very simple yet powerful as all the styling for the tabbed box is done via CSS and completly comtrolled by you. It is part of my MooTools library so you will need to use [ElementSwap][] for it to work.

![Screenshot](http://github.com/vincentbluff/Tabs/raw/master/screenshot.png)

Requirements
------------

* [MooTools Core 1.2.4](http://mootools.net/core): Class, Class.Extras, Element, Selectors and their dependencies
* [ElementSwap][] and its dependencies

How to use
----------

### Syntax
	#JS
	var myTabs = new Tabs([options]);

### Arguments

1. options - (*object*, optional) An object with options. See below.

### Options

- tabs - (*mixed*: defauls to '.tabs_title li') (*array*), a collection of DOM elements for the tabs; can also be a [$$][] selector (*string*).
- panels - (*mixed*: default to '.tabs_panel') (*array*), a collection of DOM elements for the panels; can also be a [$$][] selector (*string*).
- selectedClass - (*string*: defaults to 'active') the CSS class name you want to use when a tab is selected.
- elementSwapOptions - (*object*) ElementSwap options object, see [ElementSwap][] for available options. (Defaults to: {
	selectedClass: 'active',
	panelWrap: 'tabsPanelWrap',
	panelWrapClass: 'tabs_panelwrap',
	activateOnLoad: 0,
	events: true,
	autoPlay: false
	})
- mouseOverClass - (*string*: defaults to 'over') the CSS class name you want to use when a tab is mousedover

### Events

- onActive - (*function*) callback executed when a tab is shown, passed two arguments: the index of the tab (*integer*), the tab (*element*)
- onBackground - (*function*) callback executed when a tab is hidden, passed one argument: the tab (*element*)

### Example

### JavaScript

	#JS
	var myTabs = new Tabs();

### CSS

	#CSS
	#tabs {
		position:relative;
		width:300px;
		height:200px;
		overflow:hidden;
	}
	
	.tabs_title {
		list-style-image: none;
		list-style-type: none;
		margin: 0px;
		padding: 0px;
		height: 24px;
	}
	
	.tabs_title li {
		float: left;
		background-color: #3975BD;
		padding: 2px 8px 2px 8px;
		margin-right: 2px;
		cursor: pointer;
		color: #fff;
		font-family: "Trebuchet MS";
		font-size: 12px;
		height: 24px;
		line-height: 24px;
	}
	
	.tabs_title a {
		text-decoration:none;
		color: #fff;
	}
	
	.tabs_title li.over {
		font-weight: bold;
	}
	
	.tabs_title li.active {
		background-color: #49A8EC;
	}
	
	.tabs_panelwrap {
		position: absolute;
		top:28px;
		overflow: hidden;
		width:300px;
		height:172px;
	}
	
	.tabs_panel {
		/*position:absolute;
		top:28px;*/
		width:300px;
		height:172px;
		display:none;
		overflow: auto;
		background-color: #49A8EC;
		color: #fff;
		clear: both;
	}
	
	.tabs_panel.active {
		display: block;
	}
	
	.tabs_panel p {
		margin-left:5px;
	}

#HTML

	#HTML
	<div id="tabs">

		<!-- tab headings -->

		<ul class="tabs_title">
			<li title="my_work">My Work</li>
			<li title="about_me">About Me</li>

			<li title="contact">Contact</li>
		</ul>

			
		<!-- Tab1 content -->

		<div id="my_work" class="tabs_panel">
			<h1>Tab 1</h1>
			<p>content</p>
		</div>

		<!-- Tab2 content -->

		<div id="about_me" class="tabs_panel">
			<h1>Tab 2</h1>
			<p>content</p>
		</div>
			
		<!-- Tab3 content -->

		<div id="contact" class="tabs_panel">
			<h1>Tab 3</h1>
			<p>content</p>
		</div>
	
	</div>


[$$]: http://www.mootools.net/docs/core/Element/Element#dollars
[ElementSwap]: http://www.mootools.net/forge/p/elementswap