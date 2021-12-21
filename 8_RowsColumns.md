# Rows & Colums
---
```dart
        child: Row(
            children: <Widget>[
			
				// every widget you want
			
            ],
        ),
```

```dart
        child: Column(
            children: <Widget>[
			
				// every widget you want
			
            ],
        ),
```

---
## Rows: Alignment
### Horizontal 
the `mainAxisAlignment` in the row is the horizontal, so with this property you can manage the horizontal alignment of the row
```dart
        child: Row(
            mainAxisAlignment: MainAxisAlignment.center,
            children: <Widget>[
                Text("we can have"),
                Text("multiple widgets"),
                Text("in the same row"),
            ],
        ),
```

### Vertical
the `CrossAxisAlignment` in the row is the vertical, so with this property...
```dart
        child: Row(
            crossAxisAlignment: CrossAxisAlignment.center,
            children: <Widget>[
                Text("we can have "),
                Text("multiple widgets "),
                Text("in the same row"),
            ],
        ),
```

### Property Breakdown
here some example with images of the `main` and `cross` axis for understanding

Property | Example | Property | Example 
--- | --- | --- | --- 
`mainAxisAlignment.` | choose below | `CrossAxisAlignment.` | choose below
`center` | [[centerMain.png]] | `center` | [[centerCross.png]]
`spaceBetween` | [[spaceBetween.png]] | `end` | [[endVertical.png]]
`spaceEvenly` | [[spaceEvenly.png]] | `start` | [[startVertical.png]]
`spaceAround` | [[spaceAround.png]] | `stretch` | [[stretchCross.png]]

---
## Column: Vertical & Horizontal Alignment
works the same as [[#Rows Alignment]] but here the `main axis` is inverted because we are working in a columns, not in rows like  [[columnAlignment.png]]


```dart
        child: Column(
            mainAxisAlignment: MainAxisAlignment.end,
            crossAxisAlignment: CrossAxisAlignment.stretch,
            children: <Widget>[

                Container(
                    padding: EdgeInsets.all(10.0),
                    color: Colors.cyan,
                    child: Text("one"),
                ),

                Container(
                    padding: EdgeInsets.all(15.0),
                    color: Colors.pinkAccent,
                    child: Text("two"),
                ),

                Container(
                    padding: EdgeInsets.all(20.0),
                    color: Colors.amber,
                    child: Text("three"),
                ),
                
            ],
        ),
```

---
## Sized Box
we can use the [[sizedBox.png]] for making some space between things
```dart
        child: Column(
            children: <Widget>[
                Text("some space"),
                SizedBox(height: 10.0),
                Text("between things"),
                SizedBox(height: 20.0),
                Text("is useful"),
            ],
        ),
```

---
## Divider
a small line between things, `height` gives empty space in the height
```dart
        child: Divider(
            height: 90.0,
            color: Colors.grey[800],
        )
```
