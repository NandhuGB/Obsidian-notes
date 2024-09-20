
#### Multiple CSS class selectors 

	if `anchor <a>` tag has two classes `highlight` and `main-anchor` appling same styles for say, then declaration of that classes on `.css` document decides its specificity. IN following example: Color:white will be applied

```html
<a class="main-anchor highlight"> some content</a>
```
```css
.main-anchor{
color:black;
}
.highlight{
color:white;
}
```

	 if you want to avoid this, you can use more specific selector

```css
a.main-anchor{
color:black;
}
.highlight{
color:white;
}
```

	 in above example, color:black will be applied, despite it declared before `highlight`. because `a.main-anchor` as more specificity than `.highlight` selector

#### ID vs Class selectors







#### !Important

`!important` gives that high specificity --> this style will be applied no more what

```css
.main-anchor{
color:black !important;
}
.highlight{
color:white;
}
```

because of `!important`  `main-anchor`-->`color` style will be applied