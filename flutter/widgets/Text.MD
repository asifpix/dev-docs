## Text - Widget
```
import 'package:flutter/material.dart';

void main() {
  runApp(MaterialApp(
    home: Scaffold(
      appBar: AppBar(
        title: Text('Hello Appbar'),
      ),
      body: Center(
        child: Text('Hello World!',
            style: TextStyle(
              color: Colors.white,
              fontSize: 30.0,
              fontWeight: FontWeight.w700,
              decoration: TextDecoration.underline,
              wordSpacing: 5.0,
              backgroundColor: Colors.amber,
            )),
      ),
    ),
  ));
}

```