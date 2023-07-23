// We create the main function to execute the program.
fun main() {
    var option: Int

    // We use a while loop to display the menu and allow the user to choose an option.
    while (true) {
        println("Welcome to the menu")
        println("1. Operators")
        println("2. Conditionals")
        println("3. Loops")
        println("4. Exit")
        println("Enter the number of the desired option:")

        // We read the user's input and store it in "option" as an integer.
        option = readLine()!!.toInt()

        // We use a "when" statement to determine the action to be executed based on the selected option.
        when (option) {
            1 -> {
                menuOperators()
            }
            2 -> {
                menuConditionals()
            }
            3 -> {
                menuLoops()
            }
            4 -> {
                println("Exiting the program...")
                return // Exit the loop and end the program.
            }
            else -> {
                println("Invalid option. Please enter a valid option.")
            }
        }
    }
}

// Here we define the functions for the "Operators" menu.
fun menuOperators() {
    var option: Int
    // We use a while loop to display the options to the user (if they choose option 11, it returns to the main menu).
    while (true) {
        println("Operators")
        println("1. Triangle area")
        println("2. Sum of two numbers")
        println("3. Number squared")
        println("4. Euros to dollars")
        println("5. Square area and perimeter")
        println("6. Cylinder area")
        println("7. Cylinder volume")
        println("8. Circumference length")
        println("9. Inscribed circle area")
        println("10. Average of three numbers")
        println("11. Back to the main menu")
        println("Enter the number of the desired option:")

        option = readLine()!!.toInt()

        when (option) {
            1 -> {
                println("Enter the base of the triangle:")
                val base = readLine()!!.toDouble()
                println("Enter the height of the triangle:")
                val height = readLine()!!.toDouble()
                val area = areaTriangle(base, height)
                println("The area of the triangle is: $area")
            }
            2 -> {
                println("Enter the first number:")
                val num1 = readLine()!!.toDouble()
                println("Enter the second number:")
                val num2 = readLine()!!.toDouble()
                val sum = sumNumbers(num1, num2)
                println("The sum of the two numbers is: $sum")
            }
            3 -> {
                println("Enter the number:")
                val number = readLine()!!.toDouble()
                val square = numberSquared(number)
                println("The number squared is: $square")
            }
            4 -> {
                println("Enter the amount in euros:")
                val euros = readLine()!!.toDouble()
                val dollars = eurosToDollars(euros)
                println("$euros euros are equivalent to $dollars dollars.")
            }
            5 -> {
                println("Enter the side of the square:")
                val side = readLine()!!.toDouble()
                val (area, perimeter) = calculateSquareAreaPerimeter(side)
                println("The area of the square is: $area")
                println("The perimeter of the square is: $perimeter")
            }
            6 -> {
                println("Enter the cylinder radius:")
                val radius = readLine()!!.toDouble()
                println("Enter the cylinder height:")
                val height = readLine()!!.toDouble()
                val area = calculateCylinderArea(radius, height)
                println("The area of the cylinder is: $area")
            }
            7 -> {
                println("Enter the cylinder radius:")
                val radius = readLine()!!.toDouble()
                println("Enter the cylinder height:")
                val height = readLine()!!.toDouble()
                val volume = calculateCylinderVolume(radius, height)
                println("The volume of the cylinder is: $volume")
            }
            8 -> {
                println("Enter the circumference radius:")
                val radius = readLine()!!.toDouble()
                val length = calculateCircumferenceLength(radius)
                println("The circumference length is: $length")
            }
            9 -> {
                println("Enter the inscribed circle radius:")
                val radius = readLine()!!.toDouble()
                val area = calculateInscribedCircleArea(radius)
                println("The inscribed circle area is: $area")
            }
            10 -> {
                val average = calculateAverage()
                println("The average of the three numbers is: $average")
            }
            11 -> {
                return // Exit the loop and return to the main menu.
            }
            else -> {
                println("Invalid option. Please enter a valid option.")
            }
        }
    }
}

