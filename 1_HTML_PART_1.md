
# HTML BASIC TYPOGRAPHY

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

# Lists
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

# HTML LINKS

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

### Opening links in a new window

```html
<html>
	<head>
		<title>Opening Links in a New Window</title>
	</head>
	<body>
		<p>
			<a href="http://www.imdb.com" target="_blank">Internet Movie Database</a> (opens in new window)
		</p>
	</body>
</html>
```

# Images

### Adding images

```html
<html>

<head>

<title>Adding Images</title>

</head>

<body>

<img src="https://images.unsplash.com/photo-1712928247899-2932f4c7dea3?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Quokka (Setonix brachyurus)" />

</body>

</html>
```

### Adjusting the width and height of images

```html
<html>

<head>

<title>Height and Width of Images</title>

</head>

<body>

<img src="https://images.unsplash.com/photo-1712928247899-2932f4c7dea3?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Quokka (Setonix brachyurus)" alt="Quokka (Setonix brachyurus)" width="600" height="450" />

</body>

</html>
```

### Adding two images

```html
<html>
	<head>
		<title>Where to Place Images in Your Code</title>
	</head>
	<body>
		<div style="width:450">
			<img src="https://images.unsplash.com/photo-1712955685153-1b9c8edd071f?q=80&w=2003&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Bird" width="100" height="100" />
			<p>There are around 10,000 living species of birds that inhabit different ecosystems from the Arctic to the Antarctic. Many species undertake long distance annual migrations, and many more perform shorter irregular journeys.</p>
			<hr />
			<p><img src="https://images.unsplash.com/photo-1712926097966-b86f0d8c131d?q=80&w=2071&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Bird" width="100" height="100" /> There are around 10,000 living species of birds that inhabit different ecosystems from the Arctic to the Antarctic. Many species undertake long distance annual migrations, and many more perform shorter irregular journeys.</p>
			<hr />
			<p>There are around 10,000 living species of birds that inhabit different ecosystems from the Arctic to the Antarctic. <img src="https://images.unsplash.com/photo-1713080045896-0b78f9a6bb55?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" alt="Bird" width="100" height="100" /> Many species undertake long distance annual migrations, and many more perform shorter irregular journeys.</p>
		</div>
	</body>
</html>
```

# HTML Tables 

### Basic Table Structure

 - ```<tr>``` means table row
 - ```<td>``` means table data

```html
<html>
	<head>
		<title>Basic Table Structure</title>
	</head>
	<body>
		<table>
			<tr>
				<td>15</td>
				<td>15</td>
				<td>30</td>
			</tr>
			<tr>
				<td>45</td>
				<td>60</td>
				<td>45</td>
			</tr>
			<tr>
				<td>60</td>
				<td>90</td>
				<td>90</td>
			</tr>
		</table>
	</body>
</html>
```

### Table headings

```html
<html>
	<head>
		<title>Table Headings</title>
	</head>
	<body>
		<table>
			<tr>
				<th></th>
				<th scope="col">Saturday</th>
				<th scope="col">Sunday</th>
			</tr>
			<tr>
				<th scope="row">Tickets sold:</th>
				<td>120</td>
				<td>135</td>
			</tr>
			<tr>
				<th scope="row">Total sales:</th>
				<td>$600</td>
				<td>$675</td>
			</tr>
		</table>
	</body>
</html>
```

### Long tables

- ```<th>``` means table headings. It stores the column name. 

