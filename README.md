# BASICS-OF-OOP
## How Objects Were Introducted?
- Back in the day, primitive data types were used to store single and simple values. 
- **Eg:**
  - Byte
  - Int 
  - Float 
  - Boolean etc 
- However, when programmers wanted to group similar pieces of data together, primitive data types were of no use then.
- **Eg:** 
  - You are a developing a car racing game and you want to program a car into the game. 
  - You will need to define plenty of variables such as color, speed, position and a boolean to define whether it won or lost the game.
  - Now, you will need each of these variables for each car in the game. 
  - Each of which will contain different data.
  - Now it will be easy, if you could group each of these variables related to one car together. 
  - So that you can deal with them as one entity.
- This is when, **STRUCTURES** in C were introduced. 
### Structures
- Structures allow programmers to store data of different data types together, which is not the case with Arrays. 
  - So, you can store all the pieces of data related to the car in a single structure.
  - You can also store all the car structures together in one structure that represents all of the cars.
![image](https://user-images.githubusercontent.com/88162824/215736969-00f3f81a-b04d-4a9a-b511-5848ee6dc848.png)
#### Limitation of Structures
- You cannot define function within a structure.
- With reference to car racing game example, this prevents you from defining a function related to the cars. 
- This is where **OBJECT ORIENTED PROGRAMMING CAME ALONG**.
### Objects
- Objects allow you to group differnt data types together and define and store functions (known as methods in objects) within an object. 
- EG:
```js
//Object of one individual car
var car1 = {
    name: "Toyota",
    color: "red",
    move: function() {
        return ....;
    }
}

//Object of second individual car
var car2 = {
    name: "Audi",
    color: "white",
    move: function() {
        return ....;
    }
}
```
- As you can see above, there is a lot of duplicated code between both objects. The move() function appears in each object. 
- Since we want the same information for each car, we can use objects and classes instead.
- Grouping related information together to form a class structure makes the code shorter and easier to maintain.
## Classes
- Classes are essentially user-defined data types. 
- Classes are where we create a blueprint for the structure of methods and attributes. 
- Individual objects are instantiated from this blueprint.
  - In our Car Racing game class example, attributes include name & color, while methods include move().
  - In the car racing example, here’s how a programmer could think about organizing an OOP:
    1. Create a class for all cars as a blueprint of information and behaviors (methods) that all cars will have, regardless of type. 
    2. Create objects from the  class that represent car.
- EG:
```js
class Car {
    constructor(name, color) {
        this.name = name;
        this.birthday = color;
    }
    move() {
        //calculate movement
        return ...
    }
    
}

//instantiate a new object of the Car class, and individual car named car1
const car1 = new Car("Toyota", "blue");
```

