# Lists & Grids
---
## Static List, Static Item Number
[[staticList.png]]
``` dart
	child: ListView(
	  children: const <Widget>[
		ListTile(
		  leading: Icon(Icons.map),
		  title: Text('Map'),
		),
		ListTile(
		  leading: Icon(Icons.photo_album),
		  title: Text('Album'),
		),
		ListTile(
		  leading: Icon(Icons.phone),
		  title: Text('Phone'),
		),
	  ],
	)
```

---
## Static List, Dynamic Item Number
[[staticListDynamicNum.png]]
```dart
		import 'package:flutter/material.dart';

		void main() {
		  runApp(
			MyApp( // here pass values that you want to generate in the list
			  items: List<String>.generate(50, (i) => 'Item $i'),
			),
		  );
		}

		class MyApp extends StatelessWidget {

		  final List<String> items; // holds the data
		  // here arrives the values passed
		  const MyApp({Key? key, required this.items}) : super(key: key);
		  
		  @override
		  Widget build(BuildContext context) {
			return MaterialApp(
			  home: Scaffold(
			  
				body: ListView.builder( // this is the effective list
				  itemCount: items.length,
				  itemBuilder: (context, index) {
				  
					return ListTile( // return every item you want
					  title: Text(items[index]),
					); // list tile is for example
					
				  },
				),
				
			  ),
			);
		  }
		}
```

---
## Static Grid
[[staticGrid.png]]
```dart
        child: GridView.count(
          crossAxisCount: 2, // create a grid with 2 columns
          // Generate 50 widgets that display their index in the List.
          children: List.generate(50, (index) {
            return Center(
              child: Text(
                'Item $index',
                style: Theme.of(context).textTheme.headline5,
              ),
            );
          }),
        ),
```