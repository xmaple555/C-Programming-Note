# Overview
This note is intented to help the students taking the NTUST EMI course ET3405302 to quickly understand C Programming and mathematics in English. 

[Hackmd Link](https://hackmd.io/@oViyvE1kTJmMinrhoK7HCg/ryViX2Wxo)

## References
* [C Tutorial - W3Schools](https://www.w3schools.com/c/)
* [Mathematical English (a brief summary)](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwiahcqc-Zn6AhUMfN4KHSh_DfcQFnoECBAQAQ&url=https%3A%2F%2Fwebusers.imj-prg.fr%2F~jan.nekovar%2Fco%2Fen%2Fen.pdf&usg=AOvVaw2kpr1mc7trlu9bzDfuPlzl)

# C Programming

## Basic Syntax
```clike=
#include <stdio.h>

int main() 
{
  printf("Hello World!");
  return 0;
}
```

`#include <stdio.h>` , a hash `#` followed by the string `include`,  tells the C compiler to include the header file `header.h` for `printf` function. The angle bracket `<>` is used to include files for the C standard library.

The main function is the first function to be executed when the program begins running.

All code between the open brace bracket <code>&#123;</code> and close bracket <code>&#125;</code> will be executed. 

A semicolon `;` is used at the end of all the instructions.

`printf` function outputs the string `Hello World!` inside the two double quotations `" "` .

`return 0` ends the main function and returns the value 0.




## New lines
```clike=
printf("Hello World!\n");
```
A backward slash followed by n `\n` is used to insert a new line.



## Comments
We can use comments to explain code to make it more readable. All comments will be ignored and not be executed.



### Single-line Comments
```clike=
// This is a single-line comment.
printf("Hello World!");
```
Single-line comments begin with two forward slashes `//`.


### Multi-line Comments
```clike=
/* Here is 
           multi-line comment. */
printf("Hello World!");
```
Multi-line comments start with a forward slash followed by an asterisk `/*` and end with an asterisk followed by a forward slash `*/` .



## Variables
Variables are used to store data values.


```clike=
int myNum = 15;
```
We create a variable of type `int` and assign the value 15 to it. 



### int
`int`, short for integer, is a signed integer number without decimals, such as 45, -45. The bytes number of `int` is 4. 


### unsigned int
Compared to `int` , `unsigned int` only stores data values from zero to positive numbers.  The bytes number of `unsigned int` is 4.


### float
`float` is a single-precision floating point value that can hold up to 7 decimal digits, such as 1.12, -0.3.  The bytes number of `float` is 4.


### double
`double` is a double-precision floating point value. Compared to `float`, `double` can hold up to 15 decimal digits.  The bytes number of `double` is 8.


### long double
Compared to `double`, `long double` can express more precise. On the x86 architecture, most C compilers store `long double` as 12 bytes or 16 bytes, but Microsoft Visual C++ defines `long double` as same as `double` .

### char
`char`, short for character, is used to store a single character. Each `char` occupies one byte.


Unlike many other programming languages, C doesn't have a string type. However, we can declare an array of characters or a `char` pointer to make a string. 



#### Null Character
Null character, a backslash followed by zero`'\0'`, is included at the end of a string to specify where the string ends.



### void
`void` is a special type that indicates nothing or no type. When `void` is used as a function type, it will not return any values.



## Type Casting
Type Casting is a method that converts one data type into another. To convert a variable's type, type a new data type inside the parenthesis `()` followed by the variable's name.

```clike=
int sum = 17, count = 5;
double mean;

mean = (double) sum / (double)count;
printf("Value of mean : %f\n", mean );
```
When the above example is executed, it produces the answer `3.4`.

It should be noted here that the answer would be 3 if we didn't convert the sum's type.


## Printf Format String
```clike=
int myNum = 5; 
printf("%d", myNum);
```
The printf format string, percent d inside two double quotations`"%d"`, will output the integer value of myNum.

Printf format string, also known as format specifier, starts with a percent symbol `%` to print a variable's value . To print different types, use percent c `%c` for char, percent s `%s` for string ,and percent f `%f` for float.


## Constants
```clike=
const int myNum = 15; 
myNum = 10;
```
When we don't want the variable to be modified the value after its declaration, use the keyword `const` before the type of the variable.

The second line causes the error `expression must be modified`.



## Operators
Operators are used to perform mathematical calculations on variables.


```clike=
int myNum = 100 + 50;
```
We use the plus operator `+` to perform the expression `100 + 50` to initialize the variable myNum.


### Arithmetic Operators

| Operator           | Expression | Description       |
| ------------------ | ---------- | ---------------- |
| `+` Addition       | `x + y`    | x plus y         |
| `-` Subtraction    | `x - y`    | x minus y        |
| `*` Multiplication | `x * y`    | x times y        |
| `/` Division       | `x / y`    | x divided by y   |
| `*` Modulus        | `x % y`    | x modules y      |
| `++` Increment     | `x ++`     | increment x by 1 |
| `--` Decrement     | `x --`     | decrement x by 1 |

### Assignment Operators
```clike=
int myNum = 10;
```
We use the assignment operator `=` to assign the value 10 to myNum.



```clike=
int x = 10;
x += 5;
```
In the second line, we use the addition assignment operator `+=` to increase the value x by 5 .


### Comparison Operators
```clike=
int x = 5;
int y = 3;
printf("%d", x > y);
```
We use the greater than operator `>` to find out if x is greater than y.




| Operator | Expression | Description                     |
| -------- | ---------- | ------------------------------- |
| `==`     | `x == y`   | x is equal to y                 |
| `!=`     | `x != y`   | x is not equal to y             |
| `>`      | `x > y`    | x is greater than y             |
| `<`      | `x < y`    | x is less than y                |
| `>=`     | `x >= y`   | x is greater than or equal to y |
| `<=`     | `x <= y`   | x is less than or equal to y    |

### Logical Operators
Logical Operators are used to calculate the boolean value of statements.




| Operator                                       | Name        | Description (In English)                     |
| ---------------------------------------------- | ----------- | -------------------------------------------- |
| `&&` (two ampersands)                          | Logical and | Return true if all the statements are true   |
| <code>&#124;&#124;</code> (two vertical lines) | Logical or  | Return true if one of the statements is true |
| `!` (exclamation mark)                         | Logical not | Reverse the boolean value of the statement   |

## If Statement
The `if` statement allows us to check a certain condition. If the condition is true, we can do one thing, and if the condition is false, we can do another thing. Usually, we use an open brace bracket`{` and close bracket`}`to enclose the block of code to be executed.



```clike=
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if the condition1 is false and condition2 is true
} else {
  // block of code to be executed if the condition1 is false and condition2 is false
}
```

If `condition1` is evaluated to be true, the first block of code will be executed.

To specify the two conditions, we use the `if` followed by the`else if`. The `else if` will be executed if the `if` statement is evaluated to be false.

When all the conditions are false, the third block of code will be executed.




```clike=
int num1 = 10 , num2 =5 , maxnum;
if (num1 > num2){
    maxnum = num1;
}else{
    maxmum = num2;
}
printf("The maximum number is %d.\n",maxmum);
```
In the first line, we create the three variables num1 , num2 ,and maxmum with assigning the value 10 and 5 respectively to the first two variables but without initializing maxnum.

If the condition `num1 is greater than num2` is true, maxnum is set to be num1. And if the condition is false, the program skips the third line and moves on to the fifth line.



## Switch
Instead of writing many `if` statements, we can use the `switch` statement.



```clike=
char grade = 'A';
switch(grade){
    case 'A':
        printf ("The grade is A.\n");
        break;
    case 'B':
        printf ("The grade is B.\n");
        break;
    case 'C':
        printf ("The grade is C.\n");
        break;
    case 'D':
        printf ("The grade is D.\n");
        break;  
    default:
        printf ("Not found any matched cases.\n");
}
```
In the above example, we put the grade in the parenthesis`()` to compare the different values of each `case` to do something different.

All the `cases` end with a colon <code>&#58;</code> .

The `break` statements break out of the switch block.

The keyword `default` specifies some code to run if there is no matched case.



## While Loop
`While Loop` is used to repeat a block of code until the specified condition is not true.



```clike=
int index = 1;
while(index <= 10){
    printf("%d\n",index);
    index++;
}
```
In the above example, the first thing before doing anything in the `while loop` is to check the condition. The index value is one, so it's definitely less than ten. The program in the loop prints out the index value and a new line. In the next line, the program increases the value of the index by 1. Proceeding that, the code goes back up to the second line to do the same thing until the index is greater than 10.



## For Loop
When we know exactly how many times we want to loop through a block of code, use a `for loop` instead of a `while loop`.



```clike=
int i;
for(i=1;i<=10;i++){
    printf("%d\n",i);
}
```
In the parenthesis of the `for loop`, we have the three different statements that we need to specify instead of one in a `while loop` :

Statement 1: Set the value 1 to the variable i before executing the block of code.
Statement 2: Specify the looping condition.
Statement 3: Increment the variable i by 1 every time we go through this loop.



## Arrays
Arrays are data structures that allow us to store multiple values of the same type in a single variable.



```clike=
int myNum[] ={1, 2, 3, 4};
```
When we put an open square bracket `[` and close bracket `]` in front of the variable's name, it is going to tell the program that we declare an array variable.

Inside the curly bracket `{}`, we put many numbers and use commas `,` to separate them.



### Index
To access an array element, use its index number, the position of the element, to specify the data we want to read or write.

In C programming, we start array indices at 0: the first element is `[0]` , the second element is `[1]` , etc. 




## User Input
To get some information from a user, we can use `scanf` function.


```clike=
int myNum;
scanf("%d", &myNum);
printf("myNum is %d\n",myNum);
```
In the above example, `scanf` function will prompt us for the integer value of myNum. It is noteworthy that we need to put an ampersand`&` in front of myNum because `scanf` takes the parameter's address.



## Structures
Structures are data structures where we can store groups of data types in one single data type.



```clike=
struct MyStructure {   
  int myNum;           
  char myLetter;       
}; 
MyStructure instance1;
instance1.myNum = 10;
```
In the first four lines, we put a `int` type alongside a `char` type to define the structure `MyStructure`. After this, we create an instance of `MyStructure` structure. 

To access the structure members, use a dot `.` after the instance's name. 



## Pointers
While a process is running, the process has its own virtual memory in which all the data values of the process are stored.



```clike=
int myNum = 10; 
printf("%d", myNum);  //10
printf("%p", &myNum); //0x7ffe077e7fd4
```
To get the variable's address, use the reference operator `&` before the variable's name.

In the above example, we can see that myNum's address is 0x7ffe077e7fd4. &myNum is a pointer that points to myNum.

A pointer is a variable that stores the memory address of another variable as its value.


```clike=
int myNum = 10;
int* pmyNum = &myNum;
printf("%p\n", pmyNum);  //0x000000B47638F5F4
printf("%p\n", &myNum);  //0x000000B47638F5F4
printf("%d\n", *pmyNum); //10
printf("%d\n", myNum);   //10
```
In the second line, we create the pointer pmyNum that points to the variable myNum. pmyNum holds myNum's address, and we can see that pmyNum's value is equal to myNum's address.

In the fifth line, we use the dereference operator `*` to get the value of the address that pmyNum holds

The dereference operator `*` is opposite to the reference operator `&` : we can get a variable's address by using `&` and get a value of the address that a pointer points to by using `*` .



## Functions
A function is a block of code that only runs when it is called. We can pass data, also known as parameters, into a function.



```clike=
#include <stdio.h>
void myFunction(int myNum) {
  printf("The number is %d\n", myNum);
}

int main() {
  myFunction(10); 
  return 0;
}
```

In the above example, we declare the function `myFunction` of `void` type with a parameter to print out the number we pass. To call the function, we just need to type out the function's name and the argument inside the parenthesis `()` .



### Recursion

In C programming, when a function calls itself then the process is known as recursion. The process allows us to make algorithms easier to be implemented, but it may be a little difficult to trace the function while debugging. Also, we need to be careful to define an exit condition, otherwise it will go into an infinite loop. 


The factorial of n equals the product of n with the next smaller factorial:

$$\begin{align*}
n! &=n\times(n-1)\times(n-2)\times\dots\times3\times2\times1\\
&=n\times(n-1)!
\end{align*}$$


```clike=
int factorial(int i) {
   if(i <= 1) {
      return 1;
   }
   return (i * factorial(i - 1));
}
int i = 5;
printf("Factorial of %d is %d\n", i, factorial(i)); //Factorial of 5 is 120
```
Using the recursion technique, we can simplify the factorial function: return 1 when i is less than or equal to 1, otherwise return the parameter i times its function of i minus 1.


## Scope Rules
Scope Rules tell C program that if a variable is accessible at certain regions.


### Local Variables
Local variables are declared inside a function or a block. They can only be used by code in the same function or block of code.


### Global Variables
Global Variables are accessible by any functions after their declarations. Usually, we declare on top of the program. 


```clike=
#include <stdio.h>
int myGlobalNum = 10;

void myFunction(){
    printf("The global number is %d\n",myGlobalNum);
    printf("The local number is %d\n",myLocalNum);
}

int main(){
    int myLocalNum = 5;
    myFunction();
}
```
In the above example, we declare a global variable and a local variable. The global variable can be accessed in `myFunction` function, but the local variable can only be used in the main function, so the fifth line causes the error `undeclared identifier`. 



# Mathematics

## Arithmetic

### Integers

| Expression        | In English                                       |
| ----------------- | ------------------------------------------------ |
| $$-245$$          | minus two hundred and forty-five                 |
| $$22,731$$        | twenty-two thousand seven hundred and thirty-one |
| $$1,000,000$$     | one million                                      |
| $$56,000,000$$    | fifty-six million                                |
| $$1,000,000,000$$ | one billion                                      |

### Fractions (Rational Numbers)
| Expression         | In English               |
| ------------------ | ------------------------ |
| $$1\over2$$      | one half                 |
| $$1\over3$$      | one third                |
| $$1\over4$$      | one quarter , one fourth |
| $$1\over5$$      | one fifth                |
| $$-1\over17$$    | minus one seventeenth    |
| $$3\over8$$      | three eights             |
| $$26\over9$$     | twenty-six ninths        |
| $$2\frac{3}{7}$$ | two and three sevenths   |

### Real Numbers
| Expression      | In English                                 |
| --------------- | ------------------------------------------ |
| $$-0.067$$      | minus nought point zero six seven          |
| $$81.59$$       | eighty-one point five nine                 |
| $$-2.3 · 10^6$$ | minus two point three times ten to the six |
| $$4 · 10-3$$    | four times ten to the minus three          |

### Complex Numbers
| Expression                    | In English                                                     |
| ----------------------------- | -------------------------------------------------------------- |
| $$3 + 4i$$                    | three plus four i                                              |
| $$1 - 2i$$                    | one minus two i                                                |
| $$\overline{1 - 2i}= 1 + 2i$$ | the complex conjugate of one minus two i equals one plus two i |

### Basic arithmetic operations
| Expression                        | In English                                                       |
| --------------------------------- | ---------------------------------------------------------------- |
| $$3 + 5 = 8$$                     | three plus five equals (= is equal to) eight                     |
| $$3-5=-2$$                        | three minus five equals minus two                                |
| $$3·5 = 15$$                      | three times five equals fifteen                                  |
| $$3/5 = 0.6$$                     | three divided by five equals zero point six                      |
| $$(2-3)·6+1=-5$$                  | two minus three in brackets times six plus one equals minus five |
| $$\frac{1-3}{2+4}= -\frac{1}{3}$$ | one minus three over two plus four equals minus one third        |
| $$4!$$                            | four factorial                                                   |
| $$a \equiv b\ (\textrm{mod}\ m)$$ | a is congruent to b modulo m                                     |

### Exponentiation, Roots
| Expression        | In English                                     |
| ----------------- | ---------------------------------------------- |
| $$5^2$$           | five squared                                   |
| $$5^3$$           | five cubed                                     |
| $$5^4$$           | five to the (power of) four                    |
| $$5^{-1}$$        | five to the minus one                          |
| $$5^{-2}$$        | five to the minus two                          |
| $$\sqrt{3}$$      | the square root of three                       |
| $$\sqrt[3]{64}$$  | the cube root of sixty four                    |
| $$\sqrt[5]{32}$$  | the cube root of sixty four                    |
| $$(1+2)^{(2+2)}$$ | one plus two, all to the power of two plus two |
| $$e^{\pi i}=-1$$  | e to the (power of) pi i equals minus one      |


## Algebra
### Algebraic Expressions
| Expression               | In English                                                                                     |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| $$A=a^2$$                | capital a equals small a squared                                                               |
| $$a = x + y$$            | a equals x plus y                                                                              |
| $$b = x - y$$            | b equals x minus y                                                                             |
| $$c = x · y · z$$        | c equals x times y times z                                                                     |
| $$c = xyz$$              | c equals x y z                                                                                 |
| $$(x + y)z + xy$$        | x plus y in brackets times z plus x y                                                          |
| $$x^2+y^3+z^5$$          | x squared plus y cubed plus z to the (power of) five                                           |
| $$x^n+y^n=z^n$$          | x to the n plus y to the n equals z to the n                                                   |
| $$(x-y)^{3m}$$           | x minus y in brackets to the (power of) three m ;<br/> x minus y, all to the (power of) three m |
| $$2^xx^3$$               | two to the x times three to the y                                                              |
| $$ax^2+ bx + c$$         | a x squared plus b x plus c                                                                    |
| $$\sqrt{x}+\sqrt[3]{y}$$ | the square root of x plus the cube root of y                                                   |
| $$\sqrt[n]{x+y}$$        | the n-th root of x plus y                                                                      |
| $${a+b}\over{c+d}$$      | a plus b over c minus d                                                                        |
| $$\dbinom{n}{r}$$        | (the binomial coefficient) n over r                                                            |

### Indices
| Expression                                 | In English                                                                                                              |
| ------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------- |
| $$x_0$$                                    | x zero; x nough                                                                                                         |
| $$x_1 + y_i$$                              | x one plus y                                                                                                            |
| $$R_{ij}$$                                 | (capital) R (subscript) i j; <br/> (capital) R lower i                                                                  |
| $$M^k_{ij}$$                               | (capital) M upper k lower i j ; <br/> (capital) M superscript k subscript i                                             |
| $$\sum_{i=0}^{n}$$                         | sum of a i x to the i for i from nought (zero) to n ; <br/> sum over i (ranging) from zero to n of a i (times) x to the |
| $$\prod_{m=1}^{\infty}b_m$$                | product of b m for m from one to infinity <br/> product over m (ranging) from one to infinity of b                      |
| $$\sum_{j=1}^{n} a_{ij}b_{ij}$$            | sum of a i j times b j k for j from one to n; <br/> sum over j (ranging) from one to n of a i j times b j               |
| $$\sum_{i=0}^{n} \dbinom{n}{i}x^iy^{n-i}$$ | sum of n over i x to the i y to the n minus i for i from nought (zero) to n                                             |



## Functions

### Formulas/Formulae
| Expression               | In English                                      |
| ------------------------ | ----------------------------------------------- |
| $$f(x)$$                 | f of x                                          |
| $$g(x, y)$$              | g of x (comma) y                                |
| $$h(2x, 3y)$$            | h of two x (comma) three y                      |
| $$sin(x)$$               | sine x                                          |
| $$cos(x)$$               | cosine x                                        |
| $$tan(x)$$               | tan x                                           |
| $$arcsin(x)$$            | arc sine x                                      |
| $$arccos(x)$$            | arc cosine x                                    |
| $$arctan(x)$$            | arc tan x                                       |
| $$sinh(x)$$              | hyperbolic sine x                               |
| $$cosh(x)$$              | hyperbolic cosine x                             |
| $$tanh(x)$$              | hyperbolic tan x                                |
| $$sin(x^2)$$             | sine of x squared                               |
| $$sin(x)^2$$             | sine squared of x; sine x, all squared          |
| $${x+1}\over{tan(y^4)}$$ | x plus one, all over over tan of y to the four  |
| $$3^{x-cos(2x)}$$        | three to the (power of) x minus cosine of two x |
| $$exp(x^3+y^3)$$         | exponential of x cubed plus y cubed             |

### Intervals
| Expression | In English                                                     |
| ---------- | -------------------------------------------------------------- |
| $$(a,b)$$  | open interval a b                                              |
| $$[a, b]$$ | closed interval a b                                            |
| $$(a, b]$$ | half open interval a b (open on the left, closed on the right) |
| $$[a, b)$$ | half open interval a b (open on the right, closed on the left) |


## Greek Letters

### Lowercase Greek Letters
| Expression                  | In English | Expression     | In English |
| --------------------------- | ---------- | -------------- | ---------- |
| $$\alpha$$                | alpha      | $$\beta$$    | beta       |
| $$\gamma$$                | gamma      | $$\delta$$   | delta      |
| $$\epsilon\,\varepsilon$$ | epsilon    | $$\zeta$$    | zeta       |
| $$\eta$$                  | eta        | $$\theta$$   | theta      |
| $$\iota$$                 | iota       | $$\kappa$$   | kappa      |
| $$\lambda$$               | lambda     | $$\mu$$      | mu         |
| $$\nu$$                   | nu         | $$\xi$$      | xi         |
| $$\omicron$$              | omicron    | $$\pi$$      | pi         |
| $$\rho$$                  | rho        | $$\sigma$$   | sigma      |
| $$\tau$$                  | tau        | $$\upsilon$$ | upsilon    |
| $$\phi$$                  | phi        | $$\chi$$     | chi        |
| $$\psi$$                  | psi        | $$\omega$$   | omega      |

### Uppercase Greek Letters
| Expression   | In English | Expression | In English |
| ------------ | ---------- | ---------- | ---------- |
| $$\Delta$$   | Delta      | $$\Theta$$ | Theta      |
| $$\Lambda$$  | Lambda     | $$\Xi$$    | Xi         |
| $$\Pi$$      | Pi         | $$\Sigma$$ | Sigma      |
| $$\Upsilon$$ | Upsilon    | $$\Phi$$   | Phi        |
| $$\Psi$$     | Psi        | $$\Omega$$ | Omega      |
| $$\Gamma$$   | Gamma      |            |            |
