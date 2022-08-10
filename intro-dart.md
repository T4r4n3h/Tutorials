# Intro to Dart Language
// this is a comment in dart
## Variables:

```dart
void main() {
  int age = 30;
  String name = "Tara";
  bool isFemale = true;
  dynamic maturity = "Can change in the futute";
  List names = ["Tara", "Britteny","
  
  print ('hello');
}
```
## Functions
below is the automatic function that Dart will start 
functions have a type and that is what it is meant to return 
Arrow functions work the same way as JS if the logic fits into one line


```dart
void main() {
 ...
}
// OR:

void main() {
    print('something');
    String greet = greeting();
    
}
String greeting(){
        return "Hello";
    }
String greeting() => "Hello";

```
## List 
*List*s in Dart  are like Arrays in JavaScript. 
```dart
 void main() {
  
  List names = ["chun-li", "Tara", "yoshi", "mario"];
  names.add("lucy");
  names.remove("yoshi");
  names.add(30); //this is doable but not best practice 
  
  print(names);
 
 }
```
it is *Best Practice* to declare the *type of List* like below 

```dart
void main() {
  
  List<String> names = ["chun-li", "Tara", "yoshi", "mario"];
  names.add("lucy");
  names.remove("yoshi");
  names.add(30); //Now this will be an error
  
  print(names);
 
}
```
## Classes
Blue print for an object by giving them *properties* and *methods*.
```dart
class User {
  String userName = "mario";
  int age = 25;
  
  void login(){
    print('user logged in');
    
  }
}
```
this does not create anything is just a model for our object
in order for it to create a user we have to invoke (instantiating a Class) it like so:
```dart
void main() {
  User userOne = User();
  print(userOne.username);
  print(userOne.age);
  userOne.login();

  User userTwo = User();
  print(userTwo.username);
}

class User {
  String username = "Mina";
  int age= 65 ;
 
  void login(){
    print('user logged in');
    
  }
}

```
the code above is going to create every user with the same username and age so in order to create a user with different property we use a *Constructor* like below: 

#### *Constructor:*
it is a method(function) that runs at the time of instantiation and allows us to overrides values. 
```dart
void main() {
  User userOne = User("Tara", 45);
  print(userOne.username);
  print(userOne.age);
  userOne.login();
 User userTwo = User("Mina", 65);
  print(userTwo.username);
  print(userTwo.age);
}

class User {
  String username;
  int age;
 
  User ( String Banana, int foo){//Constructor 
   this.username = Banana;
   this.age = foo;
   
  }
   
   
  void login(){ // Method
    print('user logged in');
    
  }
}
```
#### *Inheritance*
when we have a class that inherits from another class *(Super Class)*
in the example below. the SuperUser is an inherit class:
```dart
  User userOne = User("Tara", 45);
  print(userOne.username);
  print(userOne.age);
  userOne.login();
  User userTwo = User("Mina", 65);
  print(userTwo.username);
  print(userTwo.age);
  
  SuperUser userThree = SuperUser ("yoshi", 40);
  print(userThree.username);
  userThree.publish();
}

class User {
  String username;
  int age;
 
  User(this.username, this.age){//Constructor 
  
   
  }
   
   
  void login(){ // Method
    print('user logged in');
    
  }
}
class SuperUser extends User {// this is an inheriance 
  SuperUser(String usename, int age) : super(usename, age);
  
  void publish(){//this is only for superUser
    print ('published update');
  }
}
```


