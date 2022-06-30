Syntax

    fun main (args: Array<String>) {
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
    println("$x plus $y is $sum or ${x + y}") }
    
