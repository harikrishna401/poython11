# poython11
# Program 9: Reverse a String
def reverse_string(s):
    return s[::-1]

input_str = input("Enter a string to reverse: ")
reversed_str = reverse_string(input_str)
print(f"The reversed string is: {reversed_str}")


# Program 10: Convert Celsius to Fahrenheit
def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

celsius = float(input("Enter temperature in Celsius: "))
fahrenheit = celsius_to_fahrenheit(celsius)
print(f"{celsius} degrees Celsius is equal to {fahrenheit} degrees Fahrenheit")


# Program 11: Check Armstrong Number
def is_armstrong_number(num):
    order = len(str(num))
    sum = 0
    temp = num
    while temp > 0:
        digit = temp % 10
        sum += digit ** order
        temp //= 10
    return num == sum

num = int(input("Enter a number to check if it's an Armstrong number: "))
if is_armstrong_number(num):
    print(f"{num} is an Armstrong number")
else:
    print(f"{num} is not an Armstrong number")

# Program 12: Calculate Factorial
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n-1)

num = int(input("Enter a number to calculate its factorial: "))
fact = factorial(num)
print(f"The factorial of {num} is: {fact}")

# Program 13: Bubble Sort
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

# Example usage:
num_list = [int(x) for x in input("Enter numbers separated by space: ").split()]
bubble_sort(num_list)
print("Sorted array:", num_list)
