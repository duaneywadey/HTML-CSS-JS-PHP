
<h1 style="text-align: center"># HTML PART 1 TUTORIAL</h1>

## HTML BASIC TYPOGRAPHY

### Body, head, and title
```html
<html>
	<head>
		<title>This is the Title of the Page</title>
	</head>
	<body>
		<h1>This is the Body of the Page</h1>
		<p>Anything within the body of a web page is displayed in the main browser window.</p>
	</body>
</html>
```

### Headings
```html
<html>
	<body>
		<h1>This is the Main Heading</h1>
		<p>This text might be an introduction to the rest of the page. And if the page is a 
			 long one it might be split up into several sub-headings.<p>
		<h2>This is a Sub-Heading</h2>
		<p>Many long articles have sub-headings so to help you follow the structure of what 
			 is being written. There may even be sub-sub-headings (or lower-level headings).
			 </p>
		<h2>Another Sub-Heading</h2>
		<p>Here you can see another sub-heading.</p>
	</body>
</html>
```

### More headings
```html
<html>
	<head>
		<title>Headings</title>
	</head>
	<body>
		<h1>This is a Main Heading</h1>
		<h2>This is a Level 2 Heading</h2>
		<h3>This is a Level 3 Heading</h3>
		<h4>This is a Level 4 Heading</h4>
		<h5>This is a Level 5 Heading</h5>
		<h6>This is a Level 6 Heading</h6>
	</body>
</html>
```
### Making a word appear bold
```html
<html>
	<head>
		<title>Bold</title>
	</head>
	<body>
		<p>This is how we make a word appear <b>bold.</b></p>
		<p>Inside a product description you might see some <b>key features</b> in bold.</p>
	</body>
</html>
```

### Making a word appear italic

```html
<html>
	<head>
		<title>Italic</title>
	</head>
	<body>
		<p>This is how we make a word appear <i>italic</i>.</p>
		<p>It's a potato <i>Solanum teberosum</i>.</p>
		<p>Captain Cook sailed to Australia on the <i>Endeavour</i>.</p>
	</body>
</html>
```

## Lists
### Ordered Lists

```html
<html>
	<head>
		<title>Ordered Lists</title>
	</head>
	<body>
		<ol>
			<li>Chop potatoes into quarters</li>
			<li>Simmer in salted water for 15-20 minutes until tender</li>
			<li>Heat milk, butter and nutmeg</li>
			<li>Drain potatoes and mash</li>
			<li>Mix in the milk mixture</li>
		</ol>
	</body>
</html>
```

### Unordered Lists

```html
<html>
	<head>
		<title>Unordered Lists</title>
	</head>
	<body>
		<ul>
			<li>1kg King Edward potatoes</li>
			<li>100ml milk</li>
			<li>50g salted butter</li>
			<li>Freshly grated nutmeg</li>
			<li>Salt and pepper to taste</li>
		</ul>
	</body>
</html>
```

## HTML LINKS

### Linking to other sites

```html
<html>
	<head>
		<title>Linking to Other Sites</title>
	</head>
	<body>
		<p>Movie Reviews:
			<ul>
				<li><a href="http://www.empireonline.com">Empire</a></li>
				<li><a href="http://www.metacritic.com">Metacritic</a></li>
				<li><a href="http://www.rottentomatoes.com">Rotten Tomatoes</a></li>
				<li><a href="http://www.variety.com">Variety</a></li>
			</ul>
		</p>
	</body>
</html>
```

### Linking to other pages

Create the following HTML files in the same directory where the template below is stored. You may copy them on the link given below.

- index.html: https://github.com/duaneywadey/HTML-and-CSS-Resources/blob/master/chapter-04/index.html
- about-us.html: https://github.com/duaneywadey/HTML-and-CSS-Resources/blob/master/chapter-04/about-us.html
- movies.html: https://github.com/duaneywadey/HTML-and-CSS-Resources/blob/master/chapter-04/movies.html
- contact.html: https://github.com/duaneywadey/HTML-and-CSS-Resources/blob/master/chapter-04/contact.html


```html
<html>
	<head>
		<title>Linking to Other Pages on the Same Site</title>
	</head>
	<body>
		<p>
			<ul>
				<li><a href="index.html">Home</a></li>
				<li><a href="about-us.html">About</a></li>
				<li><a href="movies.html">Movies</a></li>
				<li><a href="contact.html">Contact</a></li>
			</ul>
		</p>
	</body>
</html>
```