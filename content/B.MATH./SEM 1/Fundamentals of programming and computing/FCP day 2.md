---
date: 28-7-25
duration: 2 hr
prev: "[[FCP day 1]]"
next: "[[FCP day 3]]"
---
###### Parsing of the last code
1. **Pre-pocessor.** The pre-processor `gcc`, usually integrated with the compiler, takes in any `#` command called *directives* and makes appropriate changes to the program.
2. **Compiler.** A program that converts high level language code to machine language code.
3. **Linker.** This links the main program with the machine code.
A C-program always features headers, functions, etc. 

###### Directives
Directives are things referred to the preprocessor, by using a `#` symbol. No need to distinguish it with a semicolon or any other marker.

###### Functions
This is the thing, the main thing of all C programs. These are also called "procedures" and "subroutines". These are parts of code which execute complete actions. Every C program has to have one function: the `main` function. It has to be called exactly that `main` and not anything else. Functions can return stuff or may even not. Main, when returns, returns to the operating system.

###### Printing strings
The `printf()` function prints *string literals*. 

###### Comments
Comments are purely for people who deal with the source code of the program. The C format looks like `/* ... */` and one can put any amount of text inside that would be ignored during compiling. C-99 allows single line comments that do not require closings, as `//` and it takes that entire line to be a comment.

#### Variables and assignment
Data, permanent or temporary, needs to be stored somewhere. The memory block where any particular type of data can be stored, is called a **variable**.

###### Data types
Different types of data carry different amount of data based on how "rich" or "heavy" they are. A variable of type `int` stores integers between certain limits, `float` stores fractions, i.e. integers with digits after decimal point.

###### Declaration
Variables have to be declared before using, so that the compiler makes room for them in memory. This is a statement, and has to end with a semicolon.

###### Assignments
After a variable has been declared, values are to be assigned to them, since that's what they are made from. This is also a statement so should end with a semicolon as well. 

###### Printing for a variable value
Here the `printf()` function comes in, and it takes in a string literal placed inside `"..."`. So if we are to refer to some variable in a print command, we use something called *placeholders*, with are of the form `%_`, takes in an abbreviation of a datatype, and refer to a variable of that type with comma after the string literal `"..."`. 
**Note.** `printf("whatever %.2f",float_var);` prints the float only up to two digits after decimal place.

###### Initialisation
Some variables are initialised to various values whenever they are declared. To prevent that, we could just initialised it to some value ourselves. In C jargon the usual initialisation (mainly to prevent data and memory corruption) is `8` for numerical values.

###### Reading inputs
Sometimes it is required to input some data from the user. The standard function for that is `scanf()`. The `f` in both `printf()` and `scanf()` stands for *formatting*. Vaguely, what happens here is the functions need formatted strings to decide on the way the data input is taken in and how it is displayed. 
A standard statement using the `scanf` function looks like `scanf("%d", &var);`. Here the data input is a decimal integer stored in the variable `var`. The `&` tells the compiler to store the data at the *address* of the variable involved. The user input has to end with certain keys, mainly `enter`, also sometimes `tab`.

###### Macro definition
Instead of defining every constant data in the `main()` function, some data can be defined *globally* in the preprocessor region. One usual instance would be `#define SPECIAL_VALUE 420`. No semicolons or other stuff, just the preprocessor requirements. The regular convention with macro definition is to name the variable in all caps, and...though not a requirement in any way, is better followed. Notice we do not even need datatypes for macros.

###### Identifiers
These are just names of variable. It can be made up of letters, digits, underscores, but there are certain rules that the name can only start with a letter or an underscore. So they cannot start with a number. The usual convention has come to it that all main variables are named with small letters with underscores only and the macros are all caps. One can also use multi-word names, and separate the words by capitalising the middles. 

###### Keywords
There are certain strings that are part of the syntax of C and cannot be used as identifiers. There is a whole list of them not worth remembering.

###### Tokens
Tokens are parts of statements that cannot be broken down into smaller meaningful and independent units, like the name of a variable, or some keyword or other command.

###### Spaces
Spaces make it easier to distinguish between tokens. It is just a matter of readability. 