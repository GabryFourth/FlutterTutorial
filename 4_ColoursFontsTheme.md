# Colours & Fonts & Theme
---
## Color
[color tool material](https://material.io/resources/color/)

---
## Text Property
 with style property you can add to the text some styles, this code outputs [this](2021-05-28-20-27-09.png)
	
``` dart
	child: Text(
		"hello",
		style: TextStyle(
			fontSize: 20.0,
			fontWeight: FontWeight.bold,
			letterSpacing: 5.0,
			color: Colors.grey[600],
			backgroundColor: Colors.pink[100],
		),
	),
```

---
## Change Font
[Google Fonts](https://fonts.google.com/) for getting the font file, ex. IndieFlower-Regular
create a folder called `fonts` into the project like [this](2021-05-27-14-03-11.png)

put this code into `pubspec.yaml`
``` yaml
	fonts:
	- family: IndieFlower
	  fonts:
	  - asset: fonts/IndieFlower-Regular.ttf
```
	
put this code into `main.dart` wherever you need to change the font of a widget,
remember to put before Text and Textstyle

``` dart
	child: Text(
		"hello",
		style: TextStyle(
			fontFamily: "indieFlower",
		),
	),
```

---
# Theme
use instead of the classic colors the [[themeColor.png]] 
``` dart
	child: Text(
		"colored text",
		style: TextStyle(
			color: Theme.of(context).primaryColor, // referres to the theme
			fontWeight: FontWeight.bold
		),
	),
```

a complete `example` of a modified theme, you  can change *everything* 
```dart
        import 'package:flutter/material.dart';

        void main() => runApp(MaterialApp(
		  theme: ThemeData(
				brightness: Brightness.dark, // changes to dark mode
				primaryColor: Colors.lightBlue[800], // changes the primary color
				
				fontFamily: 'Georgia', // default font family.

				textTheme: TextTheme( // define the default TextTheme
				  	headline6: TextStyle(
						fontSize: 36.0, 
						fontStyle: FontStyle.italic
					),
				  	bodyText2: TextStyle(
						fontSize: 14.0, 
						fontFamily: 'Hind'
					),
				),
		  	),
            home: Scaffold( body: Center( child: Text("just a test") ) )
        ));
```
