# First-trying-project

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error: Division by zero"
    return x / y

def power(x, y):
    return x ** y

def modulo(x, y):
    if y == 0:
        return "Error: Modulo by zero"
    return x % y

def calculator():
    print("=" * 40)
    print("         Python Calculator")
    print("=" * 40)
    
   while True:
        print("\nOperations:")
        print("1. Addition (+)")
        print("2. Subtraction (-)")
        print("3. Multiplication (*)")
        print("4. Division (/)")
        print("5. Power (^)")
        print("6. Modulo (%)")
        print("7. Exit")
        
   choice = input("\nEnter choice (1-7): ")
        
   if choice == '7':
            print("Thank you for using the calculator!")
            break
        
   if choice not in ['1', '2', '3', '4', '5', '6']:
            print("Invalid choice! Please try again.")
            continue
        
  try:
            num1 = float(input("Enter first number: "))
            num2 = float(input("Enter second number: "))
            
   if choice == '1':
                print(f"\n{num1} + {num2} = {add(num1, num2)}")
            elif choice == '2':
                print(f"\n{num1} - {num2} = {subtract(num1, num2)}")
            elif choice == '3':
                print(f"\n{num1} * {num2} = {multiply(num1, num2)}")
            elif choice == '4':
                result = divide(num1, num2)
                print(f"\n{num1} / {num2} = {result}")
            elif choice == '5':
                print(f"\n{num1} ^ {num2} = {power(num1, num2)}")
            elif choice == '6':
                result = modulo(num1, num2)
                print(f"\n{num1} % {num2} = {result}")
                
   except ValueError:
            print("Invalid input! Please enter numeric values.")
        except Exception as e:
            print(f"An error occurred: {e}")

if __name__ == "__main__":
    shivamcalculator()
