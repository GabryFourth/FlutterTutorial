# Flutter Generals
---
## Testing Code 
for testing the other stuff inside this tutorial use this [[#Testing Code]], putting instead of `// everything you want` the code starting with `child:` around the next tutorial pages
```dart
        import 'package:flutter/material.dart';

        void main() => runApp(MaterialApp(
            home: Home(),
        ));

        class Home extends StatelessWidget {
            @override
            Widget build(BuildContext context){
                return Scaffold(
                    body: Center(

                        // everything you want

                    ),
                );
            }
        }
```

---
## [Dart Pad](https://dartpad.dartlang.org/flutter) 
put the code above in this page and run it, `learn by watching`

---

## Widget
in flutter everything is a widget, 
```dart
			Center(), 
```
widgets starts with a `Capital Letter`  because they are the constructor of their class

---
## Property
are the parameters of the [[#Widget]] constructor 
```dart
			Center( 
				property: "the value of the property",
				property2: MethodOrWidgetPassedInTheProperty(),
				child: Text("example") // real example of it
			), 
```
property can have [[#Widget]] inside of it,  `child: ...` kinda means `Center` this `Text`


>### Ternary Operator
>used often in the [[#Property]]s for rapid `(if) ? then : else` in the widgets
>``` dart
>	property: (condition) ? thisIs = "then" : thisIs = "else";
>```
	
---
## Light Tool
use [[lightTool.png]], makes your work easier. Try it while working with `Android Studio`

---
## Flutter Docs
use [Flutter Docs](https://docs.flutter.dev/), they provides good run-time examples and explanation

---
# Other Useful Widget
a short list of other useful widget we didn't breakdown in the tutorial

>### Page Manager
create multiple pages with the [Page View](https://api.flutter.dev/flutter/widgets/PageView-class.html) and then manage it with the [Page Controller](https://api.flutter.dev/flutter/widgets/PageController-class.html) 

>### Animated Containers
[Animated Containers](https://docs.flutter.dev/cookbook/animation/animated-container) do what they say  

>### Constrained Box
the [Constrained Box](https://api.flutter.dev/flutter/widgets/ConstrainedBox-class.html) it's used for making maximum and minimum limit to the dimension of something. Used for having visual `order` between your widgets 

>### Wraps
the [Wrap](https://api.flutter.dev/flutter/widgets/Wrap-class.html) is a better way to manage Row and Colums, with automated systems

>### Fitted Box
[Fitted Box](https://api.flutter.dev/flutter/widgets/FittedBox-class.html) are fundamental when we are working with images, `watch the video`

### Others
- [Safe Area](https://api.flutter.dev/flutter/widgets/SafeArea-class.html) check if your widgets are not visible 
- [Clip Rect](https://api.flutter.dev/flutter/widgets/ClipRRect-class.html) can round everything 
- with the [Align](https://api.flutter.dev/flutter/widgets/Align-class.html) you can free align everything you want
---

# Pub Dev
[Pub Dev](https://pub.dev/) holds all the package maded from the community, some examples.

- [Another Flushbar](https://pub.dev/packages/another_flushbar) customizable Snackbars
- [Arc Text](https://pub.dev/packages/flutter_arc_text) visualize text's in a circle
- [Dio](https://pub.dev/packages/dio) powerful Http client for Dart
- [Flutter Chart](https://pub.dev/packages/fl_chart) every type of chart
- [Google Maps](https://pub.dev/packages/google_maps_flutter) provides a widget with Google Maps
- [Image Picker](https://pub.dev/packages/image_picker) from gallery or from photo
- [Motion Tab Bar](https://pub.dev/packages/motion_tab_bar) and  [Bottom Navy Bar](https://pub.dev/packages/bottom_navy_bar) are beautiful bars
- [Share](https://pub.dev/packages/share) helps you to share things
- [Shared Preferences](https://pub.dev/packages/shared_preferences) key-value autosaved in memory
- [URL Launcher](https://pub.dev/packages/url_launcher) helps on opening URL's