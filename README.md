# Bank Management System

## Description
This project is a simple banking management system that allows users to manage their accounts efficiently. The system includes features such as creating accounts, performing transactions, managing user data, and providing a secure interface for bank managers.

---

## Implementation Steps

### Step 1: Create Database Class
The **Database Class** is responsible for managing user data, including saving, loading, and authentication. It interacts with files (`users.txt` and `managers.txt`) to store and retrieve user information.

#### Key Functionalities
1. **saveUsersToFile**
   - Saves all usernames, passwords, and account balances to `users.txt`.

2. **loadUsersFromFile**
   - Reads login information from `users.txt` and populates an unordered map of users.

3. **loadManagersFromFile**
   - Reads manager login data from `managers.txt` and populates an unordered map of managers.

4. **createUser**
   - Receives a `username` and `password` as input, initializes the user's account balance to `0`, and saves the information to the database.

5. **deleteUser**
   - Removes a provided user from the database. This is used when a user requests to close their account.

6. **login**
   - Prompts the user to enter a username and password.
   - Checks if the provided credentials exist in the system.
   - If the credentials are incorrect, it allows the user to try again. If correct, the user is successfully logged into their account.

---

### Step 2: Define Transaction Class
The **Transaction Class** manages and tracks transactions made by users.

#### Key Functionalities
- Tracks the type of transaction performed (e.g., deposit, withdrawal).
- Records the amount of money involved in each transaction.

---

### Step 3: Create Bank Account Class
The **Bank Account Class** handles the structure and functionalities of individual bank accounts. It defines the various actions that users can perform once logged in.

#### Key Functionalities
1. **Withdraw**
   - Removes a specified amount of funds from the user's account if they have sufficient balance.

2. **Deposit**
   - Adds a specified amount of money to the user's account. This operation succeeds only if the account is currently open. Otherwise, the user is notified of the error.

3. **PrintAccountSummary**
   - Displays the user's complete transaction history as well as their current account balance.

4. **CloseAccount**
   - Closes the user’s account if requested and removes their login data from the database.

5. **setUsername**
   - Updates the account with a username chosen by the user.

---

### Step 4: Define Bank Manager Class
The **Bank Manager Class** is designed for bank managers to securely access user data and perform administrative tasks.

#### Key Functionalities
1. **login**
   - Prompts the manager for a username and password.
   - Verifies the credentials against the data in `managers.txt`. If correct, the manager is successfully logged into their account.

2. **loadManagersFromFile**
   - Reads manager login data from `managers.txt` and stores it in an unordered map of managers.

#### How to Set Up Manager Credentials
1. Create a `managers.txt` file in the project directory.
2. Add manager credentials in the format:
Each pair of credentials must be separated by a space.

3. Place the file in the same directory as the program to allow manager logins.

---

### Step 5: Finalize The Banking Simulation
To complete the banking simulation, we will display a menu of banking and account options. The user will choose from the available options by entering the corresponding number.

#### User Choices
When logged in, the user will see a list of choices such as:
1. **Withdraw funds**
2. **Deposit funds**
3. **Print account summary**
4. **Close account**
5. **Log out**

Managers will have a separate set of options to view and manage user data.

---

### Step 6: Testing Our Implementation
Testing is essential to ensure the banking system works as expected. Follow these steps to test the implementation:


