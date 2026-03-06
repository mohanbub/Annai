import 'package:flutter/material.dart';

void main() {
  runApp(AnnaiApp());
}

class AnnaiApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Foodie',
      theme: ThemeData(
        primaryColor: Colors.blue,
        accentColor: Colors.pink,
        fontFamily: 'Poppins',
        textTheme: TextTheme(
          headline6: TextStyle(color: Colors.blue, fontWeight: FontWeight.bold),
          bodyText2: TextStyle(color: Colors.black87),
        ),
        buttonTheme: ButtonThemeData(
          buttonColor: Colors.blue,
          shape: RoundedRectangleBorder(
            borderRadius: BorderRadius.circular(12),
          ),
        ),
      ),
      home: HomeScreen(),
    );
  }
}

class HomeScreen extends StatelessWidget {
  final List<Map<String, String>> restaurants = [
    {"name": "Spicy Hub", "rating": "4.5", "time": "30 min"},
    {"name": "Pizza Palace", "rating": "4.2", "time": "25 min"},
    {"name": "Veggie Delight", "rating": "4.8", "time": "20 min"},
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Discover Restaurants"),
        backgroundColor: Colors.blue,
      ),
      body: Column(
        children: [
          Padding(
            padding: const EdgeInsets.all(12.0),
            child: TextField(
              decoration: InputDecoration(
                hintText: "Search for food or restaurants",
                prefixIcon: Icon(Icons.search, color: Colors.pink),
                border: OutlineInputBorder(
                  borderRadius: BorderRadius.circular(12),
                ),
              ),
            ),
          ),
          Expanded(
            child: ListView.builder(
              itemCount: restaurants.length,
              itemBuilder: (context, index) {
                final restaurant = restaurants[index];
                return Card(
                  margin: EdgeInsets.symmetric(horizontal: 12, vertical: 6),
                  shape: RoundedRectangleBorder(
                    borderRadius: BorderRadius.circular(12),
                  ),
                  child: ListTile(
                    leading: Icon(Icons.restaurant, color: Colors.pink),
                    title: Text(
                      restaurant["name"]!,
                      style: TextStyle(fontWeight: FontWeight.bold),
                    ),
                    subtitle: Text(
                        "⭐ ${restaurant["rating"]} • ${restaurant["time"]} delivery"),
                    trailing: ElevatedButton(
                      style: ElevatedButton.styleFrom(
                        backgroundColor: Colors.pink,
                        shape: RoundedRectangleBorder(
                          borderRadius: BorderRadius.circular(8),
                        ),
                      ),
                      child: Text("Order"),
                      onPressed: () {
                        // Navigate to restaurant details
                      },
                    ),
                  ),
                );
              },
            ),
          ),
        ],
      ),
    );
  }
}
