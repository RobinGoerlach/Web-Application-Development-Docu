## CSS
```html
.dropdown a {
  display: none;
}
.dropdown:hover .dropdown-content a {
  display: block;
}
```


## HTML
```html
<div class="dropdown">
	<a href="#" Items</a>
	<div class="dropdown-content">
		<a href="#">Item 1</a>
		<a href="#">Item 2</a>
		<a href="#">Item 3</a>
	</div> <!-- dropdown-content -->
</div> <!-- dropdown -->		
```


Hiding unused components until clicked on top entry