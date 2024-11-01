
Python Program Developing a Grade Statistics Program 
Matthew Morrison
Colorado State University Global
CSC-320-1
Dr. Mujeye
October 25, 2024








Python Program Developing a Grade Statistics Program 
	In the realm of education, understanding student performance through grades is key for both teachers and students. A program that computes important statistics such as average, maximum, and minimum grades can significantly aid in this understanding. This essay outlines the development of such a program using a for-loop to process user input and include strategies to prevent infinite loops. 
	To begin, before diving into the source code, it is crucial to outline the program’s logic using pseudocode. For example, this helps in visualizing the flow of the program without getting bogged down by syntax. 
START
    Initialize total to 0
    Initialize maxGrade to a very small number (e.g., -infinity)
    Initialize minGrade to a very large number (e.g., infinity)
      FOR i FROM 1 TO 10 DO
        PROMPT "Enter grade #" + i + ": "
        READ grade
        
        WHILE grade is not a valid floating-point number DO
            PROMPT "Invalid input. Please enter a valid grade:"
            READ grade
        END WHILE
         Add grade to total
        IF grade > maxGrade THEN
            Set maxGrade to grade
        END IF
        IF grade < minGrade THEN
            Set minGrade to grade
        END IF
    END FOR
    Calculate average by dividing total by 10
    PRINT "Average grade: " + average
    PRINT "Maximum grade: " + maxGrade
    PRINT "Minimum grade: " + minGrade
END

Here is the implementation of the pseudocode in Python, a language well-suited for this task due to its simplicity and ease of use. 


def main():
    grades = []
 # Loop to read five grades from user input
    for i in range(5):
        while True:
            try:
                grade = float(input(f"Enter grade {i + 1}: "))
                grades.append(grade)
                break  # Exit the loop if input is valid
            except ValueError:
                print("Invalid input. Please enter a valid floating-point number.")

    # Calculate statistics
    average = sum(grades) / len(grades)
    maximum = max(grades)
    minimum = min(grades)

    # Print the results
    print(f"\nAverage grade: {average:.2f}")
    print(f"Maximum grade: {maximum:.2f}")
    print(f"Minimum grade: {minimum:.2f}")

if __name__ == "__main__":
    main()


Here are the screenshots of the code executing.
 

Screen Shot 1
Matt Morrison, Screenshot, October 25, 2024
Note. This screenshot shows the code executed on Python Emulator. The user is prompt to enter 5 grades, after entering 5 grades the program calculates and displays the average, maximum, and minimum grades clearly.





Screen Shot 2 


Matt Morrison, Screenshot, October 25, 2024
Note. This screenshot shows the code executed on Python Emulator. The program displays the average, maximum, and minimum grades clearly. 

	In conclusion, the development of a grade statistics program using a for-loop provides valuable insights into student performance. Implementing input validation, the program enhances user experience and reliability. The combination of pseudocode, source code, and real-time execution demonstrates the program’s efficacy and robustness. This tool is not only beneficial for teachers assessing overall class performance but also for students aiming to understand their academic standing. 












	

























	Reference


