# Matlab

- Operator: + - * / ^

- Result is computed,and displayed as **ans**

- Precedence rules:

> - Left-to-right within a precedence groups

> - Precedence groups are(highest first)

> > 1. Parenthesis()

> > 2. Power(^)

> > 3. Multiplication and Division(*,/)

> > 4. Addition and subtraction(+,-)   

<br>

## Variables

Variables do NOT need to be declared before assignment

A single "equal" sign (=) is the assignment operator

Upper case and Lower case are different.

Variable names can begin with character but not a number



## Special Variables and Constants

#### Use "iskeyword" to look up.

ans

i , j : complex number

Inf

exp : 2.2204e-016

NaN : not a number

pi

#### MATLAB Calling Priority

1. Variable

2. Built-in function

3. Subfunction

4. Private function

   MEX-file

   P-file

   M-file

   

   ``clear variable``

#### Numeric Display "Format"

short

long

shortE

longE

bank : Currency format with 2 digits after the decimal point

hex

rat : Ratio of a small integers



## Command Line Terminal

#### Obverse the equation

a=10;

a=10

#### Some functions 

``clc`` : clear command window display

``clear`` : remove all variables in the workspace

``who`` : variables in the workspace 

``whos ``: variables information of the workspace 



## Array(Vector and Matrix)

- **Row vector**

  \>\> ``a =[1 2 3 4]``

- **Column vector**

  \>\> ``b=[1;2;3;4]``

- Try

  \>\> ``a*b``

  \>\> ``b*a``

- Key in the following matrix in MATLAB

  \>\>`` arr = [1 2 3; 4 5 6; 7 8 9]``



## Array Indexing 

- Select a certain subset of elements inside a matrix

  a = [1 21 6; 5 17 9; 31 2 7]

- <font color="blue">what's the answer from MATLAB after typing ?</font>

  \>\> ``a(8)``

  \>\> ``a([1 3 5])``

  \>\> ``a([1 3;1 3])``

  \>\> ``a(3,2)``

  \>\>`` a([1,3],[1,3])``



Colon Operator

- Want to create a long array: A = [1 2 3 ... 100]

  \>\> A=[1:100]

- Want to create a long array: A = [1 3 ... 99]

  \>\> A=[1:2:99]



Some Special Matrix

eye(n)

zeros(n1,n2)

ones(n1,n2)

diag() : diagonal matrix



## Script Flow

- Typically scripts run from the first line to the last
- Structured programming techniques(subroutine,loop,condition,etc) are applied to make the program look neat.



### low Control

if <font color="red"><strong> condition1</strong> </font>

<font color="blue"><strong> 			statement1</strong> </font>

​	

elseif <font color="red"><strong> condition2</strong> </font>

​	<font color="blue"><strong> 		statement2</strong> </font>

else

​	<font color="blue"><strong> 		statement3</strong> </font>

end



### Relational(Logical) Operator

<

<=

\>

\>=

==

~=

&&

||



Pre-allocating Space to variables

- In the previous example, we do not pre-allocate space to vector a rather than letting MATLAB resize it on every iteration

- Which method is faster? 

  ``tic``

  ``for ii=1:2000``

  ​	``for jj=2000``

  ​		``a[ii,jj]=ii+jj;``

  ​	``end``

  ``end``

  ``toc`` 



Tips for Script Writing

- At the beginning of your script, use command
  - clear all 
  - close all



Exercise 

- Write a function that asks for a temperature in degrees Fahrenheit

- Compute the equivalent temperate in degrees Celsius

- Show the converted temperates in degrees Celsius

- The function should keep running until no number is provided for conversation

- You may use these functions:

  input, isempty, break, disp, num2str



Function Default Variables

inputname: Variable name of function inut

mfilename: File name of currently running function

nargin: Number of function input arguments

nargout: Number of function output arguments

varargin: Variable length input argument list

varargout: Variable length output argument list