# scroll-to-index

A new Flutter package project.

## Getting Started

In the `pubspec.yaml` of your flutter project, add the following dependency:

```yaml
dependencies:
  ...
  scroll_to_index: any
```

In your library add the following import:

```dart
import 'package:scroll_to_index/scroll_to_index.dart';
```

For help getting started with Flutter, view the online [documentation](https://flutter.io/).

## Usage

This is a widget level library, means you can use this mechanism inside any Flutter widget.

for example of Flutter ListView

```
ListView(
  scrollDirection: scrollDirection,
  controller: controller,
  children: randomList.map<Widget>((data) {
    return AutoScrollTag(
      key: ValueKey(index),
      controller: controller,
      index: index,
      child: Text('index: $index, height: $height'),
      highlightColor: Colors.black.withOpacity(0.1),
    );
  }).toList(),
)

```

you can wrap any of your row widget using with variable height

```
  AutoScrollTag(
    key: ValueKey(index),
    controller: controller,
    index: index,
    child: child
  )
```

with the `AutoScrollController` controller.

for full example, please see the example folder.

## Who Uses

* [Quire](https://quire.io) - a simple, collaborative, multi-level task management tool.