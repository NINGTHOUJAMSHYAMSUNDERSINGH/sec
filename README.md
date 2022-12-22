import 'package:flutter/material.dart';

// ignore: camel_case_types
class secondPage extends StatefulWidget {
  const secondPage({super.key});

  @override
  State<secondPage> createState() => _SecondPageState();
}

class _SecondPageState extends State<secondPage> {
  List<String> name = [];
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      floatingActionButton: FloatingActionButton(
        child: const Icon(Icons.add),
        onPressed: () {  
       showDialog(context: context,
           builder: (context)
           builder:(context) {
            return AlertDialog()
             
           }{

  );
            name.add("Value");
            setState(() {});
          },
        ),
      ),
      appBar: AppBar(
        title: const Text("Second Page"),
      ),
      body: name.isNotEmpty
          ? ListView.builder(
              itemCount: name.length,
              itemBuilder: (context, index) {
                return ListTile(
                  title: Text("${index + 1}:${name[index]}"),
                );
              },
            )
          : const Center(child: Text("NO Users")),
    );
  }
}
