
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
     
   1. if & when

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

        1.3 "when" similar to "switch" in C lang, but in Kotlin, it's "when"
                
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
                              
       > if..else..
                     
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
         
      
   > While loop
           
           var i = 0
            while(i < 100) {
               i+=5
               print("$i, ")
            }
         
         5, 10, 15, 20, 25, 30, 35, 40, 45, 50, 55, 60, 65, 70, 75, 80, 85, 90, 95, 100, 

   > Do...while loop

         do {
            i-=5
            print("$i, ")
         } while(i > 0)
         
         95, 90, 85, 80, 75, 70, 65, 60, 55, 50, 45, 40, 35, 30, 25, 20, 15, 10, 5, 0, 
       
    
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
  
    listOf
    List<T> and MutableList<T> 
    No modifying methods 
    MutableList<T> has "add()" & "remove()"
     
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

