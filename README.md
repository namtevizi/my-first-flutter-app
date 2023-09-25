# The Fundermentals of Flutter 
## Flutter Commands

```bash
$ flutter doctor
$ flutter upgrade
$ flutter --help --verbose
$ flutter --version
$ flutter help <command>
```

```bash
$ flutter create <new-app-name>
$ flutter analyze
$ flutter test
$ flutter run lib/main.dart
$ flutter run <DART_FILE>
```

```bash
$ flutter drive
$ flutter emulators
$ flutter screenshot
$ flutter logs
$ flutter install -d <DEVICE_ID>
```

```bash
$ flutter pub get
$ flutter pub outdated
$ flutter pub upgrade
```

Refer to https://docs.flutter.dev/reference/flutter-cli

## Dart Basics
### 1. Data Types
In Dart, every value we use in the program will have a data type either number or string should be known when we compile the code. Following are some common data types:

   1. String: String variables store text values.
   2. Num: Num Data type refers to number. Dart has two kinds of numerical values:
`Integer`
`Double`
  3. Boolean: It utilizes the “bool” keyword for representing the Boolean values true and false.
  4. Object: In Dart, everything is an object, but a thing can be more difficult.

### 2. Variables
Variables are defined as the namespaces that store values. The names of the variables are known as identifiers. Variables are the data containers that can store the value of any data type. For example:

`var myAge = 10;`

In the above example, “myAge” is the variable that holds the integer value 10.

### 3. Operators
Dart programming language supports all the operators available in the other programming languages like Java, C, C#. Following are the operators of Dart:

> Equality
> Arithmetic
> Logic
> Increment and Decrement
> Comparison.

### 4. Loops and Decision Making
Decision-Making statements are the features that enable us to determine the condition before the instructions are implemented. Dart programming language supports the below decision-making statements:

> If-else statement
> If Statement
> Switch Statement.

We use Loops for executing a code block repeatedly until a particular condition becomes true. Dart programming language supports the following loop statements:

`while`
`for`
`for..in`
`do-while`

### 5. Functions
Functions are another essential feature of any programmiThisg language. They are statements that carry out a particular task. They are arranged into the building blocks of the code that are maintainable, reusable, and readable. The function declaration includes the return type, parameters, and function name.

[ Check out: Flutter vs React Native ]

### 6. Comments
Comments are defined as non-executable code lines. They are one of the primary aspects of all programming languages. Dart programming supports the following kinds of comments:

