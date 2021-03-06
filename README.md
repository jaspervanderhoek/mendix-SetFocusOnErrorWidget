mendix-SetFocusOnErrorWidget
==============================

Set the focus on the input widget that has an error.

Mendix does not position the screen to show validation errors. Especially with larger pages this becomes frustrating because the user thinks the applications hangs. Actually, there is an error message on a part of the page that is outside the currently visible area of the page.
Of course the user would see the error when scrolling the page.

It is much more user friendly to reposition the page to the input element with the error.

This widget does that: it finds an input element with an error (usually the first) and sets the focus on it. The page is scrolled to make sure the widget is visible. If the widget is in a groupbox that is currently collapsed, the groupbox is expanded too. 

##Typical Usage Scenario
Large pages or pages with many input elements. When validation fails, it is immediately visible why because the input element with an error message is scrolled into view.

##Features And Limitations
Reposition the page to show validation errors. Expand groupboxes if necessary.

The input element must be in a table cell.

As of the first release, this widget does not work with tab containers. There is an issue with tab containers, ticket 204322. In some situations the error messages are shown in a popup unless the user actually visited the tabs. As soon as this issue is solved, the widget can be enhanced to show the tab which has validation error(s) on its input elements. 

##Installation
Normal installation using the App Store.

##Dependencies
Mendix 5 Environment. I tested with Mendix 5.9.1.
 
##Configuration
In the designer, place this widget in the topmost dataview of the page. 

##Properties
delay: For large pages, showing many validation errors can take a little time. As this widget can only act after the validation errors are shown, this property can be used to set a delay.
