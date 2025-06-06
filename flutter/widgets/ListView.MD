## ListView - Widget
Example 1:
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

Example 2:
```
import 'package:flutter/material.dart';

final countries = [
  'Bangladesh',
  'India',
  'Pakistan',
  'Nepal',
  'Bhutan',
  'Maldive'
];

List<Widget> helloList() {
  return countries.map((country) => Text(country)).toList();
}

void main() {
  runApp(MaterialApp(
    home: Scaffold(
        appBar: AppBar(
          title: Text('Hello Appbar'),
        ),
        body: ListView(children: [
          ...helloList(),
          SizedBox(height: 50),
          Text('Another Text'),
        ])),
  ));
}

```
Example 3: ListView.builder
```
import 'package:flutter/material.dart';

final countries = [
  'Bangladesh',
  'India',
  'Pakistan',
  'Nepal',
  'Bhutan',
  'Maldive'
];

void main() {
  runApp(MaterialApp(
    home: Scaffold(
        appBar: AppBar(
          title: Text('Hello Appbar'),
        ),
        body: ListView.builder(
          padding: EdgeInsets.all(5.0),
          itemCount: countries.length,
          itemBuilder: (context, index) => ListTile(title: Text(countries[index])),
        )),
  ));
}

```