# Styling with CSS

### Background color
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Background Color</title>
		<style type="text/css">
			body {
				background-color: rgb(200,200,200);
				color: white;
				padding: 20px;
				font-family: Arial, Verdana, sans-serif;}
			h1 {
				background-color: DarkCyan;
				padding: inherit;}
			h2 {
				background-color: #ee3e80;
				padding: inherit;}
			p {
				background-color: white;
				color: rgb(100,100,90);
				padding: inherit;}
		</style>
	</head>
	<body>
		<h1>Marine Biology</h1>
		<h2>The Composition of Seawater</h2>
		<p>Almost anything can be found in seawater. This includes dissolved materials from Earth's crust as well as materials released from organisms. The most important components of seawater that influence life forms are salinity, temperature, dissolved gases (mostly oxygen and carbon dioxide), nutrients, and pH. These elements vary in their composition as well as in their influence on marine life.</p>
	</body>
</html>
```

### Foreground color

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Foreground Color</title>
		<style type="text/css">
			body {
				padding: 20px;
				font-family: Arial, Verdana, sans-serif;}
			/* color name */
			h1 {
				color: DarkCyan;}
			/* hex code */
			h2 {
				color: #ee3e80;}						
			/* rgb value */
			p {
				color: rgb(100,100,90);}
		</style>
	</head>
	<body>
		<h1>Marine Biology</h1>
		<h2>The Composition of Seawater</h2>
		<p>Almost anything can be found in seawater. This includes dissolved materials from Earth's crust as well as materials released from organisms. The most important components of seawater that influence life forms are salinity, temperature, dissolved gases (mostly oxygen and carbon dioxide), nutrients, and pH. These elements vary in their composition as well as in their influence on marine life.</p>
	</body>
</html>
```

