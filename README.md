Resources
==

Android Mobile App Developer Tools https://developer.android.com/

Playground IDE  https://developer.android.com/training/kotlinplayground

Skillsoft Percipio 
  https://www.skillsoft.com/percipio-app

## In this article
 1. [ Syntax ](https://github.com/yanisapths/Kotlin-Android-Guide#1syntax)
  - 1.1 [Defining Strings](https://github.com/yanisapths/Kotlin-Android-Guide#11-defining-strings)
  - 1.2 [Null Safety](https://github.com/yanisapths/Kotlin-Android-Guide#12-null-safety)
  - 1.3 [String Operations](https://github.com/yanisapths/Kotlin-Android-Guide#13-string-operations)
   - 1.4 [Kotlin Conditionals](https://github.com/yanisapths/Kotlin-Android-Guide#14-kotlin-conditionals)
 2. [ Loops & Functions ](https://github.com/yanisapths/Kotlin-Android-Guide#2loops--functions) 
  - 2.1 [Types Checking](https://github.com/yanisapths/Kotlin-Android-Guide#21-types-checking)
  - 2.2 [Ranges](https://github.com/yanisapths/Kotlin-Android-Guide#22-ranges)
  - 2.3 [Loop creation](https://github.com/yanisapths/Kotlin-Android-Guide#23-loop-creation)
     - [while loop](https://github.com/yanisapths/Kotlin-Android-Guide#while-loop)
     - [do..while loop](https://github.com/yanisapths/Kotlin-Android-Guide#dowhile-loop)
     - [for loop](https://github.com/yanisapths/Kotlin-Android-Guide#for-loop)
  - 2.4 [When Statement](https://github.com/yanisapths/Kotlin-Android-Guide#24-when-statement)
  - 2.5 [Collections](https://github.com/yanisapths/Kotlin-Android-Guide#25-collections)
     - [Arrays](https://github.com/yanisapths/Kotlin-Android-Guide#arrays)
     - [Read-only List](https://github.com/yanisapths/Kotlin-Android-Guide#read-only-list)
     - [Mutable List](https://github.com/yanisapths/Kotlin-Android-Guide#mutable-mutablelist)
     - [Set](https://github.com/yanisapths/Kotlin-Android-Guide#set)
     - [Maps](https://github.com/yanisapths/Kotlin-Android-Guide#maps)
      
     
 Android Basics in Kotlin
   - [Unit 2: Layout](https://github.com/yanisapths/Kotlin-Android-Guide#unit-2-layouts)
    - [Classes & Inheritance](https://github.com/yanisapths/Kotlin-Android-Guide#classes--inheritance-in-kotlin)
    - [Modify classes in the hierachy](https://github.com/yanisapths/Kotlin-Android-Guide#modify-classes-in-the-hierachy)
    - [vararg](https://github.com/yanisapths/Kotlin-Android-Guide#vararg)

 1.Syntax
 ============

   1.1 Defining Strings
   --

          var name = "Cody"
          println(name)

          var firstname:String = "Codie"
          var middle:String = "Curve"
          var lastname:String = "Blackwell"
          println(firstname+" "+middle+" "+lastname)
          println(firstname[3]+" "+lastname[1]+firstname[1]+middle[3]+middle[4]+" "+middle[1])
          firstname = "James"
          println(firstname)

          //tab
          println(firstname+"\t"+lastname)

          //new line
          println(firstname+"\n"+lastname)

          //normal backslash or character
          println(firstname+"\\"+lastname)
          println(firstname+"\$"+lastname)



   1.2 Null Safety
   --
     
          var newname:String? = "John"

          firstname = null.toString()
          newname = null
          println(newname+" "+"is"+" "+firstname)

          var fname:String = "James"
          var tel:Int = 123456

          val jamesB = "Employee Tel.: = $tel"
          println("$fname , $jamesB")

          var x = 2
          var y = 4
          val sum = x+y
          println("$x plus $y is $sum or ${x + y}") 

    
    
  1.3 String Operations
  --
    
          var name1:String = "Cody Blackwell"
          var name2:String = "Martha Horowitz"
          var firstname:String = "Raj "
          var lastname:String = "Chawanda"
          
 1.1 trimMargin()

           val firstN:String = name1.trimMargin("Cody ")
           println(firstN)
           println(name1.length)
           println(name2.length)

 1.2 compareTo()

           println(name1.compareTo(name2))

 1.3 plus()

           var addNames = firstname.plus(lastname)
           println(addNames)

           var addNames2 = name1.plus(" "+name2)
           println(addNames2)

  1.4 Kotlin Conditionals
  --
     
   1. if 

         1.1 "if" statement returns value , no ternary required

                     if (x=y) z=10

         1.2 "if" can be represented as blocks

                   var z = if (x == y) {
                         println("equal")
                         x
                     } else {
                          println("not equal")
                          y
                     }

      > Standard

          if (x==y) z=1

      > Expression

          var z= if (x == y) x else y

      > Else

           if (x == y) {
               z = 1
           } else {
               z = 0
           }

     
   2. "when" similar to "switch" in C lang, but in Kotlin, it's "when"
                
                   when (x) {
                        1 -> println("x equals 1")
                        2 -> println("x equals 2")
                        else -> {
                            println("x not equal to 1 or 2")
                        }
                    }


      Working with Conditionals :

              var x = 10
              var y = 20
              var z = 10

       > Normal "if" , but "if" alone doesn't help much
                        
                      if(x == y)
                        println("$x is equal to $y") //ignored as it's not equal,(not match the statement)
                      if(x < y)
                        println("$x is less than $y")
                      if(y > z)
                        println("$y is greater than $z")
                              
   3. if..else..
                     
                     if(x == y)
                          println("$x is equal to $y") else {
                              println("$x is not equal to $y")
                          }

                      val a = if (x < y) {
                          println("a is x($x) less than y($y)")
                      } else {
                          println("a is x($x) not less than y($y)")
                          y
                      }
                   println(a)

                 
                 var x = 5
                 val y = 10
                   if(x > y)
                       println("x is greater than y") else {
                           println("x is not greater than y")
                       }
         

2.Loops & Functions
 ============

   2.1 Types Checking
   --
   
       var myVal:Any? = "yes"
       if(myVal is String){
           println("This is a string")
       } else {
           println("This is not a string")
       }
       if(myVal !is Int){
           println("This is not an Int")
           myVal = null
           println(myVal)
       }
      
   Output
      
     > If "myVal" is a string
     
         This is a string
         This is not an Int
         null
         
      > If "myVal" is an interger
      
          This is not a string
          
   2.2 Ranges
   --
   There are three ways for creating Range in Kotlin –

   - Using (..) operator
   - Using rangeTo() function
   - Using downTo() function
      
         var x:Int = 20
         var y:Int = 10
         if(x in 1..y) {
            println("In range")
         } else {
            println("out of range")
         }
         
  2.3 Loop Creation
  --
    
            for(i in 1..10) {
               print("$i, ")
            }

            println("\nCounting backward")
            for(i in 50 downTo 0) {
               print("$i, ")
            }
            println("\nStepping")
            for(i in 50 downTo 0 step 2) {
               print("$i, ")
            }
        
  Output
     
      1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 
      Counting backward
      50, 49, 48, 47, 46, 45, 44,...., 11, 10, 9, 8, 7, 6, 5, 4, 3, 2, 1, 0, 
      Stepping
      50, 48, 46, 44, 42, 40, 38, 36, 34, 32, 30, 28, 26, 24, 22, 20, 18, 16, 14, 12, 10, 8, 6, 4, 2, 0, 
         
      
#### While loop
  use a while loop to execute a block of code until the expression evaluates to false and you exit the loop.
           
           var i = 0
            while(i < 100) {
               i+=5
               print("$i, ")
            }
         
         5, 10, 15, 20, 25, 30, 35, 40, 45, 50, 55, 60, 65, 70, 75, 80, 85, 90, 95, 100, 

#### Do...while loop

         do {
            i-=5
            print("$i, ")
         } while(i > 0)
         
         95, 90, 85, 80, 75, 70, 65, 60, 55, 50, 45, 40, 35, 30, 25, 20, 15, 10, 5, 0, 
#### For loop
  use a for loop to iterate over all items of a list
     
      for (item in myList) {
        // Execute this code block for each element of the list
      }
    
  2.4 When statement
  --
  
            var choice:Int = 5
            when(choice) {
               1 -> print("It's a 1")
               2 -> print("It's a 2")
               else -> {
                  print("Not 1 or 2")
               }
            }
      
  2.5 Collections
  --
   
   Arrays
   --
    
    arrayOf()
    Array<T>
    mutable
    fixed size 
    
  Lists 
  --
   Kotlin standard library function listOf()
   
   - ## Read-only: List 
      - cannot be modified after you create it
      - "List < String >" holds a list of Strings
      - you can have a "List < Car >" that holds a list of Car object instances.
      - reversed() 
        returns a new list where the elements are in the reverse order.
      - sorted()
        returns a new list where the elements are sorted in ascending order.
            
         val numbers: List<Int> = listOf(1, 2, 3, 4, 5, 6)
        
     If the type of the variable can be guessed (or inferred), then you can omit the data type of the variable.
         
         val numbers = listOf(1, 2, 3, 4, 5, 6)
      
   - ## Mutable: MutableList 
      - can be modified after you create it, add, remove
      - you have to explicitly state the type. 
      ex. string, int, otherwise "Not enough information to infer type variable"
      
             val entrees: MutableList<String> = mutableListOf()
      - add()
      
               println("Add noodles: ${entrees.add("noodles")}")
               
      - addAll()
      
              val moreItems = listOf("ravioli", "lasagna", "fettuccine")
              println("Add list: ${entrees.addAll(moreItems)}")
              
      - remove()
      - removeAt() with an index
      - clear()
          Clear out the list
       - isEmpty()
          Check if the list is empty
  
         

----
   
    var fruit = listOf<String>("Apple", "Orange", "Banana")
    println(fruit)

   [Apple, Orange, Banana]

                  println(fruit.size)

   3

                   for(i in fruit) {
                       println(i)
                   }

   Apple
              Orange
              Banana

                  when{
                       "Banana" in fruit -> print("Banana is indeed yellow")
                   }

  Banana is indeed yellow

             var fruit:MutableCollection<String> = mutableListOf<String>("Mango","Berries","Watermelon")
             println(fruit)
             
             fruit.add("Cherries")
             println(fruit)

   [Mango, Berries, Watermelon]

   [Mango, Berries, Watermelon, Cherries]
   
   
  Set
  --
   - It's a group of related items.
   - Can't be any duplicates.
   - Order doesn't matter.
   
  Ex. there's a set of books that you've read, and reading them multiple times doesn't change the fact that it's in the set of book you've read.
    
   > From Lists to Set
   
        val books = listOf("Harry1","Harry2","Harry3", "Harry1","Harry2","Harry3")
        val setBook = books.toSet()
        println("list: ${books}\nset: ${setBook}")
        
   > Output  
   
      list: [Harry1, Harry2, Harry3, Harry1, Harry2, Harry3]
      set: [Harry1, Harry2, Harry3]
      
 #### Mutable & (Immutable) Set
   
        val set1 = setOf(1,2,3)
        val set2 = mutableSetOf(3,2,1)
      
 #### contains()
   
       println(" $s1 == $s2 : ${s1 == s2 }\ncontains 9: ${s1.contains(9)}")
      
   > Output  
 
      [1, 2, 3] == [3, 2, 1] : true
      contains 9: false

  Maps
  --
   - the keys (names) are unique, but the values (ages) can have duplicates.
   - The key doesn't get added again, but the value it maps to is updated.

          val ages = mutableMapOf<String, Int>(
            "Fred" to 30,
            "Ann" to 22
          ) 
          println(ages)
        
  #### put() 
  
        ages.put("Sam", 14)
  
  > short-hand
  
        ages["Tim"] = 12
        
    
  #### forEach
   Goes through all the items for you and performs an operation on each one.
   
   - it : an identifier of forEach that specifies the current item.

           ages.forEach {
              print("${it.key} is ${it.value}, ")
           }
         
  > Fred is 30, Ann is 22, 
  
  #### map()
   Applies a transformation to each item in a collection.
      
        println(ages.map {"${it.key} is ${it.value}"}.joinToString(", "))
   
 #### joinToString(", ") 
  Adds each item in the transformed collection to a string, separated by , and it knows not to add it to the last item.
  
       Fred is 31, Ann is 23
  
  
  #### filter()
   Returns the items in a collection that match, based on an expression.
      
       val filterNames = ages.filter{ it.key.length > 3 }
  
   > {Fred=30}
  
  Lambdas
  --
  A function with no name that can immediately be used as an expression. 
  
   - You can store functions in variables and classes, pass functions as arguments, and even return functions.
   - You can treat them like you would variables of other types like Int or String.
      
  #### Function types
  
  _function types_, where you can define a specifc type of function based on its input parameters and return value.
    
       (Int) -> Int
  
 A function with above fn type must take in a paramter of type ( Int ) , and return a value of type 'Int'.
  
> Notation 
  
  - Parameters : listed in parentheses (seperated by commas if there're multiple) 
  - Arrow -> 
    followed by
  - Return type 
     
         val triple: (Int) -> Int = {a : Int -> a * 3}
         println(triple(3))

   > a : Int ;can be ommited to 'it'
   
       val double: (Int) -> Int = { it * 2 }
       
 
  #### Higher-order functions
  
   - _map, filter, forEach_  are examples of higer-order functions beacuse they took a function as parameter.
    
         val names = listOf("Fred", "Ann", "Barbara", "Joe")
         println(names.sortedWith { str1: String, str2: String -> str1.length - str2.length })
       
       The last expression in the lambda is the return value. 
       In this case, it returns the difference between the length of the first string and the length of the second string, which is an Int. 
       ##### sortedWith()  
       Outputs a list where the names will be in order of increasing length.
    
 > Output 

    [Ann, Joe, Fred, Barbara]

#### OnClickListener and OnKeyListener in Android
  
 SAM (Single-Abstract-Method) : the shortened version of the code is possible.
          
 ![image](https://user-images.githubusercontent.com/72002605/178110046-914f2989-6a50-4456-bf21-1642549224c3.png)   
   
   You just need to make sure the lambda function type matches the function type of the abstract function.
   Since the view parameter is never used in the lambda, the parameter can be omitted.  
     
 
 ##### OnKeyListener
  the abstract method has the following parameters 
  
           onKey(View v, int keyCode, KeyEvent event)   
           
  You can pass in a lambda to setOnKeyListener().
      
        costOfserviceEditText.setOnKeyListener { view, keyCode, event -> handleKeyEventr(view,keyCode) }
  
 > Note: If you don't use a lambda parameter in the function body, you can name it _
 
      costOfServiceEditText.setOnKeyListener { view, keyCode, _ -> handleKeyEvent(view, keyCode) }
  
---------------------------------------------------------------------------------------------------------------------------

Android Basics in Kotlin : Reference
============

- https://developer.android.com/courses/android-basics-kotlin/course

- https://developer.android.com/training/kotlinplayground

Unit 2: Layouts
============

   Classes & Inheritance in Kotlin
   ----

   > buildingMaterial cannot be given a value, so use "abstract" to indicate that it is not going to be defined here.
        
            abstract class Dwelling(private var residents:Int){
                abstract val buildingMaterial:String
                 abstract val capacity:Int

                 fun hasRoom(): Boolean {
                   return residents < capacity
                 }
             }
         
         
   > When you declare abstract functions, it's like a promise to give them values and implementations later, 
       any subclass needs to implement the function body 
        
           class SquareCabin(residents:Int):Dwelling(residents){
                 override val buildingMaterial = "Wood"
                 override val capacity = 6
             }

            val squareCabin = SquareCabin(6)
             println("Material: ${squareCabin.buildingMaterial}")
  
  
  Simplified code
  
       : with(instancename){ operations..}
         
            with(squareCabin){
                 println("\nSquare Cabin\n===========")
                 println("Capacity: ${capacity}")
                 println("Material: ${buildingMaterial}")
                 println("Has room? ${hasRoom()}")
             }
  
       
      Square Cabin
      ============
      Capacity: 6
      Material: Wood
      Has room? false
      
    
Open 
--
  
  By default, "classes are final" and cannot be subclaased. Only allowed to inherit from "abstract" classes or classes that are marked with the "open" keyword. 
      
         open class RoundHut(residents:Int): Dwelling(residents) {
            override val buildingMaterial = "Straw"
            override val capacity = 4
         }
      
Subclass 
--
   
   RoundTower is a subclass of 'RoundHut'
         
         class RoundTower(
            residents:Int, 
            val floors:Int = 2 ) : RoundHut(residents){
            
            override val buildingMaterial = "Stone"
            override val capacity = 4 * floors
         }
      
    
    
Modify classes in the hierachy 
===

 Calculate the floor area
 ----

  All abstract methods in an abstract class must be implemented in every of the subclasses.
 
        import kotlin.math.PI
     
    
 //abstract class
   
    abstract class Dwelling(private var residents: Int) {
       //methods
        ....
       abstract fun floorArea(): Double
   }
   
 //subclasses
   
    class SquareCabin(residents: Int, 
       val length: Double) : Dwelling(residents) {
       ......
       override fun floorArea(): Double {
          return length * length
       }
     }


     open class RoundHut(residents: Int, 
         val radius: Double) : Dwelling(residents) {
         ....
         override fun floorArea(): Double {
             return PI * radius * radius
         }
     }


     class RoundTower(
         residents: Int, radius: Double, 
         val floors: Int = 2) 
         : RoundHut(residents, radius) {

         ....
         override fun floorArea(): Double {
             return super.floorArea() * floors
         }
    }

  Allow a new resident to get a room
  --
  
    residents++ as a shorthand for residents = residents + 1
   
   //inside abstract class
          
        abstract class Dwelling(private var residents:Int){
             ......
             fun getRoom() {
                  if (capacity > residents) {
                      residents++
                      println("You got a room!")
                  } else {
                      println("Sorry, at capacity and no rooms left.")
                  }
              }
         }
       
   //main
    
       fun main() {
       ...
       
          println("Has room? ${hasRoom()}")
          getRoom()
       }
       
  Fit a carpet into a round dwelling
  --
  
    import kotlin.math.sqrt
    
  Implement function in RoundHut class to calculate carpet length.
  
     fun calculateMaxCarpetLength(): Double {

       return sqrt(2.0) * radius
     }
   
  Print in main()
   - you can add calculateMaxCarpetLength() to RoundHut, and RoundTower inherits it.
   
    println("Carpet Length: ${calculateMaxCarpetLength()}")
    
    
  ## Display a scrollable list
  > Use Lists in Kotlin
        
  - Create a class called "Item", where the constructor takes 2 params.
  
         open class Item(val name: String, val price: Int)
       
  - Vegetables extends from "Item", and called the superclass constructor, 
      inherits the name property from its parent class Item.
  ##### Override toString() method
    
             class Vegetables(vararg val toppings: String) : Item("Vegetables", 5) {
                    override fun toString(): String {
                        if (toppings.isEmpty()) {
                            return "$name Chef's Choice"
                        } else {
                            return name + " " + toppings.joinToString()
                        }
                    }
                }
      
   ##### vararg 
   modifier allows you to pass a variable number of arguments of the same type into a function or constructor.
      In that way, you can supply the different vegetables as individual strings instead of a list.
  
   