Block Comments: It is the multi-line comment(/*...*/)
Make format comments: It is the single-line comment(//)
Doc comment: It is the document comment that we use for types and member(///).

### 7. “Continue” statement
The continue statement enables us to jump the rest of the code in the loop and instantly go to the later loop iteration.

```
void main() { 
  for (int i = 1; i <= 10; i++) { 
    if (i == 5) { 
      print("Hello"); 
      continue; //it will skip the rest statement
    }
    print(i);
  }
}
```

### 8. “Break” statement
The break statement allows us to stop the existing flow of the program and consistent execution after the loop body.

```
void main() { 
  for (int i = 1; i <= 10; i++) { 
    if (i == 5) { 
      print("Hello"); break;//it will terminate the rest statement
    }
    print(i); 
  }
}
```

### 9. “Final” statement
We use the Final statement for restricting the user. We can use it in various perspectives like classes, methods, and variables. 

### 10. “Const” keyword
We use the “Const” keyword for declaring the constants. After announcing a constant, we cannot modify the value.

```
void main() {
  final a 100;
  const pi 3.14;
  print (a);
  print (pi);
}
```

### 11. Object-Oriented Programming
In Dart, everything and value is an object, so Dart is object-oriented. In Dart, a number is also an object. 

Object: Object is defined as the entity which has behavior and state. It can be logical or physical. Dart enables us to develop our custom objects for expressing complex relations between the data.

Class: Class is a group of objects. It indicates that we create objects through classes because all the objects require a blueprint according to which we can create a separate entity. The class definition contains the below things:

Methods
Fields
Getters and Setters
Constructors

```
class Mobile {
  // Property Declaration
  String color, brandName, modelName;

  // Method Creation
  String calling() {
    return "Mobile can do call to everyone.";
  }

  String musicPlay() {
    return "Mobile can play all types of Music.";
  }

  String clickPicture() { 
    return "Mobile can take pictures.";
  }
}

void main() {
  // Object Creation
  var myMob = new Mobile();
}
```

## Flutter Basics
### Flutter Widgets
In Flutter, whenever we code to build anything, it will be available in a widget. The primary purpose is to create the apps from the devices. It explains how our app view must appear with their present state and configuration. When we make any modification in the code, the widget redevelops its descriptions by computing the difference of current and previous widgets for determining the minimum changes to render in the User Interface(UI) of the application.

### Kinds of Widgets

In Dart, we can divide the Flutter Widgets into two kinds:

#### 1. Visible Widget

Visible Widgets are associated with the user output and input data. Following are the essential types of this Widget are:

- **Text**: The text widget displays text for displaying on the screen. We can coordinate with the text widget by utilizing the “textAlign” property. The style property enables us to customize the text that contains font style, font weight, letter spacing, color, font, etc.
- **Button**: This Widget enables us to carry out some action on the click. In Flutter, we cannot use the Button widget directly; instead, it utilizes a kind of buttons like a RaisedButton and a FlatButton.
- **Image**: The Image widget stores the image that can retrieve from various sources, such as from the asset folder or URL. It offers multiple constructors to load the following images:
  - Image: It is the generic image loader that ImageProvider uses.
  - File: It loads images from the system folder.
  - Asset: It loads images from the project asset folder.
  - Memory: It loads images from memory.
- **Icon**: This Widget serves as the container to store the Icon in Flutter. 

#### 2. Invisible Widget

The Invisible Widgets are associated with the control and layout of widgets. It offers controlling how widgets truly behave and how they look into the screen. Some of the essential kinds of these widgets are:

- **Column**: The Column widget is a kind of widget that organizes all the children’s widgets in the vertical alignment. It offers spacing widgets through “crossAxisAlignment” and  “main axis alignment” properties. In these properties, the cross axis is the horizontal axis, and the central axis is the vertical axis.
- **Row**: The row widget is similar to the column widget, yet it builds the widget horizontally instead of vertically. In this Widget, the cross axis is the vertical axis, and the main axis is the horizontal axis. 
- **Center**: We use this widget to center the child widget, which comes in it. 
- **Padding**: This widget covers other widgets to provide them padding in particular directions. We can offer padding in all directions.
- **Stack**: It is the important widget, which we primarily use for overlapping the widget, like a button on the background gradient.
- **Scaffold**: This widget offers the framework that enables us to insert material design elements such as Floating Action Buttons, AppBar, Drawers, etc.

### Flutter Layout
The primary concept of the layout process is widgets. Thus, the icon, image, text, and layout of our application are all widgets. Flutter enables us to create the layout by forming multiple widgets for building more difficult widgets. 

The container is the widget class that customizes the child widget. It is primarily used for adding borders, margins, padding, background color, etc. The text widget gets into the container to add the margins. The complete row is stored in the container to add margin and pad around the rows. The remaining UI is governed by the properties like text style, color, etc.

### Layout the Widget

> __Step1__: First, we have to choose the widget layout.
> 
> __Step2__: Later, create the visible widget.
> 
> __Step3__: After that, insert the widget into the layout widget.
> 
> __Step4__: Lastly, insert the widget layout to the page where we have to display it.

#### Kinds of Layout Widgets
##### 1. Single Child Widgets

Single Child Widget is a kind of widget that can store only one widget in the parent layout widget. These widgets can also include particular layout functionality. Flutter offers several child widgets for making application UI attractive. If we utilize the widgets properly, it can reduce our time and causes the app code to be readable.

- **Container**: It is the most famous layout widget that offers customizable for positioning, sizing, and painting of devices.
- **Padding**: It is the widget that we use for arranging their child widget by the provided padding. It includes “EdgeInsets.from TRB” and “EdgeInsets” for the required side we have to offer to pad.
- **Align**: It is the widget that coordinates its child widget within itself and sizes it according to the size of the child. It offers more control for placing child widgets in the exact position where we require them.
- **Center**: This widget enables us to center the child widget inside itself.
- **Aspect Ratio**: The AspectRatio allows us to hold the child widget size to a particular aspect ratio.
- **SizedBox**: This Widget enables us to provide a particular size to child widget across all the screens.
- **ConstrainedBox**: It is the widget that enables us to force further constraints on the child widget.
- **Baseline**: This widget transfers the child’s widget as per the baseline of the child.

##### 2. Multiple Child Widgets

Multiple Child Widgets are a kind of widget that includes multiple child widgets, and the layout of these widgets is distinct. For instance, the Row widget laying out of the child widget in the vertical direction.

- **Column**: It enables us to organize the child widgets in the vertical direction.
- **ListView**: It is the most famous scrolling widget that enables us to organize the child widgets one by one in the scroll direction.
- **Expanded**: It makes the children of the Row and Column widget for occupying the maximum possible area.
- **Flow**: It enables us to implement the flow-based widget.
- **Table**: It is the widget that allows us to organize its children in the table-based widget.
- **GridView**: It enables us to organize its child widgets as the scrollable, 2D array of the widgets. It contains an iterated pattern of the cells arranged in the vertical and horizontal layout.
- **Stack**: It is the important widget, which we primarily use to overlap various children’s widgets.

#### Some More Widgets
##### Flutter Row and Column
Rows and Columns are not one widget; they are two distinct widgets,  namely column, and row. We can integrate those two widgets because they have the same properties that allow us to understand rapidly and efficiently. Row and Column are two important widgets that enable us to coordinate children vertically and horizontally as per our requirements.

##### Row Widget
The Widget organizes the children in the horizontal direction on the screen. Put it differently, and it will anticipate child widgets in the horizontal array. If the child requires to fill the accessible horizontal space, we should enfold children’s widgets in the expanded widget.

The row widget does not display scrollable, yet the widgets appear in the visible view. Therefore, it is regarded wrong if we have more children in the row, which will not suit in available space. If we have to make the scrollable list of widgets. We can control the child widget of the row through the below properties:

- __Start__: It will locate the children from starting of the main axis.
- __End__: It will locate children at the end of the main axis.
- __Center__: It will locate children in the middle of the main axis.
- __spaceAround__: It will locate free space between children uniformly and half of the space before and after the first and the last children widget.

##### Column Widget
The Column Widget organizes its children in the vertical direction on screen. Put it differently, and it will anticipate the vertical array of the child widgets. If child widgets have to occupy existing vertical space, we need to enfold the children’s widgets in the expanded widget. The Column Widget does not arise scrollable because it exhibits the widget's invisible view. Therefore, it is wrong if we have more children in the column that will not suit in the accessible space. If we have to make the scrollable list of the column widgets, we have to use the “ListView” widget.

##### Flutter Buttons
Buttons are defined as the graphical control elements that offer the user to invoke the event like making choices, taking actions, searching for things, etc. We can locate the buttons anywhere in the UI, like forms, cards, toolbars, dialogs,  etc. Buttons are Flutter widgets which is a portion of the material design library. Flutter offers various kinds of buttons that contain different styles, features, and shapes. Following are the features of the buttons:

1. We can simply apply the themes to the shapes, colors, animation, and buttons.
2. We can also theme the text and icons in the button.
3. Buttons can have different child widgets for the other characteristics.

##### Kinds of Flutter Buttons

Following are the different kinds of Flutter buttons:

- **Flat Button**: It is the text label button that does not contain more decoration and is exhibited without elevation. Flat button contains two properties: 1) child 2) onPressed(). It is primarily utilized in the inline or dialogs toolbars with the content.  
- **Floating Button**: The Floating button is the circular icon button that invokes the main action in the application. It is the most frequently utilized button in nowadays applications. We can utilize this button to add, refresh or share the content.
- **Raising Button**: It is the button, which is according to material widgets and contains a rectangular body. It is the same as the flat button, yet it contains the elevation that raises when we press the button. It inserts the dimension to UI along the Z-axis. It has various properties like shape, text color, button color, padding, the color of the button.

