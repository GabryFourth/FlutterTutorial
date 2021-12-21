# Images & Assets
---
## Network Image
image from the internet with *links*
``` dart
        child: Image(
            image: NetworkImage("https://picsum.photos/500"),
        ),
```
cleaner code for same thing
``` dart
        child: Image.network("https://picsum.photos/500"),
```

---
## Assert Image
1. create a folder called `assets` into the project like [this](2021-05-28-00-40-13.png)
2. fill it with the images you want *ex. space-1.jpg* 
3. then put the code below in the file specified 

> [picsum site](https://picsum.photos/) for getting example images

put this code into `pubspec.yaml`  
``` dart
        assets:
        - assets/space-1.jpg
        - assets/space-2.jpg
        - assets/space-3.jpg
```
or if you have only images that you need in the folder, for takeing everything inside of it
``` dart
        assets:
        - assets/
```

put this code into `main.dart` wherever you need to put the image
``` dart
        child: Image(
            image: AssetImage("assets/space-1.jpg"),
        ),
```
cleaner code for same thing
``` dart
        child: Image.assets("assets/space-1.jpg"),
```

---
## Circle Avatar
wraps an image in a circle smaller image, bigger *radius* means bigger image
``` dart
        child: CircleAvatar(
            backgroundImage: AssetImage("assets/space-1.jpg"),
            radius: 40.0,
        ),
```