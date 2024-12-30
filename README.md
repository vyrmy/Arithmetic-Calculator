# Arithmetic-Calculator
# This is a simple arithmetic calculator that can handle, as the name suggests, arithmetic operations. Such as +,-,*, and /.

```python
numInput1 = input("Enter a number: ")

while True:
    if numInput1.isdigit():
        break
    else:
        print(f"{numInput1} is not a number. Try again.")
        numInput1 = input("Enter a number: ")

operatorInput = input("Enter an operator (+,-,*,/): ")

while operatorInput not in ['+','-','*','/']:
    print("Invalid operator. Try again.")
    operatorInput = input("Enter an operator (+,-,*,/): ")
    
numInput2 = input("Enter a number: ")

while True:
    if numInput2.isdigit():
        break
    else:
        print(f"{numInput2} is not a number. Try again.")
        numInput2 = input("Enter a number: ")
        
def process(x,y):
    if operatorInput == '+':
        print(f"Result: {x + y}")
    elif operatorInput == '-':
        print(f"Result: {x - y}")
    elif operatorInput == '*':
        print(f"Result: {x * y}")
    elif operatorInput == '/':
        if y == 0:
            print("Undefined.")
        else:
            print(f"Result: {x / y}")
            
x = int(numInput1)

y = int(numInput2)

process(x,y)
