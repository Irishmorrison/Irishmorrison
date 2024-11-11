
Java Program Developing a Grade Statistics Program 
Matthew Morrison
Colorado State University Global
CSC-320-1
Dr. Mujeye
November 1, 2024

Here is my pseudocode.

BEGIN
    DECLARE total AS FLOAT
    DECLARE max AS FLOAT
    DECLARE min AS FLOAT
    DECLARE grade AS FLOAT
    DECLARE numGrades AS INTEGER
    SET total = 0
    SET max = -INFINITY
    SET min = INFINITY
    SET numGrades = 10

    FOR i FROM 1 TO numGrades DO
        PROMPT "Enter grade " + i + ": "
        READ grade
        IF grade < 0 THEN
            PRINT "Grade must be non-negative. Try again."
            DECREMENT i
        ELSE
            total = total + grade
            IF grade > max THEN
                max = grade
            ENDIF
            IF grade < min THEN
                min = grade
            ENDIF
        ENDIF
    ENDFOR

    IF numGrades > 0 THEN
        SET average = total / numGrades
        PRINT "Average: " + average
        PRINT "Maximum: " + max
        PRINT "Minimum: " + min
    ELSE
        PRINT "No valid grades entered."
    ENDIF
END

Here is my Java soucre code

import java.util.Scanner;

public class GradeStatistics {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double sum = 0.0;
        double max = Double.NEGATIVE_INFINITY;
        double min = Double.POSITIVE_INFINITY;

        for (int i = 0; i < 10; i++) {
            System.out.print("Enter grade " + (i + 1) + ": ");
            while (!scanner.hasNextDouble()) {
                System.out.println("Invalid input. Please enter a numeric value.");
                scanner.next(); // clear the invalid input
            }
            double grade = scanner.nextDouble();
            sum += grade;
            if (grade > max) {
                max = grade;
            }
            if (grade < min) {
                min = grade;
            }
        }

        double average = sum / 10;
        System.out.printf("Average: %.2f%n", average);
        System.out.printf("Maximum: %.2f%n", max);
        System.out.printf("Minimum: %.2f%n", min);

        scanner.close();
    }
}
       



















	

























	Reference