### Opacity in CSS
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Opacity</title>
		<style type="text/css">
			div {
				width: 100px;
				height: 100px;
				margin: 40px;
				display: inline-block;
				background-color: #ee3e80;}
			p {
				width: 100px;
				height: 100px;
				position: relative;
				top: 20px;
				left: 20px;
				margin: 20px;}
			p.one {
				background-color: rgb(0,0,0);
				opacity: 0.5;}
			p.two {
				background-color: rgb(0,0,0);
				background-color: rgba(0,0,0,0.5);}
		</style>
	</head>
	<body>
		<div><p class="one"></p></div>
		<div><p class="two"></p></div>
	</body>
</html>
```
### Basic CSS with HTML elements

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Color</title>
		<style type="text/css">
			body {
				background-color: silver;
				color: white;
				padding: 20px;
				font-family: Arial, Verdana, sans-serif;}
			h1 {
				background-color: #ffffff;
				background-color: hsla(0,100%,100%,0.5);
				color: #64645A;
				padding: inherit;}
			p {
				padding: 5px;
				margin: 0px;}
			p.zero {
				background-color: rgb(238,62,128);}
			p.one {
				background-color: rgb(244,90,139);}
			p.two {
				background-color: rgb(243,106,152);}
			p.three {
				background-color: rgb(244,123,166);}
			p.four {
				background-color: rgb(245,140,178);}
			p.five {
				background-color: rgb(246,159,192);}
			p.six {
				background-color: rgb(245,176,204);}
			p.seven {
				background-color: rgb(0,187,136);}
			p.eight {
				background-color: rgb(140,202,242);}
			p.nine {
				background-color: rgb(114,193,240);}
			p.ten {
				background-color: rgb(84,182,237);}
			p.eleven {
				background-color: rgb(48,170,233);}
			p.twelve {
				background-color: rgb(0,160,230);}
			p.thirteen {
				background-color: rgb(0,149,226);}
			p.fourteen {
				background-color: rgb(0,136,221);}
		</style>
	</head>
	<body>
		<h1>pH Scale</h1>
		<p class="fourteen">14.0 VERY ALKALINE</p>
		<p class="thirteen">13.0</p>
		<p class="twelve">12.0</p>
		<p class="eleven">11.0</p>
		<p class="ten">10.0</p>
		<p class="nine">9.0</p>	
		<p class="eight">8.0</p>
		<p class="seven">7.0 NEUTRAL</p>
		<p class="six">6.0</p>
		<p class="five">5.0</p>
		<p class="four">4.0</p>
		<p class="three">3.0</p>	
		<p class="two">2.0</p>
		<p class="one">1.0</p>
		<p class="zero">0.0 VERY ACID</p>
	</body>
</html>
```

### Font Family
 - CSS Property to change font family

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Font Family</title>
		<style type="text/css">
			body {
				font-family: Georgia, Times, serif;}
			h1, h2 {
				font-family: Arial, Verdana, sans-serif;}
			.credits {
				font-family: "Courier New", Courier, monospace;}
		</style>
	</head>
	<body>
		<h1>Briards</h1>
		<p class="credits">by Ivy Duckett</p>
		<p class="intro">The <a class="breed" href="http://en.wikipedia.org/wiki/Briard">briard</a>, or berger de brie, is a large breed of dog traditionally used as a herder and guardian of sheep.</p>
		<h2>Breed History</h2>
		<p>The briard, which is believed to have originated in France, has been bred for centuries to herd and to protect sheep. The breed was used by the French Army as sentries, messengers and to search for wounded soldiers because of its fine sense of hearing. Briards were used in the First World War almost to the point of extinction. Currently the population of briards is slowly recovering. Charlemagne, Napoleon, Thomas Jefferson and Lafayette all owned briards.</p>
	</body>
</html>
```

### Font Size
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Font Size</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				font-size: 12px;}
			h1 {
				font-size: 200%;}
			h2 {
				font-size: 1.3em;}
		</style>
	</head>
	<body>
		<h1>Briards</h1>
		<p class="credits">by Ivy Duckett</p>
		<p class="intro">The <a class="breed" href="http://en.wikipedia.org/wiki/Briard">briard</a>, or berger de brie, is a large breed of dog traditionally used as a herder and guardian of sheep.</p>
		<h2>Breed History</h2>
		<p>The briard, which is believed to have originated in France, has been bred for centuries to herd and to protect sheep. The breed was used by the French Army as sentries, messengers and to search for wounded soldiers because of its fine sense of hearing. Briards were used in the First World War almost to the point of extinction. Currently the population of briards is slowly recovering. Charlemagne, Napoleon, Thomas Jefferson and Lafayette all owned briards.</p>
	</body>
</html>
```

### Font weight 

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Font Weight</title>
		<style type="text/css">			.credits {
				font-weight: bold;}
		</style>
	</head>
	<body>
		<h1>Briards</h1>
		<p class="credits">by Ivy Duckett</p>
		<p class="intro">The <a class="breed" href="http://en.wikipedia.org/wiki/Briard">briard</a>, or berger de brie, is a large breed of dog traditionally used as a herder and guardian of sheep.</p>
		<h2>Breed History</h2>
		<p>The briard, which is believed to have originated in France, has been bred for centuries to herd and to protect sheep. The breed was used by the French Army as sentries, messengers and to search for wounded soldiers because of its fine sense of hearing. Briards were used in the First World War almost to the point of extinction. Currently the population of briards is slowly recovering. Charlemagne, Napoleon, Thomas Jefferson and Lafayette all owned briards.</p>
	</body>
</html>
```

### Letter and word spacing
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Letter and Word Spacing</title>
		<style type="text/css">			h1, h2 {
				text-transform: uppercase;
				letter-spacing: 0.2em;}
			.credits {
				font-weight: bold;
				word-spacing: 1em;}
		</style>
	</head>
	<body>
		<h1>Briards</h1>
		<p class="credits">by Ivy Duckett</p>
		<p class="intro">The <a class="breed" href="http://en.wikipedia.org/wiki/Briard">briard</a>, or berger de brie, is a large breed of dog traditionally used as a herder and guardian of sheep.</p>
		<h2>Breed History</h2>
		<p>The briard, which is believed to have originated in France, has been bred for centuries to herd and to protect sheep. The breed was used by the French Army as sentries, messengers and to search for wounded soldiers because of its fine sense of hearing. Briards were used in the First World War almost to the point of extinction. Currently the population of briards is slowly recovering. Charlemagne, Napoleon, Thomas Jefferson and Lafayette all owned briards.</p>
	</body>
</html>
```

### Text-align property

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Text Align</title>
		<style type="text/css">
			h1 {
				text-align: left;}
			p {
				text-align: justify;}
			.credits {
				text-align: right;}
		</style>
	</head>
	<body>
		<h1>Briards</h1>
		<p class="credits">by Ivy Duckett</p>
		<p class="intro">The <a class="breed" href="http://en.wikipedia.org/wiki/Briard">briard</a>, or berger de brie, is a large breed of dog traditionally used as a herder and guardian of sheep.</p>
		<h2>Breed History</h2>
		<p>The briard, which is believed to have originated in France, has been bred for centuries to herd and to protect sheep. The breed was used by the French Army as sentries, messengers and to search for wounded soldiers because of its fine sense of hearing. Briards were used in the First World War almost to the point of extinction. Currently the population of briards is slowly recovering. Charlemagne, Napoleon, Thomas Jefferson and Lafayette all owned briards.</p>
	</body>
</html>
```

### Text-decoration
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Text Decoration</title>
		<style type="text/css">			.credits {
				text-decoration: underline;}
			a {
				text-decoration: none;}
		</style>
	</head>
	<body>
		<h1>Briards</h1>
		<p class="credits">by Ivy Duckett</p>
		<p class="intro">The <a class="breed" href="http://en.wikipedia.org/wiki/Briard">briard</a>, or berger de brie, is a large breed of dog traditionally used as a herder and guardian of sheep.</p>
		<h2>Breed History</h2>
		<p>The briard, which is believed to have originated in France, has been bred for centuries to herd and to protect sheep. The breed was used by the French Army as sentries, messengers and to search for wounded soldiers because of its fine sense of hearing. Briards were used in the First World War almost to the point of extinction. Currently the population of briards is slowly recovering. Charlemagne, Napoleon, Thomas Jefferson and Lafayette all owned briards.</p>
	</body>
</html>
```

### Text-shadow
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Text Shadow</title>
		<style type="text/css">
			p {
				font-size: 200%;
				padding: 20px;
				text-align: center;}
			p.one {
				background-color: #eeeeee;
				color: #666666;
				text-shadow: 1px 1px 0px #000000;}
			p.two {
				background-color: #dddddd;
				color: #666666;
				text-shadow: 1px 1px 3px #666666;}
			p.three {
				background-color: #cccccc;
				color: #ffffff;
				text-shadow: 2px 2px 7px #111111;}
			p.four {
				background-color: #bbbbbb;
				color: #cccccc;
				text-shadow: -1px -2px #666666;}
			p.five {
				background-color: #aaaaaa;
				color: #ffffff;
				text-shadow: -1px -1px #666666;}
		</style>
	</head>
	<body>
		<p class="one">The briard is known as a heart wrapped in fur.</p>
		<p class="two">The briard is known as a heart wrapped in fur.</p>
		<p class="three">The briard is known as a heart wrapped in fur.</p>
		<p class="four">The briard is known as a heart wrapped in fur.</p>
		<p class="five">The briard is known as a heart wrapped in fur.</p>
	</body>
</html>
```

### Applying the concepts
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Text</title>
		<style type="text/css">
			body {
				padding: 20px;}
			h1, h2, h3, a {
				font-weight: normal;
				color: #0088dd;
				margin: 0px;}
			h1 {
				font-family: Georgia, Times, serif;
				font-size: 250%;
				text-shadow: 2px 2px 3px #666666;
				padding-bottom: 10px;}
			h2 {
				font-family: "Gill Sans", Arial, sans-serif;
				font-size: 90%;
				text-transform: uppercase;
				letter-spacing: 0.2em;}
			h3 {
				font-size: 150%;}
			p {
				font-family: Arial, Verdana, sans-serif;
				line-height: 1.4em;
				color: #665544;}
			p.intro:first-line {
				font-weight: bold;}
			.credits {
				font-style: italic;	
				text-align: right;}
			a {
				text-decoration: none;}
			a:hover {
				text-decoration: underline;}
		</style>
	</head>
	<body>
		<h1>Briards</h1>
		<h2>A Heart wrapped in fur</h2>
		<p class="intro">The <a class="breed" href="http://en.wikipedia.org/wikiBriard">briard</a>, or berger de brie, is a large breed of dog traditionally used as a herder and guardian of sheep.</p>
		<h3>Breed History</h3>
		<p>The briard, which is believed to have originated in France, has been bred for centuries to herd and to protect sheep. The breed was used by the French Army as sentries, messengers and to search for wounded soldiers because of its fine sense of hearing. Briards were used in the First World War almost to the point of extinction. Currently the population of briards is slowly recovering. Charlemagne, Napoleon, Thomas Jefferson and Lafayette all owned briards.</p>
		<p class="credits">by Ivy Duckett</p>
	</body>
</html>
```


### Border-color

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Border Color</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			p {
				border-style: solid; 
				border-width: 3px;
				width: 200px;}
			p.one {
				border-color: #0088dd;}
			p.two {
				border-color: #bbbbaa #111111 #ee3e80 #0088dd;}
		</style>
	</head>
	<body>
		<p class="one">The ARP Odyssey was introduced in 1972.</p>
		<p class="two">The ARP Odyssey was introduced in 1972.</p>
	</body>
</html>
```

### Border width 
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Border Width</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			p {
				width: 200px;
				border-style: solid;}
			p.one {
				border-width: 2px;}
			p.two {
				border-width: thick;}
			p.three {
				border-width: 1px 4px 12px 4px;}
		</style>
	</head>
	<body>
		<p class="one">Hohner's "Clavinet" is essentially an electric clavichord.</p>
		<p class="two">Hohner's "Clavinet" is essentially an electric clavichord.</p>
		<p class="three">Hohner's "Clavinet" is essentially an electric clavichord.</p>
	</body>
</html>
```

### Border style
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Border Style</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			p {
				width: 250px;
				border-width: 3px;}
			p.one {
				border-style: solid;}
			p.two {
				border-style: dotted;}
			p.three {
				border-style: dashed;}
			p.four {
				border-style: double;}
			p.five {
				border-style: groove;}
			p.six {
				border-style: ridge;}
			p.seven {
				border-style: inset;}
			p.eight {
				border-style: outset;}
		</style>
	</head>
	<body>
		<p class="one">Wurlitzer Electric Piano</p>
		<p class="two">Wurlitzer Electric Piano</p>
		<p class="three">Wurlitzer Electric Piano</p>
		<p class="four">Wurlitzer Electric Piano</p>
		<p class="five">Wurlitzer Electric Piano</p>
		<p class="six">Wurlitzer Electric Piano</p>
		<p class="seven">Wurlitzer Electric Piano</p>
		<p class="eight">Wurlitzer Electric Piano</p>
	</body>
</html>
```

### Border radius
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Border Radius</title>
		<style type="text/css">
			p {
				border: 5px solid #ee3e80;
				padding: 20px;
				width: 275px;
				border-radius: 10px;
				-moz-border-radius: 10px;
				-webkit-border-radius: 10px;} 
		</style>
	</head>
	<body>
		<p>Pet Sounds featured a number of unconventional instruments such as bicycle bells, buzzing organs, harpsichords, flutes, Electro-Theremin, dog whistles, trains, Hawaiian-sounding string instruments, Coca-Cola cans and barking dogs.</p>
	</body>
</html>
```

### Width and height property
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Width Height</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			div {
				width: 400px;
				height: 300px;
				background-color: #ee3e80;}
			p {
				height: 75%;
				width: 75%;
				background-color: #e1ddda;}
		</style>
	</head>
	<body>
		<div>
			<p>The Moog company pioneered the commercial manufacture of modular voltage-controlled analog synthesizer systems in the early 1950s.</p>
		</div>
	</body>
</html>
```

### Visibility property

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Visibility</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			li {
				display: inline; 
				margin-right: 10px;}
			li.coming-soon {
				visibility: hidden;}
		</style>
	</head>
	<body>
		<ul>
			<li>Home</li>
			<li>Products</li>
			<li class="coming-soon">Services</li>
			<li>About</li>
			<li>Contact</li>
		</ul>
	</body>
</html>
```

### Margin property
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Margin</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			p {
				width: 200px;
				border: 2px solid #0088dd;
				padding: 10px;}
			p.example {
				margin: 20px;}
		</style>
	</head>
	<body>
		<p>Analog synthesizers are often said to have a "warmer" sound than their digital counterparts.</p>
		<p class="example">Analog synthesizers are often said to have a "warmer" sound than their digital counterparts.</p>
	</body>
</html>
```

### Min-height and max-height
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Min Height Max Height</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			h2, p {
				width: 400px;
				font-size: 90%;
				line-height: 1.2em;}
			h2 {
				color: #0088dd;
				border-bottom: 1px solid #0088dd;}
			p {
				min-height: 10px;
				max-height: 30px;}
		</style>
	</head>
	<body>
		<h2>Fender Mustang</h2>
		<p>The Fender Mustang was introduced in 1964 as the basis of a major redesign of Fender's student models then consisting of the Musicmaster and Duo-Sonic. It was originally popular in sixties surf music and attained cult status in the 1990s largely as a result of its use by a number of alternative rock bands.</p>
		<h2>Fender Stratocaster</h2>
		<p>The Fender Stratocaster or "Strat" is one of the most popular electric guitars of all time, and its design has been copied by many guitar makers. It was designed by Leo Fender, George Fullerton and Fredie Tavares in 1954.</p>
		<h2>Gibson Les Paul</h2>
		<p>The Gibson Les Paul is a solid body electric guitar that was first sold in 1952. The Les Paul was designed by Ted McCarty in collaboration with popular guitarist Les Paul, whom Gibson enlisted to endorse the new model. It is one of the most well-known electric guitar types in the world.</p>
	</body>
</html>
```

### Min-width and max-width
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Min Width Max Width</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			th {
				border-bottom: 1px solid #0088dd; 
				text-align: left; 
				color: #0088dd;
				font-weight: normal;}
			td {
				min-width: 150px;
				min-height: 200px;
				vertical-align: top;
				line-height: 1.4em;}
			td.description {
				min-width: 450px;
				max-width: 650px;
				text-align: left;
				padding: 5px;
				margin: 0px;}
			</style>
	</head>
	<body>
		<table>
			<tr>
				<th>Photo</th>
				<th>Description</th>
				<th>Price</th>
			</tr>
			<tr>
				<td><img src="images/rhodes.jpg" width="200" height="150" alt="Fender Rhodes" /></td>
				<td class="description">The Rhodes piano is an electro-mechanical piano, invented by Harold Rhodes during the fifties and later manufactured in a number of models, first in collaboration with Fender and after 1965 by CBS. It employs a piano-like keyboard with hammers that hit small metal tines, amplified by electromagnetic pickups.</td>
				<td>$1400</td>
			</tr>
			<tr>
				<td><img src="images/wurlitzer.jpg" width="200" height="150" alt="Wurlitzer EP200" /></td>
				<td class="description">The Wurlitzer electric piano is an electro-mechanical piano, created by the Rudolph Wurlitzer Company of Mississippi. The Wurlitzer company itself never called the instrument an "electric piano", instead inventing the phrase "Electronic Piano" and using this as a trademark throughout the production of the instrument. It employs a piano-like keyboard with hammers that hit small metal tines, amplified by electromagnetic pickups.</td>
				<td>$1600</td>
			</tr>
			<tr>
				<td><img src="images/clavinet.jpg" width="200" height="150" alt="Hohner Clavinet D6" /></td>
				<td class="description">A Clavinet is an electronically amplified clavichord manufactured by the Hohner company. Each key uses a rubber tip to perform a hammer on a string. Its distinctive bright staccato sound is often compared to that of an electric guitar. Various models were produced over the years, including the models I, II, L, C, D6, and E7.</td>
				<td>$1200</td>
			</tr>
		</table>
	</body>
</html>
```

### Padding
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Padding</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;}
			p {
				width: 275px;
				border: 2px solid #0088dd;}
			p.example {
				padding: 10px;}
		</style>
	</head>
	<body>
		<p>Analog synths produce a wave sound, whereas the sounds stored on a digital synth have been sampled and then turned into numbers.</p>
		<p class="example">Analog synths produce a wave sound, whereas the sounds stored on a digital synth have been sampled and then turned into numbers.</p>
	</body>
</html>
```

### Overflow property
```html
<!DOCTYPE html>
<html>
	<head>
		<title>Overflow</title>
		<style type="text/css">
			body {
				font-family: Arial, Verdana, sans-serif;
				color: #111111;
				font-size: 90%;
				line-height: 1.2em;
				width: 200px;}
			h2 {
				color: #0088dd;
				border-bottom: 1px solid #0088dd;}
			p {
				min-height: 30px;
				max-height: 85px;}
			p.one {
				overflow: hidden;}
			p.two {
				overflow: scroll;}
		</style>
	</head>
	<body>
		<h2>Fender Stratocaster</h2>
		<p class="one">The Fender Stratocaster or "Strat" is one of the most popular electric guitars of all time, and its design has been copied by many guitar makers. It was designed by Leo Fender, George Fullerton and Fredie Tavares in 1954.</p>
		<h2>Gibson Les Paul</h2>
		<p class="two">The Gibson Les Paul is a solid body electric guitar that was first sold in 1952. The Les Paul was designed by Ted McCarty in collaboration with popular guitarist Les Paul, whom Gibson enlisted to endorse the new model. It is one of the most well-known electric guitar types in the world.</p>
	</body>
</html>
```

### Applying the concepts

```html
<!DOCTYPE html>
<html>
	<head>
		<title>Boxes</title>
		<style type="text/css">
			body {
				font-size: 80%;
				font-family: "Courier New", Courier, monospace;
				letter-spacing: 0.15em;	
				background-color: #efefef;}
			#page {
				max-width: 940px;
				min-width: 720px;
				margin: 10px auto 10px auto;
				padding: 20px;
				border: 4px double #000;
				background-color: #ffffff;}
			#logo {
				width: 150px;
				margin: 10px auto 25px auto;}
			ul {
				width: 570px;
				padding: 15px;
				margin: 0px auto 0px auto;
				border-top: 2px solid #000;
				border-bottom: 1px solid #000;
				text-align: center;}
			li {
				display: inline;
				margin: 0px 3px;}
			p {
				text-align: center;
				width: 600px; 
				margin: 20px auto 20px auto; 
				font-weight: normal;}
			a {
				color: #000000;
				text-transform: uppercase;
				text-decoration: none;
				padding: 6px 18px 5px 18px;}
			a:hover, a.on {
				color: #cc3333;
				background-color: #ffffff;}
		</style>
	</head>
	<body>
		<div id="page">
			<div id="logo">
				<img src="images/logo.gif" alt="The Analog Specialists" />
			</div>
			<ul id="navigation">
				<li><a href="#" class="on">Home</a></li>
				<li><a href="#">For Sale</a></li>
				<li><a href="#">Repairs</a></li>
				<li><a href="#">About</a></li>
				<li><a href="#">Contact</a></li>
			</ul>
			<p>
				<img src="images/keys.jpg" alt="Fender Rhodes, Hohner Clavinet, and Wurlitzer EP200" />
			</p>
			<p>
				We specialize in the sale and repair of classic keyboards, in particular the Fender Rhodes, Wurlitzer EP200, and Hohner Clavinet.
			</p>
		</div>
	</body>
</html>
```






