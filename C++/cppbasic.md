# C++ Basic 

## How to compile and execute?
- Compile the program: 소스코드 작성 후 `g++ filename.cpp -o testname`
- Execute the program: `./testname`

## Default template
````cpp
#include <iostream>
using namespace std;

int main() {
	cout << "your code" << endl;
	return 0;
}
````

## Special Characters 
- `//`  : Double slash : Marks the beginning of a comment
- `#`   : Pound sign   : Marks the beginning of a preprocessor directive
- `< >` : Opening and closing brackets: Encloses a filename when used with the `#include` directive.
- `( )` : Opening and closing parentheses: Used in naming a function, as in `int main()`
- `{ }` : Opening and closing braces : Encloses a group of statements, such as the contents of a function
- `" "` : Opening and closing quotation marks: Encloses a string of characters, such as a message that is to be printed on the screen 
- `;`   : Semicolon: Marks the end of a complete programming statement

## Commom Escape Sequences
- `\n`  : Newline : Causes the cursor to go to the next line for subsequent printing
- `\t`  : Horizontal tab : Causes the cursor to skip over to the next tab stop 
- `\a`  : Alarm : Causes the computer to beep
- `\b`  : Backspace : Causes the cursor to back up, or move left one position 
- `\r`  : Return : Causes the cursor to go to the beginning of the current line
- `\\`  : Backslach : print a backslash 
- `\'`  : single quote : print a single quotation mark
- `\"`  : double quote : print a double quotation mark 

## Integer Data Types
- 2 bytes 
  + `short int`
  + `unsigned short int`
- 4 bytes   
  + `int`
  + `unsigned int`
  + `long int`
  + `unsigned long int`
- 8 bytes  
  + `long long int`
  + `unsigned long long int`
 
### `char` Data Type 
- `char letter = 'A';`
- Difference btw String and Char
  + `'A'` is stored as A (1-byte)
  + `"A"` is stored as A \0 (2-byte)

### `string` Class 
- `#include <string>` : requried for the string class 

### Floating-point Data Types 
- `float` : 4 bytes 
- `double` : 8 bytes 
- `long double` : 8 bytes 

### `bool` Data Type 
`bool true = true;`
`bool false = false;`

### Size of a Data Type
`sizeof(int);` 

### Named Constants 
`const double INTEREST_RATE = 0.069;`

### `cin` Object
: to read data typed at the keyboard
````cpp
#include <iostream>
using namespace std;

int main() {
	int length, width, area;

	cout << "Enter the length and width of the rectangle ";
	cout << "separated by a space.\n";
	cin >> length >> width;
	area = length * width;
	cout << "The area of the rectangle is " << area << endl;
	return 0;
}
````

### Exponents 
`area = pow(4.0, 2.0);`

### Type Casting 
`val = static_cast<DataType>(Value);`

### Formatting Output 
- `setw(n)`   : Establishes a print field of n spaces 
- `fixed`     : Displays floating-point numbers in fixed point notation.
- `showpoint` : Causes a decimal point and trailing zeroes to be displayed, even if there is no fractional part.
- `setprecision(n)` : Sets the precision of floating-point numbers
- `left`      : Causes subsequent output to be left justified
- `right`     : Causes subsequent output to be right justified
 
