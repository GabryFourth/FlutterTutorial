# Buttons & Icons
---
## Icons
it outputs something like [[icon.png]]
``` dart
        child: Icon(
            Icons.local_airport,
            color: Colors.pink,
            size: 50.0,
        ),
```

---
## Buttons
it outputs something like [[button.png]]
you can have it with a little shadow changeing `TextButton()` with `ElevatedButton()`
``` dart
        child: TextButton(
            onPressed: () {
                print("you clicked me");
            },
            child: Text("inside button"),
        ),
```
	
---
## Button with Icons
it outputs something like [[buttonWithIcon.png]]
``` dart
        child: ElevatedButton.icon(
            onPressed: () {},
            icon: Icon(
                Icons.mail
            ),
            label: Text("mail"),
        ),
```
	
---
## Icons that are Buttons
it outputs something like [[iconButton.png]]
``` dart 
        child: IconButton(
            onPressed: () {},
            icon: Icon(Icons.alarm_off),
            color: Colors.pinkAccent,
        ),
```

---
## Gesture Detector
you can make *everything* clickable, with `GestureDetector`
``` dart
	child: GestureDetector(
		onTap: () { // you can change "onTap" with "onLongPress" and others
			print("clicked"); 
		},
		child: Container(
			height: 70.0,
			width: 70.0,
			color: Colors.red,
			child: Text("click me")
		),
	),
```