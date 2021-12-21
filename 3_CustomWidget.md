# Custom Widgets
---
## Stateless Widget
stateless widget cannot change over time, we use it for not dynamic widget

> for activate the "hot reload" in Android Studio put the code inside a widget like below
>
> in Android Studio you can use the key word `stless` for creating a stateless class, just write it where you want, press enter and you have it
>
> scaffold holds the whole structure of the app, so it's better to use!

we can return everything we want, the scaffold is here just for making Home
`body: Center(),` can be removed, it's just for render something

``` dart
		import 'package:flutter/material.dart';

		void main() => runApp(MaterialApp(
			home: Home(),
		));

		class Home extends StatelessWidget {
			@override
			Widget build(BuildContext context){
				return Scaffold(
					body: Center(

						//everything you want, text is just for example
						child: Text("i'm just a text")

					),
				);
			}
		}
```

---
## Stateful Widget
they can change over time, so we can use it for dynamics widgets

> `stful` for stateful widgets template and you can convert stateless in stateful just using the [[light.png]] in Android Studio
> 
> use `setState()` for refreshing values, otherwise the values didn't change 
> 
> `$` for passing variables into widget and texts

``` dart
        import 'package:flutter/material.dart';

        void main() => runApp(MaterialApp(
            home: Test(),
        ));

        class Test extends StatefulWidget{
            @override
            _TestState createState() => _TestState();
        }

        class _TestState extends State<Test> {

            int counter = 7; //put around here the dynamic code

            @override
            Widget build(BuildContext context){
                return Scaffold(

                    appBar: AppBar(
                        title: Text("$counter"), //variables with $
                    ),

                    floatingActionButton: FloatingActionButton(
                        onPressed: () {

                            setState(() {
                                counter += 1; //for changeing values use setState
                                }
                            );
                        }
                    ),

                );
            }
        }
``` 

`TestState` defines the data of the stateful widget, `Test` is the class to call as the stateless, other things are the same

an example of the code without the code for explaining it

``` dart
        import 'package:flutter/material.dart';

        void main() => runApp(MaterialApp(
            home: Test(),
        ));

        class Test extends StatefulWidget{
            @override
            _TestState createState() => _TestState();
        }

        class _TestState extends State<Test> {

            @override
            Widget build(BuildContext context){
                return Container();
            }
        }
```