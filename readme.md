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
$primary-color: red;
.contoh{
	color : $primary-color;
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