```html
<html>
	<head>
		<title>Long Tables</title>
		<style type="text/css">
			table {
				border: none;}
			thead th {
				border-bottom: 2px solid #444444;
				width: 120px;}
			tfoot td {
				border-top: 1px solid #444444;}
		</style>
	</head>
	<body>
		<table>
			<thead>
				<tr>
					<th>Date</th>
					<th>Income</th>
					<th>Expenditure</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<th>1st January</th>
					<td>250</td>
					<td>36</td>
				</tr>
				<tr>
					<th>2nd January</th>
					<td>285</td>
					<td>48</td>
				</tr>
				<tr>
					<th>3rd January</th>
					<td>260</td>
					<td>42</td>
				</tr>
				<tr>
					<th>4th January</th>
					<td>290</td>
					<td>38</td>
				</tr>
				<tr>
					<th>5th January</th>
					<td>310</td>
					<td>115</td>
				</tr>
				<tr>
					<th>6th January</th>
					<td>168</td>
					<td>14</td>
				</tr>
				<tr>
					<th>7th January</th>
					<td>226</td>
					<td>20</td>
				</tr>
				<tr>
					<th>8th January</th>
					<td>253</td>
					<td>37</td>
				</tr>
				<tr>
					<th>9th January</th>
					<td>294</td>
					<td>33</td>
				</tr>
				<tr>
					<th>10th January</th>
					<td>216</td>
					<td>46</td>
				</tr>
				<tr>
					<th>11th January</th>
					<td>244</td>
					<td>29</td>
				</tr>
				<tr>
					<th>12th January</th>
					<td>297</td>
					<td>32</td>
				</tr>
				<tr>
					<th>13th January</th>
					<td>328</td>
					<td>86</td>
				</tr>
				<tr>
					<th>14th January</th>
					<td>215</td>
					<td>38</td>
				</tr>
				<tr>
					<th>15th January</th>
					<td>254</td>
					<td>30</td>
				</tr>
				<tr>
					<th>16th January</th>
					<td>256</td>
					<td>27</td>
				</tr>
				<tr>
					<th>17th January</th>
					<td>311</td>
					<td>68</td>
				</tr>
				<tr>
					<th>18th January</th>
					<td>212</td>
					<td>39</td>
				</tr>
				<tr>
					<th>19th January</th>
					<td>234</td>
					<td>36</td>
				</tr>
				<tr>
					<th>20th January</th>
					<td>221</td>
					<td>43</td>
				</tr>
				<tr>
					<th>21st January</th>
					<td>259</td>
					<td>38</td>
				</tr>
				<tr>
					<th>22nd January</th>
					<td>246</td>
					<td>31</td>
				</tr>
				<tr>
					<th>23rd January</th>
					<td>248</td>
					<td>17</td>
				</tr>
				<tr>
					<th>24th January</th>
					<td>229</td>
					<td>45</td>
				</tr>
				<tr>
					<th>25th January</th>
					<td>263</td>
					<td>34</td>
				</tr>
				<tr>
					<th>26th January</th>
					<td>258</td>
					<td>41</td>
				</tr>
				<tr>
					<th>27th January</th>
					<td>283</td>
					<td>22</td>
				</tr>
				<tr>
					<th>28th January</th>
					<td>256</td>
					<td>30</td>
				</tr>
				<tr>
					<th>29th January</th>
					<td>278</td>
					<td>47</td>
				</tr>
				<tr>
					<th>30th January</th>
					<td>251</td>
					<td>15</td>
				</tr>
				<tr>
					<th>31st January</th>
					<td>129</td>
					<td>64</td>
				</tr>
			</tbody>
			<tfoot>
				<tr>
					<td></td>
					<td>7824</td>
					<td>1241</td>
				</tr>
			</tfoot>
		</table>
	</body>
</html>
```

### Adding styles to our table

```html
<html>
	<head>
		<title>Border and Background</title>
	</head>
	<body>
		<table border="2" bgcolor="#efefef">
			<tr>
				<th width="150"></th>
				<th>Withdrawn</th>
				<th>Credit</th>
				<th width="150" bgcolor="#cccccc">Balance</th>
			</tr>
			<tr>
				<th>January</th>
				<td>250.00</td>
				<td>660.50</td>
				<td bgcolor="#cccccc">410.50</td>
			</tr>
			<tr>
				<th>February</th>
				<td>135.55</td>
				<td>895.20</td>
				<td bgcolor="#cccccc">1170.15</td>
			</tr>
		</table>
	</body>
</html>
```

# HTML Forms

### Form structure in HTML
```html
<html>
	<head>
		<title>Form Structure</title>
	</head>
	<body>
		<form action="http://www.example.com/subscribe.php" method="get">
			<p>This is where the form controls will appear.</p>
		</form>
	</body>
</html>
```

