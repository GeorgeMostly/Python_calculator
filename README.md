def calculate(num1, num2, operator):
    if operator == "+":
        return num1 + num2
    elif operator == "-":
        return num1 - num2
    elif operator == "*":
        return num1 * num2
    elif operator == "/":
        if num2 != 0:
            return num1 / num2
        else:
            return "Error: Division by zero"
    else:
        return "Invalid operator"

print("Welcome to the Python Calculator!")

while True:
    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operator = input("Enter the operator (+, -, *, /): ")
        result = calculate(num1, num2, operator)
        print(f"The result is: {result}")
    except ValueError:
        print("Invalid input! Please enter numeric values.")
    if input("Do you want to perform another calculation? (yes/no): ").lower() != "yes":
        break

print("Goodbye!")

 
