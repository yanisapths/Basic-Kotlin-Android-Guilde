1. Syntax
   
 1.1 Defining Strings

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
    
    var name1:String = "Cody Blackwell"
    var name2:String = "Martha Horowitz"
    var firstname:String = "Raj "
    var lastname:String = "Chawanda"

    val firstN:String = name1.trimMargin("Cody ")
    println(firstN)
    println(name1.length)
    println(name2.length)

    println(name1.compareTo(name2))

    var addNames = firstname.plus(lastname)
    println(addNames)

    var addNames2 = name1.plus(" "+name2)
    println(addNames2)
    
  1.4 Kotlin Conditionals
   1. if & when
   
        1.1 "if" statement returns value , no ternary required
         ex:
         
            if (x=y) z=10

        1.2 "if" can be represented as blocks
          ex:
          
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
        ex:
       
          when (x) {
               1 -> println("x equals 1")
               2 -> println("x equals 2")
               else -> {
                   println("x not equal to 1 or 2")
               }
           }

