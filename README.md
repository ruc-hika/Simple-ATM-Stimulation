# Simple-ATM-Stimulation
balance = 1000  # initial balance

while True:
    print("\n--- ATM MENU ---")
    print("1. Check Balance")
    print("2. Deposit")
    print("3. Withdraw")
    print("4. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        print(f"Your balance: {balance}")
    elif choice == "2":
        amt = float(input("Enter deposit amount: "))
        balance += amt
        print(f"Deposited {amt}. New balance: {balance}")
    elif choice == "3":
        amt = float(input("Enter withdrawal amount: "))
        if amt > balance:
            print("Insufficient funds!")
        else:
            balance -= amt
            print(f"Withdrew {amt}. New balance: {balance}")
    elif choice == "4":
        print("Thank you for using ATM. Goodbye!")
        break
    else:
        print("Invalid choice, try again.")
