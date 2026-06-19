Expense Tracker

A simple Python application that helps users manage expenses.

Features

- Add expenses
- View expenses
- Calculate total expenses
- Exit the application

Technologies Used

- Python

Author

Pranavi Rao.

code:




expenses = []

while True:
    print("\n===== Expense Tracker =====")
    print("1. Add Expense")
    print("2. View Expenses")
    print("3. Show Total")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        name = input("Enter expense name: ")
        amount = float(input("Enter amount: "))

        expenses.append((name, amount))
        print("Expense Added!")

    elif choice == "2":
        print("\nExpenses:")

        for name, amount in expenses:
            print(name, "-", amount)
    
    elif choice == "3":
        total = 0
        for name, amount in expenses:
             total += amount

        print("Total Expenses:", total)
    
    elif choice == "4":
        print("Thank you for using Expense Tracker!")           
    else:
        print("Invalid Choice! Please enter 1, 2, 3, or 4.")
        break 