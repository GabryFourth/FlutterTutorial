# Expanded Widgets & FlexBox
> we can use the flexbox ***only*** on stateless object
> ***EXPANDED WIDGET DOSEN'T WORK WITH LIST***
---
## Expanded Widget
takes all the available space in the row 

![[expanded.png]]
``` dart
        child: Row(
            children: <Widget>[

                Expanded(
                    child: Container(
                        padding: EdgeInsets.all(30.0),
                        color: Colors.cyan,
                        child: Text("1"),
                    ),
                ),

                Container(
                    padding: EdgeInsets.all(30.0),
                    color: Colors.pinkAccent,
                    child: Text("2"),
                ),

                Container(
                    padding: EdgeInsets.all(30.0),
                    color: Colors.amber,
                    child: Text("3"),
                ),
                
            ],
        ),
``` 

---
## Flex Value
if we `expand` all the containers they take the same amount of space, it's the same thing as putting `flex: 1` in every widget

![](flexx.png)

with all the `containers` expanded if we assign to them a `flex` value, the higher flex value takes most space

![](flexother.png)

every flex widget takes `flex_value/sum_of_all_flex_value` as a space, for example the first widget below takes 3/6 of space, the second is 2/6 of space, last one 1/6 of space
``` dart
        child: Row(
            children: <Widget>[

                Flexible(
                    flex: 3,
                    child: Container(
                        padding: EdgeInsets.all(30.0),
                        color: Colors.cyan,
                        child: Text("1"),
                    ),
                ),

                Flexible(
                    flex: 2,
                    child: Container(
                        padding: EdgeInsets.all(30.0),
                        color: Colors.pinkAccent,
                        child: Text("2"),
                    ),
                ),
                
                Flexible(
                    flex: 1,
                    child: Container(
                        padding: EdgeInsets.all(30.0),
                        color: Colors.amber,
                        child: Text("3"),
                    ),
                ),

            ],
        ),
``` 

