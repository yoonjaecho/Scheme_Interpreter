# Scheme_Interpreter

Scheme Interpreter with python following Cute16 grammar.

## How to use ?

Just run this file with..

python Scheme_Interpreter.py

## About this

1. Process with "define" about variable or function.

2. Lambda function.

3. In functions, It can call global functions.

4. Scope

5. Nested function.

6. Recursion function.


### Example

( ( lambda ( x ) ( + x 1 ) ) 100 )</br>
( ( lambda ( x ) ( + x ( ( lambda ( y ) ( + y 1 ) ) 1 ) ) ) 1 )</br>
( define plus1 ( lambda ( x ) ( + x 1 ) ) )</br>
( define plus2 ( lambda ( x ) ( + ( plus1 x ) 1 ) ) )</br>
( define cube ( lambda ( n ) ( define sqrt ( lambda ( n ) ( * n n ) ) ) ( * ( sqrt n ) n ) ) )</br>
( define foo ( lambda ( x y ) ( define goo ( lambda ( x ) ( * 2 x ) ) ) ( * ( goo x ) y ) ) ) </br>
( define quadra ( lambda ( n ) ( define cube ( lambda ( n ) </br>( define sqrt ( lambda ( n ) ( * n n ) ) ) ( * ( sqrt n ) n ) ) ) ( * ( cube n ) n ) ) )</br>
( quadra 5 )</br>
( define lastitem ( lambda ( ls ) ( cond ( ( null? ( cdr ls ) ) ( car ls ) ) ( #T ( lastitem ( cdr ls ) ) ) ) ) )</br>
( lastitem ' ( 1 2 3 ) )</br>
( define length ( lambda ( ls ) ( cond ( ( null? ls ) 0 ) ( #T ( + 1 ( length ( cdr ls ) ) ) ) ) ) )</br>
( length ' ( 1 2 3 4 5 ) )</br>
( ( lambda ( a b ) ( + a b ) ) 24 5 )</br>
( define fact ( lambda ( n ) ( cond ( ( = n 0 ) 1 ) ( #T ( * n ( fact ( - n 1 ) ) ) ) ) ) )</br>
