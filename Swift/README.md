# iOS 11 & Swift 4

## Points vx. Pixels
- Pixels: picture elements 
- Points: 1 point = 1/72 inch
	: 72 pixels per inch 
- 2x Retina: 4 pixels per a point

## Short-cut
- command + '=' : adjust the label box size## Short-cut

## pick random number
`arc4random_uniform(6)`: pick a random number from 0 to 5

## Reference
- App icons: https://developer.apple.com/library/content/qa/qa1686/_index.html

## Comments
`//this is comment`
````swift
/*
multiple 
lines 
comments
*/
````

## Print
`print(variable)`
`print("Hello World")`

## Variables, Constants and Data Types
- Declare variable: `var myInteger : Int = 24`
- Change value: `myInteger = 25`
- Declare constant: `let myName : String = "Mijeong"`
- Example
````swift
let wholeNumbers : Int = 12
let text : String = "abc"
let booleans : Bool = true
let floatingPointNumber : Float = 1.3
let double : Double = 3.1415
let diceArray = ["dice1", "dice2", "dice3", "dice4", "dice5", "dice6"]
````

## Functions 
- Declare(create) function 
````swift
func nameOfFunction(){
...
}
````
- Call function
`nameOfFunction()`

- Declare function with input 
`func getMilk(howManyMilkCartons: Int){...}`

- Call function with input 
`getMilk(howManyMilkCartons: 4)`

- Declare function with Output 
`func getMilk(howManyMilkCartons : Int, budget : Int) -> Int {...}`


## Conditional Statements 
- if/else statement
`if Condition { ... }`

## Loops 
- basic structure
````swift
let arrayOfNumbers = [1,5,3,4,6,34,56]

for number in arrayOfNumbers {
    print(number)
}
````
- other way
  + `for number in 1...10 {...}`
  + `for number in 1..<10 {...}`
  + `for number in 1...10 where number % 2 == 0 {...}`


## Do, Catch and Try
- structure 
````swift 
do {
	try ...
} catch {
  ...
}
````
- to force run this code without throw: `try! audioPlayer = AVAudioPlayer(contentsOf: soundURL!)`
- search error code here! : www.asstatus.com
 
