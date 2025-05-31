## Container - Widget
```
import 'package:flutter/material.dart';

void main() {
  runApp(MaterialApp(
    home: Scaffold(
        appBar: AppBar(
          title: Text('Hello Appbar'),
        ),
        body: Container(
          padding: EdgeInsets.all(20),
          margin: EdgeInsets.all(25),
          decoration: BoxDecoration(
              color: Colors.amber,
              border: Border.all(
                  color: Colors.grey, width: 2, style: BorderStyle.solid),
              // borderRadius: BorderRadius.circular(10.0),
              borderRadius: BorderRadius.only(
                  topLeft: Radius.circular(10),
                  bottomLeft: Radius.circular(20),
                  topRight: Radius.circular(10),
                  bottomRight: Radius.circular(10)),
              boxShadow: [
                BoxShadow(
                  color: Colors.grey,
                  offset: Offset(0, 0),
                  blurRadius: 10,
                  spreadRadius: 5,
                )
              ],
              gradient: LinearGradient(
                  colors: [Colors.blue.shade50, Colors.blue.shade900],
                  begin: Alignment.topLeft,
                  end: Alignment.bottomCenter,
                  stops: [0.5, 0.5])),
        )),
  ));
}

```