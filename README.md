import 'package:flutter/material.dart';
import 'package:taskssss/screens/home_screens.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        debugShowCheckedModeBanner: false,
        home: Homescreen(),
        );
    }
}


import 'package:flutter/material.dart';
import 'package:taskssss/screens/screen2.dart';

class Homescreen extends StatefulWidget {
  const Homescreen({super.key});

  @override
  State<Homescreen> createState() => _HomescreenState();
}

class _HomescreenState extends State<Homescreen> {
  @override
  Widget build(BuildContext context) {
    return  Scaffold(
      body: SafeArea(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.spaceEvenly,
          crossAxisAlignment: CrossAxisAlignment.center,
          children: [
            const Row(
              mainAxisAlignment: MainAxisAlignment.start,
              children: [
                SizedBox(
                  width: 40,
                ),
                Text(
                  'Choose activity',
                  style: TextStyle(
                    fontSize: 18,
                    fontWeight: FontWeight.bold,
                  ),
                ),
              ],
            ),
            InkWell(
              onTap : (){
                setState(() {
                  Navigator.push(
                      context,
                      MaterialPageRoute(builder: (context) =>const screen2(
                        scrtxt2: 'Idea',
                        scricon2: Icons.lightbulb_outlined,
                      ) ,
                      )
                  );
                }
                );
              },
              child: const contrs(txt: 'Idea', iconn:Icons.lightbulb,sizedbox: 200, ),
            ),
            InkWell(
              onTap : (){
                setState(() {
                  Navigator.push(
                      context,
                      MaterialPageRoute(builder: (context) =>const screen2(
                        scrtxt2: 'Food',
                        scricon2: Icons.fastfood,
                      ) ,
                      )
                  );
                }
                );
              },
              child: const contrs(txt: 'Food', iconn: Icons.fastfood,sizedbox: 195,),
            ),
            InkWell(
              onTap : (){
                setState(() {
                  Navigator.push(
                      context,
                      MaterialPageRoute(builder: (context) =>const Screen2(
                        scrtxt2: 'Work',
                        scricon2: Icons.work,
                      ) ,
                      )
                  );
                }
                );
              },
              child: const contrs(txt: 'Work', iconn: Icons.work,sizedbox: 195,),
            ),
            InkWell(
              onTap : (){
                setState(() {
                  Navigator.push(
                      context,
                      MaterialPageRoute(builder: (context) =>const screen2(
                        scrtxt2: 'Sport',
                        scricon2: Icons.sports_basketball,
                      ) ,
                      )
                  );
                }
                );
              },
              child: const contrs(txt: 'Sport', iconn: Icons.sports_baseball_outlined,sizedbox: 190,),
            ),
            InkWell(
              onTap : (){
                setState(() {
                  Navigator.push(
                      context,
                      MaterialPageRoute(builder: (context) =>const Screen2(
                        scrtxt2: 'Music',
                        scricon2: Icons.music_note_outlined,
                      ) ,
                      )
                  );
                }
                );
              },
              child: const contrs(txt: 'Music', iconn: Icons.music_note_outlined,sizedbox: 185,),
            ),

            Row(
              mainAxisAlignment: MainAxisAlignment.end,
              children: [
                Container(
                  width: 50,
                  height: 50,
                  decoration:  BoxDecoration(
                    color: Colors.blueAccent,
                    borderRadius: BorderRadius.circular(20),
                  ),
                  child: const Icon(
                    Icons.add,
                    color: Colors.white,
                  ),
                ),
              ],
            ),


          ],
        ),
      ),
    );
  }
}

class contrs extends StatelessWidget {
  final String txt;
  final IconData iconn;
  final double sizedbox;

  const contrs({super.key, required this.txt, required this.iconn, required this.sizedbox});

  @override
  Widget build(BuildContext context) {
    return Container(
      height: 75,
      width: 300,
      alignment: Alignment.centerLeft,
      decoration: BoxDecoration(
        color: Colors.black12,
        borderRadius: BorderRadius.circular(10),
      ),
      child: Row(
        children: [
          Icon(iconn),
          const SizedBox(
            width: 5,
          ),
          Text(
            txt,
            style: const TextStyle(
              color: Colors.black,
              fontSize: 20,
              fontWeight: FontWeight.bold,
            ),
          ),
          SizedBox(
            width: sizedbox,
          ),
          const Icon(Icons.arrow_forward_ios_sharp),
        ],
      ),
    );
  }
}


import 'package:flutter/material.dart';

class screen2 extends StatelessWidget {
  final String scrtxt2;
  final IconData scricon2;
  const screen2({super.key, required this.scrtxt2, required this.scricon2});

  @override
  Widget build(BuildContext context) {
    return  Scaffold(
      body: SafeArea(
      child: Column(
      mainAxisAlignment: MainAxisAlignment.center,
      children: [
      Row(
      mainAxisAlignment: MainAxisAlignment.center,
      children: [
        Icon(scricon2,
          size: 50,
        ),
        Text(scrtxt2,
          style: TextStyle(
            fontSize: 70,
            fontWeight: FontWeight.bold,
          ),
        ),
      ],
    ),

      ],
    ),
        )
    );
    }
}
