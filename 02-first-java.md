Write a program to print whether a number is even or odd, also take input from the user.
import java.util.Scanner;

public class EvenOdd {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int num = sc.nextInt();

        System.out.println((num % 2 == 0) ? "Even" : "Odd");

        sc.close();
    }
}
output:
Enter a number: 4
Even

Take name as input and print a greeting message for that particular name.
import java.util.Scanner;

public class Greeting {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.println("Hello, " + name + "! Welcome.");

        sc.close();
    }
}
output:
Enter your name: rajesh
Hello, rajesh! Welcome.

Write a program to input principal, time, and rate (P, T, R) from the user and find Simple Interest.
import java.util.Scanner;

public class SimpleInterest {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter Principal: ");
        float p = sc.nextFloat();

        System.out.print("Enter Time: ");
        float t = sc.nextFloat();

        System.out.print("Enter Rate: ");
        float r = sc.nextFloat();

        float si = (p * t * r) / 100;

        System.out.println("Simple Interest = " + si);

        sc.close();
    }
}
output:
Enter Principal: 1000
Enter Time: 3
Enter Rate: 6
Simple Interest = 180.0

Take in two numbers and an operator (+, -, *, /) and calculate the value. (Use if conditions)
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        double num1 = sc.nextDouble();

        System.out.print("Enter second number: ");
        double num2 = sc.nextDouble();

        System.out.print("Enter operator (+, -, *, /): ");
        char op = sc.next().charAt(0);

        if (op == '+') {
            System.out.println("Result = " + (num1 + num2));
        } else if (op == '-') {
            System.out.println("Result = " + (num1 - num2));
        } else if (op == '*') {
            System.out.println("Result = " + (num1 * num2));
        } else if (op == '/') {
            if (num2 != 0) {
                System.out.println("Result = " + (num1 / num2));
            } else {
                System.out.println("Division by zero is not allowed.");
            }
        } else {
            System.out.println("Invalid operator.");
        }

        sc.close();
    }
}
output:
Enter first number: 4
Enter second number: 6
Enter operator (+, -, *, /): +
Result = 10.0

Take 2 numbers as input and print the largest number.
import java.util.Scanner;

public class LargestNumber {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter first number: ");
        int a = sc.nextInt();

        System.out.print("Enter second number: ");
        int b = sc.nextInt();

        if (a > b) {
            System.out.println("Largest number = " + a);
        } else {
            System.out.println("Largest number = " + b);
        }

        sc.close();
    }
}
output:
Enter first number: 5
Enter second number: 7
Largest number = 7


Input currency in rupees and output in USD.
import java.util.Scanner;

public class CurrencyConverter {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter amount in Rupees: ");
        double rupees = sc.nextDouble();

        double usd = rupees / 83;

        System.out.println("Amount in USD = " + usd);

        sc.close();
    }
}
output:
Enter amount in Rupees: 1000
Amount in USD = 12.048192771084338


To calculate Fibonacci Series up to n numbers.
import java.util.Scanner;

public class FibonacciSeries {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter the number of terms: ");
        int n = sc.nextInt();

        int a = 0, b = 1;

        for (int i = 1; i <= n; i++) {
            System.out.print(a + " ");
            int c = a + b;
            a = b;
            b = c;
        }

        sc.close();
    }
}
output:
Enter the number of terms: 5
0 1 1 2 3 


To find out whether the given String is Palindrome or not.
import java.util.Scanner;

public class PalindromeString {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter a string: ");
        String str = sc.nextLine();

        String rev = "";

        for (int i = str.length() - 1; i >= 0; i--) {
            rev = rev + str.charAt(i);
        }

        if (str.equals(rev)) {
            System.out.println("Palindrome");
        } else {
            System.out.println("Not a Palindrome");
        }

        sc.close();
    }
}
output:
Enter a string: madam
Palindrome

To find Armstrong Number between two given number.
import java.util.Scanner;

public class ArmstrongRange {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("Enter starting number: ");
        int start = sc.nextInt();

        System.out.print("Enter ending number: ");
        int end = sc.nextInt();

        System.out.println("Armstrong numbers are:");

        for (int i = start; i <= end; i++) {
            int num = i;
            int temp = num;
            int digits = 0;
            int sum = 0;

            // Count the number of digits
            while (temp != 0) {
                digits++;
                temp = temp / 10;
            }

            temp = num;

            // Calculate sum of each digit raised to the power of digits
            while (temp != 0) {
                int digit = temp % 10;
                sum += (int) Math.pow(digit, digits);
                temp = temp / 10;
            }

            // Check Armstrong number
            if (sum == num) {
                System.out.println(num);
            }
        }

        sc.close();
    }
}
output:
Enter starting number: 10
Enter ending number: 200
Armstrong numbers are:
153