##### Interactive Widgets
###### 1. Touch Interactions
- **AbsorbPointer Class**: A widget that absorbs pointers during the hit testing is called AbsorbPointer class.
- **Dismissible Widget**: The Dismissible widget can be dismissed by dragging it into the accused direction.
- **DragWidget**: The DragWidget receives the data when the Draggable widget is dropped.
- **Draggable**: The Draggable widget can be dragged from or to the DragTarget.
- **GestureDetector**: The GestureDetector widget detects the gestures and tries to recognize the gestures.

###### 2. Routing
- **Hero**: The Hero widget marks its child as the candidate for hero animations.
- **Navigator**: The Navigator widget handles a group of child widgets through the stack discipline.

# Upgrade your application to the latest Flutter version

To update the project to null safety follow these steps:

> Side note: change the flutter version in pubsec.yaml, make new project and copy the following line:

```
sdk: ">=2.19.6 <3.0.0"
```

Then follow the steps:

1. Run flutter upgrade in the terminal to upgrade Flutter
2. Run dart migrate to run the dart migration tool.
3. Solve all errors which the migration tool shows.
4. Run flutter pub outdated --mode=null-safety to print all outdated packages.
5. Run flutter pub upgrade --null-safety to upgrade all packages automatically.
6. Check the code for errors and solve them (Very important).
7. Run dart migrate again and it should now be successful. Follow the link to checkout the proposed changes.
8. Press the "Apply Migration" button.
9. Check the code for errors again and fix them.

## References
- https://mindmajix.com/flutter-tutorial
- https://docs.flutter.dev/release/upgrade
- https://www.felixlarsen.com/blog/update-your-flutter-project-to-flutter-20
- https://auberginesolutions.com/blog/upgrade-the-flutter-version/
- https://stackoverflow.com/questions/64797607/how-do-i-upgrade-an-existing-flutter-app
- https://codelabs.developers.google.com/codelabs/flutter-codelab-first
- https://codelabs.developers.google.com/codelabs/flutter-next-gen-uis
