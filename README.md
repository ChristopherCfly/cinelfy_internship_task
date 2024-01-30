# Flutter Project Overview

## Getting Started with Flutter

### Installing Flutter

To set up Flutter on a clean machine, follow these steps:

1. **Download Flutter SDK:** Visit the [Flutter Install](https://flutter.dev/docs/get-started/install) page and download the Flutter SDK for your operating system.
2. **Add Flutter to Path:** Extract the Flutter SDK and add the `flutter/bin` directory to your system's PATH environment variable.
3. **Run Flutter Doctor:** Open a terminal and run `flutter doctor` to check if any additional dependencies need to be installed.
4. **Add Flutter/Dart Extensions to your IDE** In Visual Studio Code there are extensions for Flutter/Dart that will add many benefits and provide a UI option for running, restarting and reloading your app without recompiling it. There are many other useful extensions that will speed up your development
***
### Creating a New Flutter Project

(this is already done for you) To create a new Flutter project, run the following command in your terminal:

```bash
flutter create my_flutter_app
```
Replace my_flutter_app with your desired project name.
***
## Project Structure Overview
This Flutter project is structured into several key folders:

### lib/: Contains the Dart source files for the app.
main.dart: The entry point of the app.

### assets/: Houses images, fonts, and other assets.
### test/: Contains unit and widget tests for the app. (this has been removed from this project)

### Features Folder: For page-specific components.
### Pages Folder: For full-page components.
### Widgets Folder: For reusable components.
### Utilities Folder: For shared functionalities.
### Constants Folder: For constant values used across the app.
For more specifics on these folder structures, refer to the document located in the corresponding folder.
***
## Basic Concepts in Flutter
### Widget Tree
In Flutter, everything is a widget. The widget tree represents the hierarchical order of widgets in the app. Widgets can be stateful (with mutable state) or stateless (immutable).

### Packages
Although in Flutter there is a very large built in [Widget Library](https://flutter.dev/docs/development/ui/widgets) that you can use to build almost any sort of user interface, we also have access to an exhaustive library of [online packages](https://pub.dev). Here you will find all the third party packages created by other developers for Dart and Flutter. It provides a rating system to help you make decisions about the most maintained and well documented packages.

To make things even easier, the Flutter team has a youtube channel which quickly highlights the use of [different widgets](https://www.youtube.com/playlist?list=PLjxrf2q8roU23XGwz3Km7sQZFTdB996iG) and [packages](https://www.youtube.com/playlist?list=PLjxrf2q8roU1quF6ny8oFHJ2gBdrYN_AK)

When loading in a new project from Github or any other source. The first step you will want to take is to load these packages into your local machine. To do this we can take advantage of our Flutter extension by selecting the pubspec.yaml file, then saving any changes to it or by using the command
```bash
flutter pub get
```
***
### VSCode Settings
In this project you will see a .vscode folder. It contains settings about how Visual Studio Code should behave in certain scenarios. The settings allow for autoformatting code on saves, quick-fixing errors on save and organising imports on save. 

These settings will speed up development, One thing to note though is due to the quick-fixing on save, Flutter's quick-fix will add const to any declared object or assigned a fixed value to save on performance.

While this is a useful feature, if you would like to go back to change this to a rely on a variable state. You will need to remove this const to prevent an error showing
***
### Entry Point: main.dart
The main.dart file is the starting point of a Flutter app. It contains the main() function and the root widget, typically a MaterialApp or CupertinoApp.

Example: Creating a Simple Stateless Widget

```dart
import 'package:flutter/material.dart';

class MySimpleWidget extends StatelessWidget {
  final String title;

  MySimpleWidget({required this.title});

  @override
  Widget build(BuildContext context) {
    return Container(
        child: Text(title)
        ,);
  }
}
```
Example: Creating a row of widgets using a layout widget that accepts a List<Widget> as its parameter

There are also layout widgets which will help for displaying more components in a row or column.
```dart
import 'package:flutter/material.dart';

class MySimpleRowWidget extends StatelessWidget {

  MySimpleRowWidget();

  @override
  Widget build(BuildContext context) {
    return Row(
        children: [
            Container(),
            Container()
                ]);
  }
}
```
***
## Dart Classes and Null Safety
Dart uses null safety to avoid null reference errors. When declaring variables, use ? for nullable types and required for named parameters in constructors.
***
## Adding Assets
To add assets like images, edit the pubspec.yaml file:

```yaml
flutter:
  assets:
    - assets/images/my_image.png

```
Then, use the asset in your widget:

```dart
Image.asset('assets/images/my_image.png', fit: BoxFit.cover)
```
***
## Running the App
To run the app, either use the play button on the extension interface (In VSCode this is visible while the main.dart is selected) **OR** use the following command:

```bash
flutter run
```
***
## Useful Resources

- [Flutter Documentation](https://flutter.dev/docs): Official Flutter documentation, covering everything from setup to advanced topics.
- [Dart Language Tour](https://dart.dev/guides/language/language-tour): A comprehensive guide to the Dart programming language, its features, and syntax.
- [Flutter Widget Catalog](https://flutter.dev/docs/development/ui/widgets): A catalog of Flutter widgets, providing an overview and examples of usage.
- [Flutter API Reference](https://api.flutter.dev/): The detailed API reference for Flutter, including classes, functions, and libraries.
