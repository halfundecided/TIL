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
 
