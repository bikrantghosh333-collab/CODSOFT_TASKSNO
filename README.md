#PROJECT-1: CAlCULATOR 

def addition(num1, num2):
    return num1 + num2

def subtraction(num1, num2):
    return num1 - num2

def multiplication(num1, num2):
    return num1 * num2

def division(num1, num2):
    if num2 == 0:
        return "Error: Division by zero is not allowed."
    else:
        return num1 / num2

def percentage(num1, num2):
    if num2 == 0:
        return "Error: Division by zero is not allowed."
    else:
        return (num1 / num2) * 100

def modulus(num1, num2):
    if num2 == 0:
        return "Error: Division by zero is not allowed."
    else:
        return num1 % num2

def exponentiation(num1, num2):
    return num1 ** num2

def floor_division(num1, num2):
    if num2 == 0:
        return "Error: Division by zero is not allowed."
    else:
        return num1 // num2


# Main loop
choice = '0'
while choice != '9':
    print("\nSelect operation:")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")
    print("5. Percentage")
    print("6. Modulus")
    print("7. Exponentiation")
    print("8. Floor Division")
    print("9. Exit")

    choice = input("Enter choice (1-9): ")

    if choice in ('1', '2', '3', '4', '5', '6', '7', '8'):
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

        if choice == '1':
            print("RESULT:", addition(num1, num2))
        elif choice == '2':
            print("RESULT:", subtraction(num1, num2))
        elif choice == '3':
            print("RESULT:", multiplication(num1, num2))
        elif choice == '4':
            print("RESULT:", division(num1, num2))
        elif choice == '5':
            print("RESULT:", percentage(num1, num2))
        elif choice == '6':
            print("RESULT:", modulus(num1, num2))
        elif choice == '7':
            print("RESULT:", exponentiation(num1, num2))
        elif choice == '8':
            print("RESULT:", floor_division(num1, num2))

    elif choice == '9':
        print("Exiting the calculator. Goodbye!")

    else:
        print("Invalid input. Please enter a valid choice from 1 to 9.")



# Run the game
play_game()


