## RichText - Widget
```
import 'package:flutter/material.dart';

void main() {
  runApp(MaterialApp(
    home: Scaffold(
      appBar: AppBar(
        title: Text('Hello Appbar'),
      ),
      body: Center(
        child: RichText(
            text: TextSpan(text: 'Hello', children: [
          TextSpan(
              text: ' World of',
              style: TextStyle(fontSize: 30.0),
              recognizer: TapGestureRecognizer()
                ..onTap = () {
                  print('You Tapped');
                }),
          TextSpan(
              text: ' Jurassic Park',
              style: TextStyle(color: Colors.lightGreen, fontSize: 25.0)),
        ])),
      ),
    ),
  ));
}

```