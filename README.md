# Function in Kotlin 
- Don't need to be part of a class.
- Introduced with 'fun' keywords.
- Can have default parameters.
- Can have named parameters.
- Can 'extend' existing type.

## Syntax of Function
```Kotlin
//with return type and parameters...
Syntax :- fun [nameOfFunction] (parametersName : Type,parameterName : Type,...) : [return type if any] {}
Actual :- fun addTwoNum(num1: Int, num2: Int): Int {}
Example:-
fun addTwoNum(num1: Int, num2: Int): Int {
        val sum = num1 + num2
        return sum
    }
//Print the result 
 println("Result == ${addTwoNum(12, 12)}")
```
```Kotlin
//with parameters no returns 
Syntax :- fun [nameOfFunction] (parametersName : Type,parameterName : Type,...) {}
Actual :- fun addTwoNum(num1: Int, num2: Int) {}
```
