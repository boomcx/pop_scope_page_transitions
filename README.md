<!--
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/tools/pub/writing-package-pages).

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/to/develop-packages).
-->

Keeping the system's `PopScope` widget, is simpler and more efficient.


<p align=center><img src="https://github.com/boomcx/will_pop_demo/blob/main/demo.gif?raw=true" alt="demo.gif" width="30%"  /></p>



## Features

✅ You can use `PopScope` widget;

✅ Support for multiple platforms;

✅ It is the same as the default sideslip back. Takes effect only when a pop is triggered, otherwise it is cancelled;


## Usage

To use this package, add `pop_scope_page_transitions` as a dependency in your pubspec.yaml file.

[example](https://github.com/boomcx/will_pop_demo.git).


## Example

### Import the library 
```
import 'package:pop_scope_page_transitions/pop_scope_page_transitions.dart';
```

### Configure page transitions 

```dart

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Colors.deepPurple),
        useMaterial3: true,
        pageTransitionsTheme: const PageTransitionsTheme(
          builders: {
            // TargetPlatform.android: PopScopePageTransitionsBuilder(),
            TargetPlatform.iOS: PopScopePageTransitionsBuilder(),
          },
        ),
      ),
      routes: {
        '/': (context) => const HomePage(),
        '/second': (context) => const SecondPage(),
      },
    );
  }
}

```

And then, you can add `PopScope` widget in your view.
 