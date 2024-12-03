# demo
## 1

```
import 'package:flutter/material.dart';
import 'package:flutter/services.dart';
import 'package:flutter_svg/flutter_svg.dart';
void main() {
  runApp(const NiLuoPage());
}

class NiLuoPage extends StatelessWidget {
  const NiLuoPage({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        // Root widget
        home: Scaffold(
            appBar: AppBar(
              title: const Text("小尼诺"),
            ),
            body: Center(
                child: Column(children: [
              Column(children: [
                Container(
                  child: Text("安全统筹"),
                ),
                Row(children: [
                  Container(color: Colors.red,),
                  Container(color: Colors.red,),
                  Container(color: Colors.green,),
                  Container(color: Colors.green,)
                ],),
              ]),
              Row(children: [
                Text("HELLO"),
              ]),
              Row(children: [
                Text("HELLO"),
              ]),
            ]))));
  }
}
```