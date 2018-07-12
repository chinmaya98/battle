import 'package:flutter/material.dart';

void main() {
  runApp(MaterialApp(
    home: MyApp(),
  ));
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        //padding: const EdgeInsets.only(top: 16.0),
        theme: ThemeData(primaryColor: Colors.cyan),
        home: Scaffold(
          appBar: AppBar(
            title: Text(
              'Welcome to Battle of Stats',
            ),
          ),
          body: Center(
            child: new Center(
              child: Column(
                crossAxisAlignment: CrossAxisAlignment.center,
                // padding: const EdgeInsets.only(top: 16.0),
                children: [FirstScreen(), textSection()],
              ),
            ),
          ),
        ));
  }
}

class FirstScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Container(
        padding: const EdgeInsets.only(top: 180.0),
        child: new Center(
            child: Row(mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                // Add Column here:
                children: [
              new IconButton(
                icon:
                    new Icon(Icons.play_arrow, color: Colors.cyan, size: 30.0),
                onPressed: () {
                  Navigator.push(
                    context,
                    MaterialPageRoute(builder: (context) => PlayScreen()),
                  );
                },
              ),
              new IconButton(
                icon: new Icon(Icons.lightbulb_outline,
                    color: Colors.cyan, size: 30.0),
                onPressed: () {
                  Navigator.push(
                    context,
                    MaterialPageRoute(builder: (context) => LearnScreen()),
                  );
                },
              ),
            ])));
  }
}

class PlayScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Play"),
      ),
      body: Center(
          child: new Center(
              child: Column(mainAxisAlignment: MainAxisAlignment.spaceEvenly,
                  // Add Column here:
                  children: [
            RaisedButton(
              onPressed: () {
                Navigator.push(
                  context,
                  MaterialPageRoute(builder: (context) => Easy()),
                );
              },
              child: Text('Easy'),
            ),
            RaisedButton(
              onPressed: () {
                Navigator.push(
                  context,
                  MaterialPageRoute(builder: (context) => Medium()),
                );
              },
              child: Text('Medium'),
            ),
            RaisedButton(
              onPressed: () {
                Navigator.push(
                  context,
                  MaterialPageRoute(builder: (context) => Difficult()),
                );
              },
              child: Text('Difficult'),
            ),
            RaisedButton(
              onPressed: () {
                Navigator.pop(context);
              },
              child: Text('Go back!'),
            ),
          ]))
          /** child: RaisedButton(
          onPressed: () {
            Navigator.pop(context);
          },
          child:Text('Go back!'),
        ),**/
          ),
    );
  }
}

class LearnScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Learn"),
      ),
      body: Center(
        child: RaisedButton(
          onPressed: () {
            Navigator.pop(context);
          },
          child: Text('Go back!'),
        ),
      ),
    );
  }
}

Widget textSection() {
  return Container(
    padding: const EdgeInsets.all(32.0),
    child: new Center(
      child: Text(
        '''This game is Awesome to play''',
        softWrap: true,
      ),
    ),
  );
}

class Easy extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Easy Game"),
      ),
      body: Center(
        child: RaisedButton(
          onPressed: () {
            Navigator.pop(context);
          },
          child: Text('Go to Play Screen'),
        ),
      ),
    );
  }
}

class Medium extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Medium Game"),
      ),
      body: Center(
        child: RaisedButton(
          onPressed: () {
            Navigator.pop(context);
          },
          child: Text('Go to Play Screen'),
        ),
      ),
    );
  }
}

class Difficult extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Difficult Game"),
      ),
      body: Center(
        child: RaisedButton(
          onPressed: () {
            Navigator.pop(context);
          },
          child: Text('Go to Play Screen'),
        ),
      ),
    );
  }
}
