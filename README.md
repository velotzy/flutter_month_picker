# Flutter Month Picker

Flutter month picker package lets you to choose month and year only and implement in your app.

## Installation

1. Add the latest verstion of package to your pubspec.yaml

```yaml
dependencies:
  flutter_month_picker: ^0.0.1
```

2. Run

```
    flutter pub get
```

3. Import the package and use it in your Flutter app.

```
import 'package:flutter_month_picker/flutter_month_picker.dart';
```

## Example

<hr>

<table>
<tr>
<td>

```dart
class FlutterMonthPicker extends StatelessWidget {
  const FlutterMonthPicker({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: TextButton(
          onPressed: () async {
            final date = await showMonthPicker(
              context: context,
              initialDate: DateTime.now(),
              firstDate: DateTime(2000),
              lastDate: DateTime(2050),
            );
            log(date.toString());
          },
          child: const Text('Open Month Picker'),
        ),
      ),
    );
  }
}
```

</td>
<td>
<img  src="https://user-images.githubusercontent.com/53579386/126896556-911d4778-04cd-49bf-b32a-01a6eb3b0155.jpeg"  alt="">
</td>
</tr>
</table>

## Next Goals

- [ ] More customization like: size, color, textstyles, localizaton, platform.
- [ ] Implentation of lcoalization.
- [ ] Cross-platform (Android and IOS) UI.
