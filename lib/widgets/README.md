# Widgets Folder

## Overview

The Widgets Folder is dedicated to housing reusable components. These components are designed to be versatile and can be used across various parts of the app, ensuring a consistent and efficient development process.

## Folder Structure

- **widgets/**
  - `custom_button.dart`
  - `custom_tile.dart`
  - `loading_indicator.dart`
  - ...

The Widgets Folder contains Dart files, each representing a reusable UI component. These components are meant to be generic and adaptable for use in multiple contexts within the app.

## Guidelines for Using the Widgets Folder

1. **Reusability:** Focus on creating components that can be reused in different parts of the application. Reusable widgets reduce code duplication and improve consistency.

2. **Generic Inputs:** Design widgets to accept generic inputs rather than inputs specific to a particular use case. This approach increases the flexibility and applicability of the widget.

3. **Avoiding Specific Models as Parameters:** When creating widgets like a custom tile, avoid accepting a specific model as a parameter. Instead, use individual properties that the widget will display. This makes the widget more adaptable to various contexts.

4. **Descriptive Naming:** Use descriptive and clear naming for widgets, reflecting their purpose and functionality. For example, `custom_button.dart` for a customizable button widget.

5. **Organized Code:** Organize the widget code for readability and maintainability. Use comments and structure the code in a way that makes it easy to understand and modify.

## Example

If you are creating a custom tile widget for displaying user information, instead of passing a `User` model directly, pass individual properties like `title`, `imageUrl`, and `description`. This way, the custom tile can be easily reused for other types of content by passing different properties.

## Advantages of Using the Widgets Folder

- **Code Reusability:** Promotes the reuse of UI components, reducing the need to write new code for similar functionalities.
- **Consistency:** Helps maintain a consistent look and feel across the app, as the same widgets are used in multiple places.
- **Efficiency:** Increases development efficiency by providing a library of pre-built, versatile components.