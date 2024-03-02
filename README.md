# import math

def calculator():
    print("Welcome to the Advanced Calculator!")
    print("Choose operation:")
    print("1. Addition (+)")
    print("2. Subtraction (-)")
    print("3. Multiplication (*)")
    print("4. Division (/)")
    print("5. Exponentiation (x^y)")
    print("6. Square Root (√)")
    print("7. Trigonometric Functions (sin, cos, tan)")
    choice = input("Enter choice (1/2/3/4/5/6/7): ")

    if choice in ['1', '2', '3', '4']:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

    if choice == '1':
        print("Result:", num1 + num2)
    elif choice == '2':
        print("Result:", num1 - num2)
    elif choice == '3':
        print("Result:", num1 * num2)
    elif choice == '4':
        if num2 == 0:
            print("Error: Division by zero!")
        else:
            print("Result:", num1 / num2)
    elif choice == '5':
        num1 = float(input("Enter base: "))
        num2 = float(input("Enter exponent: "))
        print("Result:", num1 ** num2)
    elif choice == '6':
        num = float(input("Enter number: "))
        if num < 0:
            print("Error: Cannot compute square root of a negative number!")
        else:
            print("Result:", math.sqrt(num))
    elif choice == '7':
        angle = float(input("Enter angle in degrees: "))
        print("Trigonometric Functions:")
        print("sin({}) = {}".format(angle, math.sin(math.radians(angle))))
        print("cos({}) = {}".format(angle, math.cos(math.radians(angle))))
        print("tan({}) = {}".format(angle, math.tan(math.radians(angle))))
    else:
        print("Invalid choice!")

calculator()
