# Sass 
* Installation 
* Hello world 

## Installation 
### windows 
* Install Ruby : https://rubyinstaller.org/downloads/ 
* Install sass command : 
```java
gem install sass
```

## Hello world
* create main.scss 
```css
$bg-nav : black;
$bg-link : blue;
$hover-color: yellow;
$text-color: white;
nav {
	ul {
		background: $bg-nav;
		margin: 0;
		list-style:none;
		padding: 0;
	}
	li{
		display: inline-block;
		background: $bg-link;
	}
	a{
		color: $text-color;
		display: inline-block;
		text-decoration: none;
		padding: 10px 18px;
	}
	a:hover{
		background: $hover-color;
	}
}
```
* create html file, example : 
```html
<!Doctype html>
<html>
	<head>
		<title>hello sass</title>
		<link rel="stylesheet" href="main.css" />
	</head>
	<body>
		<nav>
			<ul>
				<li><a href="#">Home</a></li>
				<li><a href="#">About</a></li>
				<li><a href="#">Contact</a></li>
			</ul>
		</nav>
		<div class="contoh">
			hallo, arrizaqu
		</div>
	</body>
</html>
```
* check command 
```java
sass --watch F:\data\Repository_2\ex-sass\app\main.scss:main.css
```
so, it will automatically created main.css file 
