# Extra Markup

### Block Elements
 - A block element is an elementthat always creates a new line.
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Block Elements</title>
	</head>
	<body>
		<h1>Hiroshi Sugimoto</h1>
		<p>The dates for the ORIGIN OF ART exhibition are as follows:</p>
		<ul>
			<li>Science: 21 Nov - 20 Feb 2010/11</li>
			<li>Architecture: 6 Mar - 15 May 2011</li>
			<li>History: 29 May - 21 Aug 2011</li>
			<li>Religion: 28 Aug - 6 Nov 2011</li>
		</ul>
	</body>
</html>
```

### Inline Elements
 - An inline element doesn't begin with a new line. 
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Inline Elements</title>
	</head>
	<body>
    		<p>
			Timed to a single revolution of the planet around the sun at a 23.4 degrees tilt that plays out the rhythm of the seasons, this <em>Origins of Art</em> cycle is organized around four themes: <b>science, architecture, history</b> and <b>religion</b>.
		</p>
	</body>
</html>
```

### ID Attribute in HTML
 - An id attribute is used only for a single element. 

 ```html
 <!DOCTYPE html>
<html>
	<head>
		<title>ID Attribute</title>
		<style type="text/css">
			p #pullquote {
				text-transform: uppercase;}
		</style>
	</head>
	<body>
		<p>Water and air. So very commonplace are these substances, they hardly attract attention - and yet they vouchsafe our very existence.</p>
		<p id="pullquote">Every time I view the sea I feel a calming sense of security, as if visiting my ancestral home; I embark on a voyage of seeing.</p>
		<p>Mystery of mysteries, water and air are right there before us in the sea.</p>
	</body>
</html>
 ```

### Class attribute in HTML
 - A class attribute can be used by multiple HTML elements.  

 ```html
 <!DOCTYPE html>
<html>
	<head>
		<title>Class Attribute</title>
		<style type="text/css">
			.important {
				text-transform: uppercase;}
			.admittance {
				color: #FF6666;}
		</style>
	</head>
	<body>
		<p class="important">For a one-year period from November 2010, the Marugame Genichiro-Inokuma Museum of Contemporary Art (MIMOCA) will host a cycle of four Hiroshi Sugimoto exhibitions.</p>
		<p>Each will showcase works by the artist thematically contextualized under the headings "Science," "Architecture," "History" and "Religion" so as to present a comprehensive panorama of the artist's oeuvre.</p>
		<p class="important admittance">Hours: 10:00 - 18:00 (No admittance after 17:30)</p>
	</body>
</html>
 ```

### Grouping block elements

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Grouping Block Elements</title>
	</head>
	<body>
		<div id="header">
			<img src="images/logo.gif" alt="Anish Kapoor" />
			<ul>
				<li><a href="index.html">Home</a></li>
				<li><a href="biography.html">Biography</a></li>
				<li><a href="works.html">Works</a></li>
				<li><a href="contact.html">Contact</a></li>
			</ul>
		</div><!-- end of header -->
	</body>
</html>
```

# Basic CSS

### Using Internal CSS
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Using Internal CSS</title>
		<style type="text/css">
			body {
				font-family: arial;
				background-color: rgb(185,179,175);}
			h1 {
				color: rgb(255,255,255);}
		</style>
	</head>
	<body>
		<h1>Potatoes</h1>
		<p>There are dozens of different potato varieties. They are usually described as early, second early and maincrop potatoes.</p>
	</body>
</html>
```

### Using External CSS

- Create a ```styles.css``` file that will store the styles for your HTML.
- Paste the script below on your ```styles.css```  file.

```css
	body {
		font-family: arial;
		background-color: rgb(185,179,175);
	}
	h1 {
		color: rgb(255,255,255);
	}
```

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Using External CSS</title>
		<link href="styles.css" type="text/css" rel="stylesheet" />
	</head>
	<body>
		<h1>Potatoes</h1>
		<p>There are dozens of different potato varieties. They are usually described as early, second early and maincrop potatoes.</p>
	</body>
</html>
```

### CSS Inheritance

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Inheritance</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #665544;
				padding: 10px;}
			.page {
				border: 1px solid #665544;
				background-color: #efefef;
				padding: inherit;}
		</style>
	</head>
	<body>
		<div class="page">
			<h1>Potatoes</h1>
			<p>There are dozens of different potato varieties.</p>
			<p>They are usually described as early, second early and maincrop potatoes.</p>
		</div>
	</body>
</html>
```

### CSS RULES

```html
<!DOCTYPE html>
<html>
	<head>
		<title>How CSS Rules Cascade</title>
		<style type="text/css">
			* {
				font-family: Arial, Verdana, sans-serif;}
			h1 {
				font-family: "Courier New", Courier, monospace;}
			i {
				color: green;}
			i {
				color: red;}
			b {
				color: pink;}
			p b {
				color: blue !important;}
			p b {
				color: violet;}
			p#intro {
				font-size: 100%;}
			p {
				font-size: 75%;}
		</style>
	</head>
	<body>
		<h1>Potatoes</h1>
		<p id="intro">There are <i>dozens</i> of different <b>potato</b> varieties.</p>
		<p>They are usually described as early, second early and maincrop potatoes.</p>
	</body>
</html>
```

### External CSS Example

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Understanding CSS - Thinking Inside the Box</title>
		<style type="text/css">
			body {
				font-family: Helvetica, Arial, sans-serif;
				color: #665544;
				border: 2px solid #e7642c;
				padding: 20px;}
			h1, h2, p {
				border: 2px solid #e7642c;
				padding: 10px;
				line-height: 2em;}
			i, a, a:hover {
				color: #665544;
				border: 2px solid #7fcbae;
				padding: 5px;}
		</style>
	</head>
	<body>
		<h1>The Cottage Garden</h1>
		<p>The <i>cottage garden</i> is a distinct style of garden that uses an informal design, dense plantings, and a mixture of ornamental and edible plants.</p>
		<p>The Cottage Garden originated in <a href="">England</a> and its history can be traced back for centuries, although they were re-invented in 1870's England, when stylized versions were formed as a reaction to the more structured and rigorously maintained <a href="">English estate gardens</a>.</p>
		<p>The earliest cottage gardens were more practical than their modern descendants, with an emphasis on vegetables and herbs, along with some fruit trees.</p>
	</body>
</html>
```

### External CSS Example (NO BORDER)

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Understanding CSS - Thinking Inside the Box</title>
		<style type="text/css">
			body {
				font-family: Helvetica, Arial, sans-serif;
				color: #665544;
				padding: 22px;}
			h1, h2, p {
				padding: 12px;
				line-height: 2em;}
			i, a, a:hover, a:visited {
				color: #665544;}
		</style>
	</head>
	<body>
		<h1>The Cottage Garden</h1>
		<p>The <i>cottage garden</i> is a distinct style of garden that uses an informal design, dense plantings, and a mixture of ornamental and edible plants.</p>
		<p>The Cottage Garden originated in <a href="">England</a> and its history can be traced back for centuries, although they were re-invented in 1870's England, when stylized versions were formed as a reaction to the more structured and rigorously maintained <a href="">English estate gardens</a>.</p>
		<p>The earliest cottage gardens were more practical than their modern descendants, with an emphasis on vegetables and herbs, along with some fruit trees.</p>
	</body>
</html>
```
