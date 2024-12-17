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

TODO: Put a short description of the package here that helps potential users
know whether this package might be useful for them.

## Features

TODO: List what your package can do. Maybe include images, gifs, or videos.


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
 