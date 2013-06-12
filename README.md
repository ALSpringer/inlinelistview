inlinelistview
==============
#A listview that has items that can be opened inline for jQuery Mobile
This plugin is licensed under GPLv3

##[DEMO](http://alspringer.github.io/)



##To use:

To illustrate usage, let's examine the difference between two listviews.

One with 4 menu items leading to different pages.
```HTML
<ul id="widgetlist" data-role="inlinelistview">
    <li><a href="#page2">Go to a new page</a></li>
    <li><a href="#inlineimg">Open Image Inline</a></li>
    <li><a href="#inlinetext">Open Text Inline</a></li>
    <li><a href="#page2">Go to a new page</a></li>
</ul>
```

And one with 4 menu items, two of which open inline on the same page.
```HTML
<ul id="widgetlist" data-role="inlinelistview">
    <li><a href="#page2">Go to a new page</a></li>
    <li data-rel="inline"><a href="#inlineimg">Open Image Inline</a></li>
    <li id="inlineimg"><div><img src="img/images.jpg"></div></li>
    <li data-rel="inline"><a href="#inlinetext">Open Text Inline</a></li>
    <li id="inlinetext"><div><p>I'm an arbitrary amount of text being shown inline!</p></div></li>
    <li><a href="#page2">Go to a new page</a></li>
</ul>
```

###What code is needed for this second example to open these two items inline?

####For the menu items
The menu items that are to be opened inline include a 'data-rel="inline"' attribute. 
This indicates to the plugin that these menu items will have a corresponding section that opens inline.
These menu items also have a "href=#linktoinlinesection" to indicate what the id of the section that will open inline is.

####For the items opening inline
The items that are opening inline are to be a <li> with the corresponding id to href indicated in the menu item.
Inside the <li> there should be a <div> wrapping the content that is to be shown.


###Lets tie it together
```HTML
<li data-rel="inline"><a href="#inlinetext">Open Text Inline</a></li>
<li id="inlinetext"><div><p>I'm an arbitrary amount of text being shown inline!</p></div></li>
```

