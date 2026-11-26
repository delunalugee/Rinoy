import random

score_history = []

print("===================================")
print(" PYTHON PROGRAMMING REVIEWER")
print("===================================")

while True:
    print("\nMAIN MENU")
    print("1. PRELIM")
    print("2. MIDTERM")
    print("3. FINALS")
    print("4. SUGGESTIONS")
    print("5. RANDOM QUIZ")
    print("6. CODING CHALLENGE")
    print("7. SCORE HISTORY")
    print("8. EXIT")

    choice = input("\nChoose a topic: ")

    if choice == "1":
        while True:
            print("\n========== PRELIM ==========")
            print("1. Introduction to Programming")
            print("2. Python Basic Syntax")
            print("3. Arithmetic Operators and Expressions")
            print("4. Basic Input and Output")
            print("5. Prelim Quiz")
            print("6. Back to Main Menu")

            pre = input("\nChoose a lesson: ")

            if pre == "1":
                print("\nINTRODUCTION TO PROGRAMMING")
                print("Programming is the process of creating instructions for a computer.")
                print("Python is a programming language used to create programs.")
                print("An algorithm is a step-by-step procedure for solving a problem.")
                print("\nExample:")
                print('print("Hello World")')
                print("Output: Hello World")

            elif pre == "2":
                print("\nPYTHON BASIC SYNTAX")
                print("Syntax refers to the rules for writing Python code.")
                print("Python uses indentation to organize code.")
                print("The print() function displays information.")
                print("Variables store data.")
                print("\nExample:")
                print('name = "Anna"')
                print("age = 18")
                print("print(name)")
                print("print(age)")
                print("\nOutput:")
                print("Anna")
                print("18")

            elif pre == "3":
                print("\nARITHMETIC OPERATORS AND EXPRESSIONS")
                print("+ Addition")
                print("- Subtraction")
                print("* Multiplication")
                print("/ Division")
                print("// Floor Division")
                print("% Modulus")
                print("** Exponentiation")
                print("\nExample:")
                print("a = 10")
                print("b = 5")
                print("print(a + b)")
                print("print(a - b)")
                print("print(a * b)")
                print("print(a / b)")
                print("\nOutput:")
                print("15")
                print("5")
                print("50")
                print("2.0")

            elif pre == "4":
                print("\nBASIC INPUT AND OUTPUT")
                print("input() receives information from the user.")
                print("print() displays information.")
                print("\nExample:")
                print('name = input("Enter your name: ")')
                print('print("Hello", name)')

            elif pre == "5":
                questions = [
                    ("What programming language are we studying?", "python"),
                    ("What function displays output?", "print"),
                    ("What symbol is used for multiplication?", "*"),
                    ("What function receives user input?", "input"),
                    ("What stores data in a program?", "variable")
                ]

                while True:
                    score = 0
                    random.shuffle(questions)

                    print("\n========== PRELIM QUIZ ==========")

                    for question, correct in questions:
                        answer = input(f"{question} ").lower().strip()

                        if answer == correct:
                            print("Correct!")
                            score += 1
                        else:
                            print(f"Incorrect! Correct answer: {correct}")

                    percentage = score / len(questions) * 100

                    print(f"\nYour Score: {score}/{len(questions)}")
                    print(f"Percentage: {round(percentage, 2)}%")

                    if percentage >= 75:
                        print("Great job!")
                    else:
                        print("Keep reviewing!")

                    score_history.append(("PRELIM QUIZ", score, len(questions)))

                    retry = input("\nTry again? (yes/no): ")

                    if retry.lower() != "yes":
                        break

            elif pre == "6":
                break

            else:
                print("Invalid choice.")

            input("\nPress ENTER to continue...")

    elif choice == "2":
        while True:
            print("\n========== MIDTERM ==========")
            print("1. Introduction to Conditional Statements")
            print("2. Relational Operators")
            print("3. If Statement")
            print("4. If-Else Statement")
            print("5. If-Elif-Else Statement")
            print("6. Nested Condition")
            print("7. Logical Operators and Truth Tables")
            print("8. Midterm Quiz")
            print("9. Back to Main Menu")

            mid = input("\nChoose a lesson: ")

            if mid == "1":
                print("\nCONDITIONAL STATEMENTS")
                print("Conditional statements allow a program to make decisions.")
                print("They execute different instructions depending on a condition.")
                print("\nExample:")
                print("age = 18")
                print("if age >= 18:")
                print('    print("Adult")')

            elif mid == "2":
                print("\nRELATIONAL OPERATORS")
                print("== Equal to")
                print("!= Not equal to")
                print("> Greater than")
                print("< Less than")
                print(">= Greater than or equal to")
                print("<= Less than or equal to")
                print("These operators compare two values.")
                print("The result is either True or False.")

            elif mid == "3":
                print("\nIF STATEMENT")
                print("The if statement executes code when a condition is True.")
                print("\nExample:")
                print("age = 20")
                print("if age >= 18:")
                print('    print("You can vote.")')

            elif mid == "4":
                print("\nIF-ELSE STATEMENT")
                print("The if-else statement provides two possible results.")
                print("\nExample:")
                print("number = 5")
                print("if number > 0:")
                print('    print("Positive")')
                print("else:")
                print('    print("Negative or Zero")')

            elif mid == "5":
                print("\nIF-ELIF-ELSE STATEMENT")
                print("The elif statement checks another condition if the first is False.")
                print("\nExample:")
                print("grade = 90")
                print("if grade >= 90:")
                print('    print("Excellent")')
                print("elif grade >= 75:")
                print('    print("Passed")')
                print("else:")
                print('    print("Failed")')

            elif mid == "6":
                print("\nNESTED CONDITION")
                print("A nested condition is an if statement inside another if statement.")
                print("\nExample:")
                print("age = 20")
                print("has_id = True")
                print("if age >= 18:")
                print("    if has_id:")
                print('        print("Allowed")')

            elif mid == "7":
                print("\nLOGICAL OPERATORS")
                print("\nAND OPERATOR")
                print("True and True = True")
                print("True and False = False")
                print("False and True = False")
                print("False and False = False")

                print("\nOR OPERATOR")
                print("True or True = True")
                print("True or False = True")
                print("False or True = True")
                print("False or False = False")

                print("\nNOT OPERATOR")
                print("not True = False")
                print("not False = True")

            elif mid == "8":
                questions = [
                    ("What statement is used to make a decision?", "if"),
                    ("What operator means equal to?", "=="),
                    ("What keyword is used when the if condition is False?", "else"),
                    ("What keyword checks another condition?", "elif"),
                    ("What operator requires both conditions to be True?", "and"),
                    ("What logical operator reverses a Boolean value?", "not")
                ]

                while True:
                    score = 0
                    random.shuffle(questions)

                    print("\n========== MIDTERM QUIZ ==========")

                    for question, correct in questions:
                        answer = input(f"{question} ").lower().strip()

                        if answer == correct:
                            print("Correct!")
                            score += 1
                        else:
                            print(f"Incorrect! Correct answer: {correct}")

                    percentage = score / len(questions) * 100

                    print(f"\nYour Score: {score}/{len(questions)}")
                    print(f"Percentage: {round(percentage, 2)}%")

                    if percentage >= 75:
                        print("Great work!")
                    else:
                        print("Review the lessons and try again.")

                    score_history.append(("MIDTERM QUIZ", score, len(questions)))

                    retry = input("\nTry again? (yes/no): ")

                    if retry.lower() != "yes":
                        break

            elif mid == "9":
                break

            else:
                print("Invalid choice.")

            input("\nPress ENTER to continue...")

    elif choice == "3":
        while True:
            print("\n========== FINALS ==========")
            print("1. Introduction to Iteration")
            print("2. For Loop")
            print("3. While Loop")
            print("4. Finals Quiz")
            print("5. Back to Main Menu")

            final = input("\nChoose a lesson: ")

            if final == "1":
                print("\nINTRODUCTION TO ITERATION")
                print("Iteration means repeating a set of instructions.")
                print("Loops are used to repeat code.")
                print("Python has two common types of loops: for loop and while loop.")

            elif final == "2":
                print("\nFOR LOOP")
                print("A for loop repeats code for each item in a sequence.")
                print("\nExample:")
                print("for number in range(1, 6):")
                print("    print(number)")
                print("\nOutput:")

                for number in range(1, 6):
                    print(number)

            elif final == "3":
                print("\nWHILE LOOP")
                print("A while loop repeats code while the condition is True.")
                print("\nExample:")
                print("number = 1")
                print("while number <= 5:")
                print("    print(number)")
                print("    number = number + 1")
                print("\nOutput:")

                number = 1

                while number <= 5:
                    print(number)
                    number = number + 1

            elif final == "4":
                questions = [
                    ("What is the process of repeating instructions?", "iteration"),
                    ("What loop is commonly used with range()?", "for"),
                    ("What loop repeats while a condition is True?", "while"),
                    ("How many times will range(1, 4) repeat?", "3"),
                    ("What must change in a while loop to avoid an endless loop?", "variable")
                ]

                while True:
                    score = 0
                    random.shuffle(questions)

                    print("\n========== FINALS QUIZ ==========")

                    for question, correct in questions:
                        answer = input(f"{question} ").lower().strip()

                        if answer == correct:
                            print("Correct!")
                            score += 1
                        else:
                            print(f"Incorrect! Correct answer: {correct}")

                    percentage = score / len(questions) * 100

                    print(f"\nYour Score: {score}/{len(questions)}")
                    print(f"Percentage: {round(percentage, 2)}%")

                    if percentage >= 75:
                        print("Well done!")
                    else:
                        print("Keep practicing!")

                    score_history.append(("FINALS QUIZ", score, len(questions)))

                    retry = input("\nTry again? (yes/no): ")

                    if retry.lower() != "yes":
                        break

            elif final == "5":
                break

            else:
                print("Invalid choice.")

            input("\nPress ENTER to continue...")

    elif choice == "4":
        print("\n========== STUDY SUGGESTIONS ==========")
        print("1. Review one chapter at a time.")
        print("2. Practice writing Python code.")
        print("3. Understand what each line of code does.")
        print("4. Practice using print() and input().")
        print("5. Memorize arithmetic, relational, and logical operators.")
        print("6. Practice writing conditional statements.")
        print("7. Understand the difference between for and while loops.")
        print("8. Take quizzes after reviewing each topic.")
        print("9. Read error messages carefully.")
        print("10. Practice simple coding problems every day.")

        print("\nREMEMBER:")
        print("Do not just memorize the code.")
        print("Understand the purpose of each statement.")

        input("\nPress ENTER to return to the Main Menu...")

    elif choice == "5":
        questions = [
            ("What function displays output?", "print"),
            ("What function receives user input?", "input"),
            ("What symbol means equal to?", "=="),
            ("What keyword checks another condition?", "elif"),
            ("What logical operator requires both conditions to be True?", "and"),
            ("What loop is used with range()?", "for"),
            ("What loop repeats while a condition is True?", "while"),
            ("What operator is used for exponentiation?", "**"),
            ("What is the process of repeating instructions?", "iteration"),
            ("What keyword is used when a condition is False?", "else")
        ]

        while True:
            score = 0
            random.shuffle(questions)

            print("\n========== RANDOM QUIZ ==========")
            print("Answer all 10 questions.")

            for question, correct in questions:
                answer = input(f"{question} ").lower().strip()

                if answer == correct:
                    print("Correct!")
                    score += 1
                else:
                    print(f"Incorrect! Correct answer: {correct}")

            percentage = score / len(questions) * 100

            print("\n========== QUIZ RESULT ==========")
            print(f"Your Score: {score}/{len(questions)}")
            print(f"Percentage: {round(percentage, 2)}%")

            if percentage >= 90:
                print("Excellent! You understand the lessons very well.")
            elif percentage >= 75:
                print("Very good! Keep practicing.")
            else:
                print("You need more practice. Review your lessons.")

            score_history.append(("RANDOM QUIZ", score, len(questions)))

            retry = input("\nTake another random quiz? (yes/no): ")

            if retry.lower() != "yes":
                break

    elif choice == "6":
        while True:
            print("\n========== CODING CHALLENGE ==========")
            print("1. Display Hello World")
            print("2. Add Two Numbers")
            print("3. Check Positive or Negative")
            print("4. Check Even or Odd")
            print("5. Display Numbers Using a For Loop")
            print("6. Display Numbers Using a While Loop")
            print("7. Back to Main Menu")

            challenge = input("\nChoose a challenge: ")

            if challenge == "1":
                print("\nCHALLENGE: DISPLAY HELLO WORLD")
                print('Write a statement that displays "Hello World".')

                answer = input("Enter your code: ").replace(" ", "").lower()

                if answer in ['print("helloworld")', "print('helloworld')"]:
                    print("Correct! Great job!")
                else:
                    print('Correct code: print("Hello World")')

            elif challenge == "2":
                print("\nCHALLENGE: ADD TWO NUMBERS")
                a = float(input("Enter the first number: "))
                b = float(input("Enter the second number: "))
                print(f"Sum: {a + b}")

            elif challenge == "3":
                print("\nCHALLENGE: POSITIVE OR NEGATIVE")
                number = float(input("Enter a number: "))

                if number > 0:
                    print("Positive")
                elif number < 0:
                    print("Negative")
                else:
                    print("Zero")

            elif challenge == "4":
                print("\nCHALLENGE: EVEN OR ODD")
                number = int(input("Enter a number: "))

                if number % 2 == 0:
                    print("Even")
                else:
                    print("Odd")

            elif challenge == "5":
                print("\nCHALLENGE: FOR LOOP")

                for number in range(1, 6):
                    print(number)

            elif challenge == "6":
                print("\nCHALLENGE: WHILE LOOP")
                number = 1

                while number <= 5:
                    print(number)
                    number += 1

            elif challenge == "7":
                break

            else:
                print("Invalid choice.")

            input("\nPress ENTER to continue...")

    elif choice == "7":
        print("\n========== SCORE HISTORY ==========")

        if len(score_history) == 0:
            print("No quiz attempts recorded yet.")

        else:
            total_score = 0
            total_questions = 0

            for i, (title, score, total) in enumerate(score_history, 1):
                percentage = score / total * 100

                print(f"{i}. {title}: {score}/{total} ({round(percentage, 2)}%)")

                total_score += score
                total_questions += total

            print(f"\nTotal Attempts: {len(score_history)}")
            print(f"Overall Score: {total_score}/{total_questions}")
            print(f"Overall Percentage: {round(total_score / total_questions * 100, 2)}%")

        input("\nPress ENTER to return to the Main Menu...")

    elif choice == "8":
        print("\nThank you for using the Python Programming Reviewer!")
        print("Keep learning and practicing Python!")
        break

    else:
        print("\nInvalid choice. Please choose from 1 to 8.")