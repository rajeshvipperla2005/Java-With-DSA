Input a year and find whether it is a leap year or not.
public class LeapYear {
    public static void main(String[] args) {

        int year = 2024;

        if (year % 400 == 0) {
            System.out.println("Leap Year");
        }
        else if (year % 100 == 0) {
            System.out.println("Not a Leap Year");
        }
        else if (year % 4 == 0) {
            System.out.println("Leap Year");
        }
        else {
            System.out.println("Not a Leap Year");
        }
    }
}
outpt:
Leap Year

Take two numbers and print the sum of both.
public class Sum {
    public static void main(String[] args) {

        int a = 25;
        int b = 30;

        int sum = a + b;

        System.out.println("Sum = " + sum);
    }
}
output:
Sum = 55

Take a number as input and print the multiplication table for it.
public class Table {
    public static void main(String[] args) {

        int n = 25;

        System.out.println(n + " x 1 = " + (n * 1));
        System.out.println(n + " x 2 = " + (n * 2));
        System.out.println(n + " x 3 = " + (n * 3));
        System.out.println(n + " x 4 = " + (n * 4));
        System.out.println(n + " x 5 = " + (n * 5));
        System.out.println(n + " x 6 = " + (n * 6));
        System.out.println(n + " x 7 = " + (n * 7));
        System.out.println(n + " x 8 = " + (n * 8));
        System.out.println(n + " x 9 = " + (n * 9));
        System.out.println(n + " x 10 = " + (n * 10));
    }
}
output:
25 x 1 = 25
25 x 2 = 50
25 x 3 = 75
25 x 4 = 100
25 x 5 = 125
25 x 6 = 150
25 x 7 = 175
25 x 8 = 200
25 x 9 = 225
25 x 10 = 250

Take 2 numbers as inputs and find their HCF and LCM.
public class HCFLCM {
    public static void main(String[] args) {

        int a = 12;
        int b = 18;

        int hcf = 1;

        for (int i = 1; i <= a && i <= b; i++) {
            if (a % i == 0 && b % i == 0) {
                hcf = i;
            }
        }

        int lcm = (a * b) / hcf;

        System.out.println("HCF = " + hcf);
        System.out.println("LCM = " + lcm);
    }
}
output:
HCF = 6
LCM = 36


Keep taking numbers as inputs till the user enters ‘x’, after that print sum of all.
import java.util.Scanner;

public class SumNumbers {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        int sum = 0;

        while (true) {
            System.out.print("Enter number or x to stop: ");
            String value = sc.next();

            if (value.equals("x")) {
                break;
            }

            int num = Integer.parseInt(value);
            sum = sum + num;
        }

        System.out.println("Sum = " + sum);
    }
}
output:
Enter number or x to stop: 12
Enter number or x to stop: 13
Enter number or x to stop: x
Sum = 25
