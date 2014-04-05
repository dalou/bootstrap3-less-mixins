bootstrap3-less-mixins
======================

Bootstrap 3 LESS Mixins, misc and responsive utilities

### Commons shortcuts headers
```css
/* Combine absolute left top position */
.absolute-lt(@left, @top);
```
...

### Responsive shortcuts headers

```css
/* rules for a minimum screen size */
.responsive-min(@size, @rules);
/* rules for a maximum screen size */
.responsive-max(@size, @rules);
/* rules for a screen size range */
.responsive-range(@start, @end, @rules);

/* rules for phone screen size panel */
.phone-[min|max|only](@rules) ;
/* rules for phone screen size panel */
.tablet-[min|max|only](@rules);
/* rules for phone screen size panel */
.desktop-[min|max|only](@rules); 
/* rules for phone screen size panel */
.lg-desktop-[min|max|only](@rules);

/* rules for gradient phone, tablet, desktop, lg-desktop */
.device-gradient(@phone-rules, @tablet-rules, @desktop, @lg-desktop);
/* same as previous but exclusive rules (only like) */
.device-gradient-exclusive(@phone-rules, @tablet-rules, @desktop, @lg-desktop);
/* same as previous but max screen sizes rules (max like) */
.device-gradient-inverted(@phone-rules, @tablet-rules, @desktop, @lg-desktop); 
```

### Usage examples
 
```css
body { 
	/* Set a default font size */
	font-size: 10px;
	
	/* Set a larger font sizing for tablet screen size and more */
	.tablet-min({
		font-size: 14px;
	})
	
	/* Set a red background for 400px screen size and less */
	.responsive-max(400px, {
		background: red;
	})
 
	/* Hide .nav-desktop elements for phone screen size only */
	.nav-desktop {
		.phone-only({
			display: none;
		})
	}
	
	/* Hide .nav-phone elements for desktop screen size only */
	.nav-phone {
		.tablet-min({
			display: none;
		})
	}
	
	/* Set H1 bold from desktop screen size minimum and H2 bold from large desktop screen size minimum */
	.device-gradient(,,{
		h1 { font-weight: bold; }
	}, {
		h2 { font-weight: bold; }	
	})
}
```
