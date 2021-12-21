# First app & Scaffold
---
## First App
if you want a rapid mockup for your app this probably works for you
``` dart
        import 'package:flutter/material.dart';

        void main() => runApp(MaterialApp( 
            home: Scaffold(
                
                appBar: AppBar(
                    title: Text("i'm on appbar"),
                    centerTitle: true,
                ),

                body: Center(
                    child: Text("hello"),
                ),

                floatingActionButton: FloatingActionButton(
                    child: Text("click"),
                    onPressed: null,
                ),

            ),
        ));
``` 
`runApp()` what you want when you start the app, we need to pass to him a route widget, this just wraps everything you create for running it
`MaterialApp()` allow us to use material design feature, like text or buttons, *every widget* came from this wrapper 


---
## Scaffold
the scaffold is the main wrapper for an android page

``` dart
        import 'package:flutter/material.dart';

        void main() => runApp(MaterialApp(
            home: Scaffold(

                //everything you want

            ),
        ));
``` 

---
## App Bar
creates a simple [[appBar.png]] on the top of the app where you can put rapid stuff
``` dart
        appBar: AppBar(
            title: Text("i'm on appbar"),
            centerTitle: true,
            elevation: 0.0,
        ),
``` 
`elevation` is the z-coordinate at which to place this material relative to its parent

---
## Body
wraps what you can see of the app, the real widget, the core of the app like [[body.png]]

``` dart
        body: Center(
            child: Text("hello"),
        ),
``` 
	
---
## Floating Button
floating circular button on the bottom right [[floatingButton.png]]
	
``` dart
        floatingActionButton: FloatingActionButton(
            child: Text("click"),
            onPressed: () {},
        ),
``` 
