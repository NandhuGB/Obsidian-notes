cascading style sheet --> multiple styles or rules can be applied on single element but the selectors specificity determines the final style of any element

css 1 --> 1996
css 2 --> 1998
css 3 -->in development --> split up as modules

```css
body{
margin:0px;
}
```

### Adding CSS
	 3 ways to add css to html
	 
Inline style --> not recommended
```html
<section style="background-color:red;">
</section>
```

using style tag
```html
<head>
<style>
section{
background:#ff1b68
}
</style>
</head>
```

external style sheet --> style.css
```css
section{
background: #ff1b68;
}
```

need to add this file through link tag

```html
<link rel="stylesheet" href="style.css">
```

### CSS Rules



### Selectors, Properties, Values

#### Selectors --> 

	 class and id names should be kebab cases

universal selector -->selects every element in that page
```css
*{
margin:0;
}
```

element  selector
```css
h1{
color:red;
}
```

class selector
```html
<h1 class="class_name">Hello!</h1>
```
```css
.class__name{
background-color:red;
}
```

id selector
```html
<h1 id="main-tite">Title</h1>
```
```css
#main-title{
color:red;
}
```

Attribute selector
```html
<button disabled>CLick</button>
```
```css
[disabled]{
color:red;
}
```
### Conflicting Styles

	 amoung all the selectors some have more priority than others. if same element is styled with different type of selectors (class, id, tag, attribute, universal), the selector with high priority style gets applied to that element.

	 if same element is styled with same selector, the last declaration (on the document from top to bottom) style will be applied.

	High priority or specificity---> from high to low ---> 

1.  In-line selector
2. ID selector
3. class (.class) , pseudo class (:pseudo class) and attribute selector 
4. tag (<tag></tag>) and pseudo element ( :: pseudo element)

	some other concepts can affect this specificity like inheritance.

#### Inheritance

	 inheritance is the styles passed to the child elements from parent element

```html
<body>
<h1>red</h1>
<h4>red</h4>
</body>
```
```css
body{
color:red;
}
```

	h1 and h4 tag will be red if anyother styles affected them. this is because of inheritance. inheritance has lowest specificity or priority among selectors



#### Combining selectors (Combinators)

	 we can combine two selectors together
	example
```html
<section id="product">
<h1> Mouse</h1>
</section>
```
```css
#product h1{
color:red;
}
```


### Combinators

#### Adjacent sibling (+)

element after first one (directly)

#### General Sibling (~)

element come after first one not directly

#### Child (>)

direct child

#### Descendant ( )

inside that parent, can be grandchild


