## GridView - Widget
Example:
```
import 'package:flutter/material.dart';

final countries = [
  'Bangladesh',
  'India',
  'Pakistan',
  'Nepal',
  'Bhutan',
  'Maldive',
  'Myanmar'
];

void main() {
  runApp(MaterialApp(
    home: Scaffold(
        appBar: AppBar(
          title: Text('Hello Appbar'),
        ),
        body: GridView.builder(
          gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(crossAxisCount: 3),
          padding: EdgeInsets.all(5.0),
          itemCount: countries.length,
          itemBuilder: (context, index) => Card(
            margin: EdgeInsets.all(20.0),
            child: Center(
              child: Text(countries[index]),
            ),
          ),
        )),
  ));
}

```
We must add "gridDelegate: SliverGridDelegateWithFixedCrossAxisCount(crossAxisCount: 3),". Here crossAxisCount will define the column number of the grid.