# Banking-System-Using-Python

Banking System in Python
This project is a Python-based banking system that demonstrates object-oriented programming concepts through the simulation of a banking application. The system supports multiple account types, including Savings and Checking accounts, and provides functionalities like deposits, withdrawals, interest calculations, and overdraft management.

Features
1. Account Types
Savings Account: Includes functionality for deposits, withdrawals, and applying interest based on a specified interest rate.
Checking Account: Allows deposits, withdrawals, and supports overdraft functionality within a defined limit.
2. Key Functionalities
Deposit: Add funds to an account while preventing negative deposits.
Withdraw: Withdraw funds, with safeguards against negative or excessive withdrawals.
Interest Application: For savings accounts, apply interest to the current balance.
Overdraft Handling: For checking accounts, enable overdrafts up to a specified limit.
Account Details: Display comprehensive account details, including account holder name, number, balance, and specific attributes like interest rate or overdraft limit.
3. Abstract Base Class
The system employs the abc module to define a base BankAccount class, enforcing the implementation of core methods (deposit and withdraw) in derived classes.
4. User Simulation

Sample accounts demonstrate functionality:
A savings account for "Shivani" showcasing deposits, withdrawals, and interest application.
A checking account for "Raushani" demonstrating overdraft usage and account balance management.

Code Highlights
The BankAccount class serves as an abstract base class, encapsulating shared attributes and methods.
SavingAccount and CheckingAccount classes extend BankAccount, providing specialized implementations for account-specific behaviors.
Clean and modular design promotes code reusability and scalability.
Sample Usage
python
Copy code
# Create a Savings Account
shivani_saving_account = SavingAccount("Shivani", 7548865423)
shivani_saving_account.deposit(50000)
shivani_saving_account.withdraw(30000)
shivani_saving_account.apply_interest()
print(shivani_saving_account.get_account_details())

# Create a Checking Account
raushani_checking_account = CheckingAccount("Raushani", 546987561236)
raushani_checking_account.deposit(75000)
raushani_checking_account.withdraw(50000)
raushani_checking_account.withdraw(75000)  # Utilizing overdraft
print(raushani_checking_account.get_account_details())

Requirements
Python 3.6 or higher
No additional libraries are required; the implementation uses only standard Python modules.

Future Enhancements
Add graphical or web-based interfaces.
Implement account authentication for security.
Integrate with a database for persistent storage.
Add support for more account types and advanced financial operations.
