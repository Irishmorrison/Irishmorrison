
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
        
        double total = 0;
        double max = Double.NEGATIVE_INFINITY;
        double min = Double.POSITIVE_INFINITY;
        int numGrades = 10;
        
        for (int i = 1; i <= numGrades; i++) {
            System.out.print("Enter grade " + i + ": ");
            double grade = scanner.nextDouble();
            
            // Check for non-negative grades
            if (grade < 0) {
                System.out.println("Grade must be non-negative. Please try again.");
                i--; // Decrement i to repeat this iteration
                continue; // Skip to the next iteration
            }
            
            total += grade;
            
            if (grade > max) {
                max = grade;
            }
            if (grade < min) {
                min = grade;
            }
        }
        
        if (numGrades > 0) {
            double average = total / numGrades;
            System.out.println("Average: " + average);
            System.out.println("Maximum: " + max);
            System.out.println("Minimum: " + min);
        } else {
            System.out.println("No valid grades entered.");
        }
        
        scanner.close();
    }
}




















	

























	Reference