// Here we define the functions for the "Conditionals" menu.
fun menuConditionals() {
    var option: Int
    // We use a while loop to display the options to the user (if they choose option 8, it returns to the main menu).
    while (true) {
        println("Conditionals")
        println("1. Check if a number is positive, negative, or zero")
        println("2. Find the greater and smaller of two numbers")
        println("3. Find the greater and smaller of three numbers")
        println("4. Add two numbers if the first is smaller than the second, or subtract them otherwise")
        println("5. Find the quotient between two numbers")
        println("6. Add two numbers if at least one of them is negative, otherwise multiply them")
        println("7. Check if a year is a leap year or not")
        println("8. Back to the main menu")
        println("Enter the number of the desired option:")

        option = readLine()!!.toInt()

        when (option) {
            1 -> {
                println("Enter the number:")
                val number = readLine()!!.toInt()
                checkPositiveNegativeZero(number)
            }
            2 -> {
                println("Enter the first number:")
                val num1 = readLine()!!.toInt()
                println("Enter the second number:")
                val num2 = readLine()!!.toInt()
                findGreaterSmaller(num1, num2)
            }
            3 -> {
                println("Enter the first number:")
                val num1 = readLine()!!.toInt()
                println("Enter the second number:")
                val num2 = readLine()!!.toInt()
                println("Enter the third number:")
                val num3 = readLine()!!.toInt()
                findGreaterSmaller(num1, num2, num3)
            }
            4 -> {
                println("Enter the first number:")
                val numA = readLine()!!.toInt()
                println("Enter the second number:")
                val numB = readLine()!!.toInt()
                addOrSubtract(numA, numB)
            }
            5 -> {
                println("Enter the first number:")
                val numA = readLine()!!.toInt()
                println("Enter the second number:")
                val numB = readLine()!!.toInt()
                findQuotient(numA, numB)
            }
            6 -> {
                println("Enter the first number:")
                val numA = readLine()!!.toInt()
                println("Enter the second number:")
                val numB = readLine()!!.toInt()
                addOrMultiply(numA, numB)
            }
            7 -> {
                println("Enter the year:")
                val year = readLine()!!.toInt()
                val isLeapYear = isLeapYear(year)
                if (isLeapYear) {
                    println("The year $year is a leap year.")
                } else {
                    println("The year $year is not a leap year.")
                }
            }
            8 -> {
                return // Exit the loop and return to the main menu.
            }
            else -> {
                println("Invalid option. Please enter a valid option.")
            }
        }
    }
}

// Here we define the functions for the "Loops" menu.
fun menuLoops() {
    var option: Int
    // We use a while loop to display the options to the user (if they choose option 8, it returns to the main menu).
    while (true) {
        println("Loops")
        println("1. Print all multiples of 3 between 1 and 100.")
        println("2. Print odd numbers between 0 and 100.")
        println("3. Print even numbers from 1 to 100.")
        println("4. Print squares of numbers from 1 to 30.")
        println("5. Sum of the squares of the first hundred natural numbers.")
        println("6. Generate and display numbers between two values in ascending sequence.")
        println("7. Add all numbers entered by the user until it's zero.")
        println("8. Back to the main menu")
        println("Enter the number of the desired option:")

        option = readLine()!!.toInt()

        when (option) {
            1 -> {
                multiplesOfThree()
            }
            2 -> {
                oddNumbers()
            }
            3 -> {
                evenNumbers()
            }
            4 -> {
                squaresFromOneToThirty()
            }
            5 -> {
                sumOfSquaresFirstHundredNumbers()
            }
            6 -> {
                println("Enter the first number:")
                val num1 = readLine()!!.toInt()
                println("Enter the second number:")
                val num2 = readLine()!!.toInt()
                showNumbersInAscendingSequence(num1, num2)
            }
            7 -> {
                sumNumbersNotZero()
            }
            8 -> {
                return // Exit the loop and return to the main menu.
            }
            else -> {
                println("Invalid option. Please enter a valid option.")
            }
        }
    }
}

// Here we define the functions for each algorithm corresponding to the "Operators" menu
fun areaTriangle(base: Double, height: Double): Double {
    return (base * height) / 2
}

fun sumNumbers(num1: Double, num2: Double): Double {
    return num1 + num2
}

fun numberSquared(number: Double): Double {
    return number * number
}

fun eurosToDollars(euros: Double): Double {
    val exchangeRate = 1.17 // Euros to dollars conversion rate
    return euros * exchangeRate
}

