# Calculator

1. Create a method that accepts two integers as input, then returns an integer that is the sum of these two parameters. (Addition)
2. Create the following additional three methods that each take two parameters:
	* Multiplication - which takes two numbers and returns the product.
	* Subtraction - which takes two numbers, then returns the result of the subtraction.
	* Division - which takes two numbers, then returns the result of the division.
3. Your division method may have returned the wrong result; This is called a rounding error and is quite common in most languages. this is because we were using ints rather than doubles. Modify the division method so that it takes Double parameters and then return a Double, if not already.

```java
public class Calculator {
		// method to sum numbers taking in two integers
		public int addition(int int1, int int2) {
			return int1+int2;
		}
		
		// method to multiply numbers taking in two numbers
		public int multiplication(int num1, int num2) {
			return num1*num2;
		}
		
		// method to subtract
		public int subtraction(int subFrom, int subThis) {
			return subFrom-subThis;
		}
		
		// method to divide
		public double division(double divFrom, double divBy) {
			return divFrom/divBy;
		}
}
```

```java
public class Runner {
	
	public static void main(String[] args) {
		
		Calculator calc = new Calculator();
		
		int firstInt = 10;
		int secondInt = 5;
		int addResult = calc.addition(firstInt, secondInt);
		System.out.println(firstInt + " + " + secondInt + " = " + addResult);
		
		int multResult = calc.multiplication(firstInt, secondInt);
		System.out.println(firstInt + " * " + secondInt + " = " + multResult);
		
		int subResult = calc.subtraction(firstInt, secondInt);
		System.out.println(firstInt + " - " + secondInt + " = " + subResult);
		
		double divResult = calc.division(firstInt, secondInt);
		System.out.println(firstInt + " / " + secondInt + " = " + divResult);
	}

}

```