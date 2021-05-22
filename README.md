# Week-3-Coding-Assignment
This repository is about Arrays and Methods.
public class App {
    public static void main(String[] args) throws Exception {

        int[] myArray = new int[3];
        myArray[0] = 23;
        myArray[1] = 42;
        myArray[2] = 43;

        System.out.println(addArray(myArray));

        double[] money = new double[5];
        money[0] = 100;
        money[1] = 120;
        money[2] = 96.99;
        money[3] = 23;
        money[4] = 50.50;

        System.out.println(moneyInWallet(money));

        System.out.println(helloMn("Hello", 3));

        // Question 1 a,b, and c
        int[] ages = { 3, 9, 23, 64, 2, 8, 28, 93 };

        System.out.println(ages[ages.length - 1] - ages[0]);

        ages = new int[] { 3, 9, 23, 64, 2, 8, 28, 93, 13, 56 };

        /**
         * newAges is an array of int values we access element inside an arry with index
         * and syntax is arrayName[index] index can be from 0 to last element of the
         * array and last element of the array is obtained by arrayName.length-1
         * 
         * arrayName[arrayName.length-1]
         */

        System.out.println(ages[ages.length - 1] - ages[0]);

        /**
         * declare a variable called sum with appropriate data type with value 0 use for
         * loop to add each elements from the ages array into the sum then finally
         * calculate and print out the average (note: this must be done outside the for
         * loop)
         */

        int sum = 0;
        for (int a = 0; a < ages.length; a++) {
            sum = sum + ages[a];
        }
        // to calculate the average: you can divide total or sum by the number of
        // elements (i.e. in this case
        // by size of the array)
        System.out.println(sum / (double) ages.length);

        // Question 2 A and B

        String[] names = new String[6];
        names[0] = "Sam";
        names[1] = "Tommy";
        names[2] = "Tim";
        names[3] = "Sally";
        names[4] = "Buck";
        names[5] = "Bob";

        int total = 0;
        for (int i = 0; i < names.length; i++) {
            total += names[i].length();
        }

        System.out.println(total / names.length);

        System.out.println("Enhance for loop:");
        String newName = "";
        for (String name : names) {
            newName += name + " ";
        }
        System.out.println(newName);

        int[] namesLength = new int[names.length];
        for (int i = 0; i < names.length; i++) {
            namesLength[i] = names[i].length();
        }

        // Question 8
        String firstName = "Andrew";
        String lastName = "Cham";
        String fullName = createFullName(firstName, lastName);

        System.out.println(fullName);

    }

    public static String createFullName(String a, String b) {
        return a + " " + b;
    }

    // Question 9
    public static boolean addArray(int[] digits) {
        int add = 0;
        for (int digit : digits) {
            add += digit;
        }
        return add > 100;
    }

    // Question 10
    public static double moneyInWallet(double[] numbers) {
        double sum = 0;
        for (double number : numbers) {
            sum += number;

        }
        return sum / numbers.length;
    }

    // Question 7
    public static String helloMn(String str, int num) {
        String result = "";
        for (int c = 0; c < num; c++) {
            result += str;
        }
        return result;
    }

    // Question 11
    public static boolean isFirstAvgGreater(double arr1[], double arr2[]) {
        if (avgArr(arr1) > avgArr(arr2)) {
            return true;
        }
        return false;
    }

    // Question 12
    public static boolean willBuyDrink(boolean isHotOutsid, double moneyInPocket) {
        if (isHotOutside && moneyInPocket > 10.50) {
            return true;
        }
        return false;
    }

    public static boolean isLeapYear(int year) {
        boolean isDivisibleBy10AND400 = (year % 100 == 0) && (hear % 400 == 0);
        boolean isDivisibleBy4 = year % 4 == 0;
        boolean isNotDivisibleBy100 = (year % 100 != 0);

        return (isDivisibleBy100AND400 || isNotDivisibleBy100) && isDivisibleBy4;
    }
}
