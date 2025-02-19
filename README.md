# Tugas-Week-5
KTM 
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Kartu Tanda Mahasiswa',
      theme: ThemeData(

        colorScheme: ColorScheme.fromSeed(seedColor: const Color.fromARGB(255, 188, 0, 0)),
        useMaterial3: true,
      ),
      home: const MyHomePage(title: 'Telkom University'),
    );
  }
}

 

class MyHomePage extends StatefulWidget {
  const MyHomePage({super.key, required this.title});

  final String title;

  @override
  State<MyHomePage> createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  int _counter = 0;

  void _incrementCounter() {
    setState(() {

      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {

    return Scaffold(
      appBar: AppBar(

        backgroundColor: Colors.redAccent,

        title: Text(widget.title),
      ),
      body: Center(

        child: Column(
          mainAxisSize: MainAxisSize.min,
          children: <Widget>[
            Image.asset('profil/fotodiri.jpg',
              height: 200,
              width: 150,
            ),
            Text(
              'Muhammad Arief Faruq Wafdan',
              style: TextStyle(fontSize: 18, color: Colors.black),
            ),
            Text(
              '103012400246',
              style: TextStyle(fontSize: 18, color: Colors.black),
            ),
            Text(
              'S1 Informatika',
              style: TextStyle(fontSize: 18, color: Colors.black),
            ),
            Icon(
             Icons.audiotrack,
             color: Colors.green,
             size: 30.0,
            ),
          ],
        ),
      ),
        floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ),
    );
  }
}
