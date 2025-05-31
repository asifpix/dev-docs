## Container - Widget
```
import 'package:flutter/material.dart';

List<String> countries = [
  'Bangladesh',
  'India',
  'Pakistan',
  'Nepal',
  'Bhutan',
  'Maldive'
];
//
var countryList = ...countries.map((country) => Text(country)).toList();

void main() {
  runApp(MaterialApp(
    home: Scaffold(
        appBar: AppBar(
          title: Text('Hello Appbar'),
        ),
        body: ListView(children: [
          ...countries.map((country) => Text(country)).toList(),
          SizedBox(height: 50),
          Text('Another Text'),
        ])),
  ));
}

```