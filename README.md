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

