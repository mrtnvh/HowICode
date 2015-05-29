# HTML

## Table of contents
1. [Format](html-format)
2. [Attribute order](html-attrs)
3. [Naming](html-naming)
4. [Practical example](html-example)


<a name="html-format"></a>
## 1. Format

* Always use lowercase tag and attribute names.
* Write one discrete, block-level element per line.
* Use one additional level of indentation for each nested block-level element.
* Use valueless boolean attributes (e.g. `checked` rather than `checked="checked"`).
* Always use double quotes to quote attribute values.
* Omit the `type` attributes from `link` stylesheet, `style` and `script` elements.
* Always include closing tags.

(Keep line-length to a sensible maximum, e.g., 80 columns.)

Example:

```html
<div class="Tweet">
	<a href="{{url}}">
		<img src="{{avatar}}" alt="">
	</a>
	<p>{{text}}</p>
	<button disabled>Reply</button>
</div>
```

#### Exceptions and slight deviations

Elements with multiple attributes can have attributes arranged across multiple
lines in an effort to improve readability and produce more useful diffs.

Example:

```html
<a class="{{class}}"
	data-action="{{action}}"
	data-id="{{id}}"
	href="{{url}}"
>
	<span>{{text}}</span>
</a>
```


<a name="html-attrs"></a>
## 2. HTML attribute order

HTML attributes should be listed in alphabetical order.

Example:

```html
<a class="{{class}}" data-name="{{name}}" href="{{url}}" id="{{id}}">{{text}}</a>
```


<a name="html-naming"></a>
## 3. Naming

Naming is hard, but very important. It's a crucial part of the process of
developing a maintainable code base. Don't be afraid to rename components.

* Use clear, thoughtful, and appropriate names for HTML classes. The names should be informative both within HTML and CSS files.
* Avoid _systematic_ use of abbreviated class names. Don't make things difficult to understand.

Example with "bad" names:

```html
<div class="cb s-scr"></div>
```

```css
.cb {
	background: #000;
}

.cb.s-scr {
	overflow: auto;
}
```

Example with better names:

```html
<div class="ColumnBody is-scrollable"></div>
```

```css
.ColumnBody {
	background: #000;
}

.ColumnBody.is-scrollable {
	overflow: auto;
}
```


<a name="html-example"></a>
## 4. HTML practical example

An example of various conventions.

```html
<!DOCTYPE html>
<html>
	<head>
		<meta charset="utf-8">
		<title>Document</title>
		<link rel="stylesheet" href="main.css">
		<script src="main.js"></script>
	</head>
	<body>
		<article class="Post" id="1234">
			<time class="Post-timestamp">{{date}}</time>
			<a data-analytics-action="{{action}}"
			 data-analytics-category="{{category}}"
			 data-id="1234"
			 href="{{url}}">{{text}}</a>
			<ul>
				<li>
					<a href="{{url}}">{{text}}</a>
					<img src="{{src}}" alt="">
				</li>
				<li>
					<a href="{{url}}">{{text}}</a>
				</li>
			</ul>

			<a class="u-linkComplex" href="{{url}}">
				<span class="u-linkComplex-target">{{text}}</span>
				{{text}}
			</a>

			<input value="text" readonly>
		</article>
	</body>
</html>
```
