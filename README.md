# Using the mini_app Library in Your Flutter Project

This guide explains how to add the `mini_app` library to your Flutter project using a Git URL and how to use its sample UI in your app.

## 1. Add the Dependency

In your project's `pubspec.yaml`, add the following under `dependencies`:

```yaml
dependencies:
  flutter:
    sdk: flutter
  mini_app:
    git:
      url: https://github.com/BlacMeW/mini_app.git
      ref: main
```

Then run:

```bash
flutter pub get
```

## 2. Import the Library

In your Dart file (e.g., `lib/main.dart`):

```dart
import 'package:mini_app/mini_app.dart';
```

## 3. Use the Demo Widget

Replace your `MaterialApp`'s `home` with the demo widget from the library:

```dart
import 'package:flutter/material.dart';
import 'package:mini_app/mini_app.dart';

void main() {
  runApp(const MainApp());
}

class MainApp extends StatelessWidget {
  const MainApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: MiniApp(), // This widget is provided by the mini_app library
    );
  }
}
```

## 4. Features
- Register a user
- Add credit points to users
- View total credit points

## 5. Notes
- Make sure the `mini_app` package is public and accessible from your environment.
- If you want to use only the Register User screen, you can use `RegisterUserScreen()` instead of `MiniApp()` if exported by the package.

## 6. Reference
- [mini_app GitHub Repository](https://github.com/BlacMeW/mini_app)
