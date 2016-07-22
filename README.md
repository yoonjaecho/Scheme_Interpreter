# Scheme_Interpreter

Scheme Interpreter with python depending on Cute16.

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

( ( lambda ( x ) ( + x 1 ) ) 100 )
( ( lambda ( x ) ( + x ( ( lambda ( y ) ( + y 1 ) ) 1 ) ) ) 1 )
( define plus1 ( lambda ( x ) ( + x 1 ) ) )
( plus1 3 )
( define plus2 ( lambda ( x ) ( + ( plus1 x ) 1 ) ) )
( plus2 9 )
( define cube ( lambda ( n ) ( define sqrt ( lambda ( n ) ( * n n ) ) ) ( * ( sqrt n ) n ) ) )
( define foo ( lambda ( x y ) ( define goo ( lambda ( x ) ( * 2 x ) ) ) ( * ( goo x ) y ) ) ) 
( cube 5 )
( foo 5 3 )
( define quadra ( lambda ( n ) ( define cube ( lambda ( n ) ( define sqrt ( lambda ( n ) ( * n n ) ) ) ( * ( sqrt n ) n ) ) ) ( * ( cube n ) n ) ) )
( quadra 5 )
( define lastitem ( lambda ( ls ) ( cond ( ( null? ( cdr ls ) ) ( car ls ) ) ( #T ( lastitem ( cdr ls ) ) ) ) ) )
( lastitem ' ( 1 2 3 ) )
lastitem
cube
( define length ( lambda ( ls ) ( cond ( ( null? ls ) 0 ) ( #T ( + 1 ( length ( cdr ls ) ) ) ) ) ) )
( length ' ( 1 2 3 4 5 ) )
( ( lambda ( a b ) ( + a b ) ) 24 5 )
( define a ( + 1 2 ) )
a
( define fact ( lambda ( n ) ( cond ( ( = n 0 ) 1 ) ( #T ( * n ( fact ( - n 1 ) ) ) ) ) ) )
( fact 3 )
( define plus1 ( lambda ( x ) ( + x 1 ) ) )
( plus1 3 )
( define x 1 )
( plus1 x )
