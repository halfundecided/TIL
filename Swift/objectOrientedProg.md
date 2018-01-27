### OOP: Object Oriented Programming on Swift

#### Class 
- like a blueprint

#### Object
- like an actual product 
1. Properties
  + `let colour = red`
  + `let numberOfSeats = 5`
  + if it goes to outside of the class, it's constants/variables
2. Methods (Action) 
  + `func drive() { moveForwards}
  + if it goes to outside of the class, it's functions 
3. Events 
  + onStart() { drive() }

#### Example
````swift
class Question {
    
    // Properties of the class
    let questionText : String
    let answer : Bool
    
    // Events
    // initialization method
    init(text: String, correctAnswer: Bool){
        questionText = text
        answer = correctAnswer
    }
````

#### why MVC?
1. Provides structure
2. Recognisable by third parties 
3. Code Reuse
4. Multitasking

