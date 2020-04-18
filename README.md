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

//Example
    private fun subTwoNum(num1: Int, num2: Int) {
        val result = num1 - num2
        println("Result== $result")
    }
```
```Kotlin
//function with no returns and no parameters
    private fun display(){
        println("Hello World..")
    }
```
```Kotlin
//Function Expression
    fun findMax(num1: Int, num2: Int): Int = if (num1 > num2) num1 else num2
    //print result 
    println("Max is== ${findMax(23,32)}")
```
## Named Parameters
```Kotlin
    fun userDetails(name: String, id: Int) {
        println("Name = $name and ID = $id")
    }
```

