# Sass 
* Installation 
* Hello world 
* @import sass (partial)
* @extend
* @mixin and @include

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

## @import sass (partial) 
sass @import can import another file of sass (.scss) extention begin _filename, example
* File name (_testName.scss)
* main css 
```css
@import "testName"
```

## @extend 
sass posible to make extend css for example class for another definition
### example
```css
$bg-mainPanel : red;
.mainPanel {
	margin-top: 20px;
	background-color: $bg-mainPanel; 
}
.panel1{
	@extend .mainPanel;
	font-size: 1em;
}
.panel2{
	@extend .mainPanel;
	font-size: 2em;
}
```

## @mixin and @include
almost the same as @extend, the difference is, with @mixin we can make as a method, definition and so we can send the variable from argument to parameter.
@mixin to definition as method, and @include to call a @mixin.
#### example : 
```css
@mixin border-radius($volume){
	-moz-border-radius: $volume;
	-webkit-border-radius: $volume;
	-ms-border-radius: $volume;
	border-radius: $volume;
}

.panel2{
	@extend .mainPanel;
	@include border-radius(50px);
	font-size: 2em;
}

```