fun calculateSquareAreaPerimeter(side: Double): Pair<Double, Double> {
    val area = side * side
    val perimeter = 4 * side
    return Pair(area, perimeter)
}

fun calculateCylinderArea(radius: Double, height: Double): Double {
    val baseArea = Math.PI * radius * radius
    val lateralArea = 2 * Math.PI * radius * height
    return baseArea + lateralArea
}

fun calculateCylinderVolume(radius: Double, height: Double): Double {
    return Math.PI * radius * radius * height
}

fun calculateCircumferenceLength(radius: Double): Double {
    return 2 * Math.PI * radius
}

fun calculateInscribedCircleArea(radius: Double): Double {
    return Math.PI * radius * radius
}

fun calculateAverage(): Double {
    println("Enter the first number:")
    val num1 = readLine()!!.toDouble()
    println("Enter the second number:")
    val num2 = readLine()!!.toDouble()
    println("Enter the third number:")
    val num3 = readLine()!!.toDouble()

    return (num1 + num2 + num3) / 3
}

// Here we define the functions for the "Conditionals" menu
fun checkPositiveNegativeZero(number: Int) {
    if (number > 0) {
        println("The number is positive.")
    } else if (number < 0) {
        println("The number is negative.")
    } else {
        println("The number is zero.")
    }
}

fun findGreaterSmaller(num1: Int, num2: Int) {
    if (num1 > num2) {
        println("The greater number is: $num1")
        println("The smaller number is: $num2")
    } else if (num1 < num2) {
        println("The greater number is: $num2")
        println("The smaller number is: $num1")
    } else {
        println("Both numbers are equal.")
    }
}

fun findGreaterSmaller(num1: Int, num2: Int, num3: Int) {
    val greater = maxOf(num1, num2, num3)
    val smaller = minOf(num1, num2, num3)
    println("The greater number is: $greater")
    println("The smaller number is: $smaller")
}

fun addOrSubtract(numA: Int, numB: Int) {
    val result = if (numA < numB) {
        numA + numB
    } else {
        numA - numB
    }
    println("The result is: $result")
}

fun findQuotient(numA: Int, numB: Int) {
    if (numB != 0) {
        val quotient = numA.toDouble() / numB
        println("The quotient is: $quotient")
    } else {
        println("Error: Cannot divide by zero.")
    }
}

fun addOrMultiply(numA: Int, numB: Int) {
    val result = if (numA < 0 || numB < 0) {
        numA + numB
    } else {
        numA * numB
    }
    println("The result is: $result")
}

fun isLeapYear(year: Int): Boolean {
    return year % 4 == 0 && (year % 100 != 0 || year % 400 == 0)
}

// Here we define the functions for the "Loops" menu
fun multiplesOfThree() {
    println("Multiples of 3 between 1 and 100:")
    for (i in 1..100) {
        if (i % 3 == 0) {
            println(i)
        }
    }
}

fun oddNumbers() {
    println("Odd numbers between 0 and 100:")
    var i = 0
    while (i <= 100) {
        if (i % 2 != 0) {
            println(i)
        }
        i++
    }
}

fun evenNumbers() {
    println("Even numbers from 1 to 100:")
    var i = 1
    while (i <= 100) {
        if (i % 2 == 0) {
            println(i)
        }
        i++
    }
}

fun squaresFromOneToThirty() {
    println("Squares of numbers from 1 to 30:")
    for (i in 1..30) {
        val square = i * i
        println("The square of $i is $square")
    }
}

fun sumOfSquaresFirstHundredNumbers() {
    var sum = 0
    for (i in 1..100) {
        sum += i * i
    }
    println("The sum of the squares of the first hundred natural numbers is: $sum")
}

fun showNumbersInAscendingSequence(num1: Int, num2: Int) {
    println("Numbers between $num1 and $num2 in ascending sequence:")
    for (i in num1..num2) {
        println(i)
    }
}

fun sumNumbersNotZero() {
    var sum = 0
    var number: Int
    do {
        println("Enter a number (enter 0 to finish):")
        number = readLine()!!.toInt()
        sum += number
    } while (number != 0)
    println("The sum of the entered numbers is: $sum")
}# fundamentals-native-mobile-development
