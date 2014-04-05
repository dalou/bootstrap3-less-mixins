bootstrap3-less-mixins
======================

Bootstrap 3 LESS Mixins, misc and responsive utilities

### Usage

*Ex: 
```css
body { 
	font-size: 10px;
	.tablet-min({
		font-size: 14px;
	})
}
```

or
```css
body { 
	font-size: 14px;
	.phone-min({
		font-size: 10px;
	})
}
```
*Ex:
```css
body { 
	.nav-phone {
		.phone-only({
			display: none;
		})
	}
	.nav-desktop {
		.desktop-only({
			display: none;
		})
	}	
}
```
