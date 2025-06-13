import math

def get_positive_integer():
    while True:
        user_input = input("Введите положительное целое число: ")
        try:
            number = int(user_input)
            if number < 0:
                print("Ошибка: число не может быть отрицательным. Попробуйте снова.")
            else:
                return number
        except ValueError:
            print("Ошибка: введено не число. Попробуйте снова.")

def main():
    number = get_positive_integer()
    factorial_result = math.factorial(number)
    print(f"Факториал числа {number} равен: {factorial_result}")

if __name__ == "__main__":
    main()
