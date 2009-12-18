<h3>Description</h3>
Computed Style uses the browsers native functions to grab CSS applied to a certain element (which you specify) and compares it against a identical element in the same hierarchy - This way you can work out what CSS that is applied to an element compared to another.

Consider this: we want to get all CSS properties for body > div#test1 that is NOT applied on body > div -- this is the default behaviour of jquery.computedstyle (read more under"Usage").

Note: It will contain browser-applied CSS, values that are changed automatically by the browser to the element. This is because it'll change indirectly when changing font-size etc., this is not really an issue since you apply something that the browser are already planning on doing anyway.

<h3>Usage</h3>
	// Returns a object with CSS properties unique to this element
	// compared to another DIV-element in the same hierarchy
	$('div#id-of-element').getCSS()

	// Returns CSS properties unique for #id-of-element compared
	// to #id-of-another-element
	$('div#id-of-element').getCSS('div#id-of-another-element')

	//Works just like above, but you pass in a (DOM) element for
	// comparison instead
	$('div#id-of-element').getCSS(myElement)
