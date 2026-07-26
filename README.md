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

#PROJECT-2: PASSWORD GENERATOR

import random 
import string 
length = int(input("Enter the password length: "))

characters = string.ascii_letters + string.digits + string.punctuation
password = ''.join(random.choice(characters) for i in range(length))
print("Generated password:", password)

#ROCK PAPER SCISSOR GAME
import random

def play_game():
    user_score = 0
    computer_score = 0

    while True:
        print("\nRock, Paper, Scissors Game")
        print("1. Rock")
        print("2. Paper")
        print("3. Scissors")
        print("4. Exit")

        user_choice = input("Enter your choice (1-4): ")

        if user_choice == '4':
            print("Exiting the game.")
            break

        if user_choice not in ['1', '2', '3']:
            print("Invalid choice. Please try again.")
            continue

        computer_choice = str(random.randint(1, 3))

        choices = {'1': 'Rock', '2': 'Paper', '3': 'Scissors'}
        print(f"You chose: {choices[user_choice]}")
        print(f"Computer chose: {choices[computer_choice]}")

        if user_choice == computer_choice:
            print("It's a tie!")
        elif (user_choice == '1' and computer_choice == '3') or \
             (user_choice == '2' and computer_choice == '1') or \
             (user_choice == '3' and computer_choice == '2'):
            print("You win!")
            user_score += 1
        else:
            print("Computer wins!")
            computer_score += 1

    print(f"\nFinal Scores:")
    print(f"You: {user_score}")
    print(f"Computer: {computer_score}")


# Run the game
play_game()


