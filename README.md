bootstrap3-less-mixins
======================

Bootstrap 3 LESS Mixins, misc and responsive utilities

### Responsive shortcuts

```less
.responsive-min(@size, @rules)
.responsive-max(@size, @rules)
.responsive-range(@start, @end, @rules)

.phone-[min|max|only](@rules)
.tablet-[min|max|only](@rules)
.desktop-[min|max|only](@rules)
.lg-desktop-[min|max|only](@rules)
```

### Usage

*Ex: 
```css
body { 
	font-size: 10px;
	/* Set a larger font sizing for tablet screen size and more */
	.tablet-min({
		font-size: 14px;
	})
	
	/* Set a red background for 400px screen size and less */
	.responsive-max(400px, {
		background: red;
	})
}
```

*Ex:
```css
body { 
	/* Hide .nav-desktop elements for phone screen size only */
	.nav-desktop {
		.phone-only({
			display: none;
		})
	}
	
	/* Hide .nav-phone elements for desktop screen size only */
	.nav-phone {
		.desktop-only({
			display: none;
		})
	}	
}
```
