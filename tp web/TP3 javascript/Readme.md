# -TP3-Introduction-JavaScript-Types-simples-variables-

## École Normale Supérieure de l’Enseignement Technique de Mohammedia
**Master SDIA**  
**Technologies du Web & Web Sémantique**

## Objectives
The purpose of this lab is to familiarize you with the basic constructs of JavaScript, including simple types, variable declarations, control statements, and loops. The syntax is very similar to the C programming language.

---

## Exercises

### Exercise 1: Temperature Conversion
Write a JavaScript function `degreC` to convert a temperature from Fahrenheit to Celsius using the formula:

\[ \text{tempC} = \frac{5}{9} (\text{tempF} - 32) \]

#### Example execution:
```
Enter a temperature in Fahrenheit: 0.0
This temperature is equivalent to -17.8 degrees Celsius

Enter a temperature in Fahrenheit: 60.0
This temperature is equivalent to 15.6 degrees Celsius
```

### Exercise 2: Duration Conversion
Write a JavaScript function `hjms` that converts a given number of seconds into days, hours, minutes, and seconds.

#### Example execution:
```
Enter duration in seconds: 235789
This duration is equivalent to 2 days 17 hours 29 minutes 49 seconds

Enter duration in seconds: 567231
This duration is equivalent to 6 days 13 hours 33 minutes 51 seconds
```

#### Exercise 2-bis: Improved Duration Conversion
Enhance the `hjms` function to ensure that:
- Zero values are omitted from the display.
- Singular units (e.g., "1 hour" instead of "1 hours") are used correctly.

#### Example execution:
```
Enter duration in seconds: 3621
This duration is equivalent to 1 hour 21 seconds
```

### Exercise 3: Sorting Three Numbers
Write a program `troisNombres` that sorts three numbers in ascending order.

#### Example execution:
```
Enter first number: 14
Enter second number: 10
Enter third number: 17
Numbers in ascending order: 10 14 17
```

### Exercise 4: Staircase Pattern
Write a program that prints a triangular pattern of a given size.

#### Example execution:
```
Enter size: 7
*
**
***
****
*****
******
```

- `triangle1`: Implement using `while` loops.
- `triangle2`: Implement using `for` loops.

### Exercise 4-bis: Pyramid Pattern
Modify the previous exercise to display a pyramid instead of a triangle.

#### Example execution:
```
Enter size: 7
     *
    ***
   *****
  *******
 *********
***********
*************
```

### Exercise 5: Prime Number Check
Write a program `Premier` that checks if a given number is prime.

#### Example execution:
```
Enter a positive integer: 7
7 is a prime number

Enter a positive integer: 25
25 is not a prime number, it is divisible by 5
```

### Exercise 6: Fibonacci Sequence
Implement the Fibonacci sequence using:
- `Fibo1`: Computes the nth Fibonacci number.
- `Fibo2`: Finds the first Fibonacci number greater than a given value.

### Exercise 7: Approximate Square Root Calculation
Using the iterative formula:

\[ u_{n+1} = \frac{1}{2} (u_n + \frac{A}{u_n}) \]

Write a function `Raca1` that computes an approximate square root of a given number A (1 ≤ A ≤ 100) until:

\[ | u_n^2 - A | < 10^{-6} \]

#### Example execution:
```
Enter a number A: 25
Approximate square root: 5.000001
```

---

## Conclusion
This lab introduces fundamental JavaScript concepts and basic problem-solving skills. Mastering these exercises will help build a strong foundation for more complex JavaScript programming tasks.
