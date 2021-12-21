# Containers & Padding
---
## Containers
containers can fit in multiple widgets [[contaier.png]]
> **tip** if you don't insert child property it works like a background
```dart
        child: Container(
            color: Colors.green[400],
            child: Text("containers wrap childs"), // text is for testing
        ),
```

---
## Padding
padding from `all` directions, padding dosen't make space, instead fill up with the object
```dart
        child: Container(
            padding: EdgeInsets.all(20.0),
            color: Colors.green[400],
            child: Text("from all directions"),
        ),
```

padding different just for `horizontal` and `vertical` like [[paddingExample.png]] 
```dart
        child: Container(
            padding: EdgeInsets.symmetric(horizontal: 30.0, vertical: 15.0),
            color: Colors.red[400],
            child: Text("horizontal and vertical"),
        ),
```

the values inside of the TRB are `left top right bottom` in the same order
```dart
        child: Container(
            padding: EdgeInsets.fromTRB(10.0, 20.0, 30.0, 40.0),
            color: Colors.blue[400],
            child: Text("containers wrap childs"),
        ),
```

there are other method for dimensioning the padding, just type `EdgeInsets.` and check

---
## Margin

works the same as [[#Padding]] but [[margin.png]] makes space instead of enlargeing the widget 
```dart
        child: Container(
            margin: EdgeInsets.all(30.0),
            color: Colors.purple[400],
            child: Text("containers wrap childs"),
        ),
```

---
## Padding & Margin Widgets
on multiple widget the same padding or margin, use `Padding()` or `Margin()`
```dart
        child: Padding(
            padding: EdgeInsets.all(30.0),
            child: Text("the other widget"),
        ),
```


```dart
        child: Margin(
            margin: EdgeInsets.all(30.0),
            child: Text("the other widget"),
        ),
```

---
## Rounded Containers & More
for example [[roundedContainer.png]], but you can round even buttons and other stuff
``` dart
		child: Container(  
			height: 50, 
			width: 100,
			decoration: BoxDecoration(  
				borderRadius: BorderRadius.all(Radius.circular(40)),  
				color: Colors.blue 
			),   
		),
```