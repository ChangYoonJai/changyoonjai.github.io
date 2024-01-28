---
title: "[Flutter] "
categories:
  - Flutter
tags:
  - Dart
  - Flutter
---

## References

[Official Tutorial](https://flutter-ko.dev/docs/cookbook/persistence/reading-writing-files)

## File I/O

### Dependencies

Add "path_provider" dependcy in pubspec.yaml

```yaml
dependencies:
  flutter:
    sdk: flutter
  path_provider:
```

### Assets a.k.a Resources

#### Add Assets (pubspec.yaml)

Add reousres files or directories in pubspec.yaml

```yaml
flutter:
  assets:
    - assets/test.json
    - assets/
```

#### Access Assets (.dart)

```dart
import 'dart:async' show Future;
import 'package:flutter/services.dart' show rootBundle;

Future<String> loadAsset(var path) async {
  return await rootBundle.loadString(path);
}

// usage sample
loadAsset('assets/test.json')
              .then((value) => ...);
```

- - -

## TBU from here

### Import

```dart
import 'dart:io';
import 'package:path_provider/path_provider.dart';

Future<String> get _localPath async {
  final directory = await getApplicationDocumentsDirectory();

  return directory.path;
}
```

