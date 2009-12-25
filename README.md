Tabs - A Simple Tab Swapper
===========================

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

- tabs - (*string*: defauls to '.tabs_title li')
- panels - (*string*: default to '.tabs_panel')
- selectedClass - (*string*: defaults to 'active')
- elementSwapOptions - (*object*) ElementSwap options object, see [ElementSwap][] for available options. (Defaults to: 
	selectedClass: 'active',
	panelWrap: 'tabsPanelWrap',
	panelWrapClass: 'tabs_panelwrap',
	activateOnLoad: 0,
	events: true,
	autoPlay: false
	)
- mouseOverClass - (*string*: defaults to 'over')

### Events

- onActive - (*function*)
- onBackground - (*function*)


[$$]: http://www.mootools.net/docs/core/Element/Element#dollars
[ElementSwap]: http://www.mootools.net/forge/p/elementswap