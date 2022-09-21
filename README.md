# onpressed-text-show-in-flutter
onpressed-text-show-in-flutter
import 'package:flutter/material.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(CustomAPP());
}

class CustomAPP extends StatefulWidget {
  @override
  State<CustomAPP> createState() {
    return _CustomAPPState();
  }
}

class _CustomAPPState extends State<CustomAPP> {
  String fullName = "";
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      color: Colors.pinkAccent,
      home: Scaffold(
        appBar: AppBar(
          title: Text("statejful"),
        ),
        body: Material(
          child: Column(
            children: [
              TextField(
                decoration: InputDecoration(
                  hintText: "enter name",
                  labelText: "name",
                ),
                onSubmitted: (String name) {
                  setState(() {
                    fullName = name;
                  });
                },
              ),
              Padding(padding: const EdgeInsets.all(17), child: Text(fullName)),
            ],
          ),
        ),
      ),
    );
  }
}