### Text input in HTML
```html
<html>
	<head>
		<title>Text Input</title>
	</head>
	<body>
		<form action="http://www.example.com/login.php">
			<p>Username:
				<input type="text" name="username" size="15" maxlength="30" />
			</p>
		</form>
	</body>
</html>
```

### Password input in HTML

```html
<html>
	<head>
		<title>Password Input</title>
	</head>
	<body>
		<form action="http://www.example.com/login.php">
			<p>Username:
				<input type="text" name="username" size="15" maxlength="30" />
			</p>
			<p>Password:
				<input type="password" name="password" size="15" maxlength="30" />
			</p>
		</form>
	</body>
</html>
```

### Submit input in HTML

```html
<html>
	<head>
		<title>Submit Button</title>
	</head>
	<body>
		<form action="http://www.example.com/subscribe.php">
			<p>Subscribe to our email list:</p>
			<input type="text" name="email" />
			<input type="submit" name="subscribe" value="Subscribe" />
		</form>
	</body>
</html>
```

### Adding labels to our input fields
```html
<html>
	<head>
		<title>Labelling Form Controls</title>
	</head>
	<body>
		<form action="http://www.example.com/subscribe.php">
			<label>Age: <input type="text" name="age" /></label>
			<br/ >
			Gender:
			<input id="female" type="radio" name="gender" value="f">
			<label for="female">Female</label>
			<input id="male" type="radio" name="gender" value="m">
			<label for="male">Male</label>
		</form>
	</body>
</html>
```


## Other HTML Input Fields

### Text Area field
```html
<html>
	<head>
		<title>Textarea</title>
	</head>
	<body>
		<form action="http://www.example.com/comments.php">
			<p>What did you think of this gig?</p>
			<textarea name="comments" cols="20" rows="4">Enter your comments...</textarea>
		</form>
	</body>
</html>
```

### Email input field
```html
<html>
	<head>
		<title>HTML5 Email Input</title>
	</head>
	<body>
		<form action="http://www.example.org/subscribe.php"> 
			<p>Please enter your email address:</p>
			<input type="email" name="email" />
			<input type="submit" value="Submit" />
		</form>
	</body>
</html>
```

### Date input field
```html
<html>
	<head>
		<title>HTML5 Email Input</title>
	</head>
	<body>
		<form action="http://www.example.org/subscribe.php"> 
			<p>Please enter your email address:</p>
			<input type="email" name="email" />
			<input type="submit" value="Submit" />
		</form>
	</body>
</html>
```

### Radio Buttons

```html
<html>
	<head>
		<title>Radio Button</title>
	</head>
	<body>
		<form action="http://www.example.com/profile.php">
			<p>Please select your favorite genre:
				<br />
				<input type="radio" name="genre" value="rock" checked="checked" /> Rock
				<input type="radio" name="genre" value="pop" /> Pop
				<input type="radio" name="genre" value="jazz" /> Jazz
			</p>
		</form>
	</body>
</html>
```

### Checkbox
```html
<html>
	<head>
		<title>Checkbox</title>
	</head>
	<body>
		<form action="http://www.example.com/profile.php">
			<p>Please select your favorite music service(s):
				<br />
				<input type="checkbox" name="service" value="itunes" checked="checked" /> iTunes
				<input type="checkbox" name="service" value="lastfm" /> Last.fm
				<input type="checkbox" name="service" value="spotify" /> Spotify
			</p>
		</form>
	</body>
</html>
```

### Dropdown list in HTML
```html
<html>
	<head>
		<title>Drop Down List Box</title>
	</head>
	<body>
		<form action="http://www.example.com/profile.php">
			<p>What device do you listen to music on?</p>
			<select name="devices">
				<option value="ipod">iPod</option>
				<option value="radio">Radio</option>
				<option value="computer">Computer</option>
			</select>
		</form>
	</body>
</html>
```

### File input in HTML
```html
<html>
	<head>
		<title>File Input Box</title>
	</head>
	<body>
		<form action="http://www.example.com/upload.php" method="post">
			<p>Upload your song in MP3 format:</p>
			<input type="file" name="user-song" /><br />
			<input type="submit" value="Upload" />
		</form>
	</body>
</html>
```
