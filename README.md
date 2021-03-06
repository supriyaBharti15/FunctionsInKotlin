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
    //Print Results will be like 
    userDetails(id = 123,name = "supriya")
```
## Extension Function in Kotlin 
```kotlin
 val inputs = "I      am        a Programmer"
        println("Result:: ${replaceWhiteSpace(inputs)}")
        println("Result::"+inputs.replaceWhiteSpaceEx())
```
```Kotlin
//Create a function to replace the white space :: normal use case 
    fun replaceWhiteSpace(inputs: String): String {
        var regex = Regex("\\s")
        return regex.replace(inputs, " ")
    }
```
```Kotlin
 // Extension of above method
    fun String.replaceWhiteSpaceEx():String{
        val regex = Regex("\\s+")
        return regex.replace(this," ")
    }
```
## infix function in Kotlin
```Kotlin
z//create two obj of MyHeader class
        val obj1 = MyHeader("H1")
        val obj2 = MyHeader("H2")
        val result = obj1 plus obj2 // after adding the infix keyword before the function
        val result = obj1.plus(obj2) // normal way to do 
        println(result.name)
//Create a class
    class MyHeader(var name: String) {}

     fun MyHeader.plus(other: MyHeader): MyHeader {
        return MyHeader(this.name + other.name)
    }
    infix fun MyHeader.plus(other: MyHeader): MyHeader {
        return MyHeader(this.name + other.name)
    }
```
```kotlin
//fibonacci series 1,1,2,3,5,8,13,21
    private fun printFabonacci(limit: Int) {
        var prevNum = 0
        var currentNum = 1
        var sum: Int
        for (i in 1..limit) {
            println(currentNum)
            sum = prevNum + currentNum
            prevNum = currentNum
            currentNum = sum
        }
```
## with and apply
```kotlin
val m = Meeting()
        //1: set value to class
        m.time = "12 jan"
        m.title = "Kotlin Example"
        m.where = "India"
        println("SUP ${m.title}") // Output :: Kotlin Example
        
        //2: set value to class
        with(m){
            m.time = "15 jan"
            m.title = "Java Example"
            m.where = "India"
        }
        println("SUP ${m.title}") // Output :: Java Example
        
        //3: set value to class
        m.apply {
            m.time = "12 jan"
            m.title = "Python Example"
            m.where = "India"
        }
        println("SUP ${m.title}") // Output :: Python Example

    }

    class Meeting {
        var title = ""
        var time = ""
        var where = ""
    }
```
