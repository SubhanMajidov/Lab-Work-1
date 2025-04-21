# calculator
Simple Calculator Code in Python

def calculator():
    print("1. Toplama")
    print("2. Çıxma")
    print("3. Vurma")
    print("4. Bölmə")

    choice = input("Hansı əməliyyatı etmək istəyirsiniz? ")

    if choice not in ['1', '2', '3', '4']:
        print("Yanlış daxiletmə")
        return

    try:
        num1 = float(input("Ilk rəqəmi daxil edin: "))
        num2 = float(input("Növbəti rəqəmi daxil edin: "))
    except ValueError:
        print("Yanlış nömrə daxiletməsi")
        return

    if choice == '1':
        result = num1 + num2
        print(f"Nəticə: {result}")
    elif choice == '2':
        result = num1 - num2
        print(f"Nəticə: {result}")
    elif choice == '3':
        result = num1 * num2
        print(f"Nəticə: {result}")
    elif choice == '4':
        if num2 == 0:
            print("Sıfıra bölmək olmaz")
        else:
            result = num1 / num2
            print(f"Nəticə: {result}")
            
calculator()
