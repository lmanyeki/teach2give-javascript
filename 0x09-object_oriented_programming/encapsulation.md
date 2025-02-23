# Encapsulation 

Encapsulation refers to the practice of hiding the internal details of an object and exposing only the necessary information to the outside world.

### Using closures

Closures are functions that have access to variables in their outer lexical environment, even after the outer function has returned. 

Private variables and methods can be created using closures.
```js
function BankAccount(accountNumber, accountHolderName, balance) {
    let _accountNumber = accountNumber;
    let _accountHolderName = accountHolderName;
    let _balance = balance;
 
    function showAccountDetails() {
        console.log(`Account Number: ${_accountNumber}`);
        console.log(`Account Holder Name: ${_accountHolderName}`);
        console.log(`Balance: ${_balance}`);
    }
 
    function deposit(amount) {
        _balance += amount;
        showAccountDetails();
    }
 
    function withdraw(amount) {
        if (_balance >= amount) {
            _balance -= amount;
            showAccountDetails();
        } else {
            console.log("Insufficient Balance");
        }
    }
 
    return {
        deposit: deposit,
        withdraw: withdraw
    };
}
 
let myBankAccount = BankAccount("123456", "John Doe", 1000);
 
myBankAccount.deposit(500); 
// Output: Account Number: 123456 Account Holder Name: 
//John Doe Balance: 1500
 
myBankAccount.withdraw(2000); // Output: Insufficient Balance
```
Output
```
Account Number: 123456
Account Holder Name: John Doe
Balance: 1500
Insufficient Balance
```

### Using classes
```js
class BankAccount {
    constructor(accountNumber, accountHolderName, balance) {
        this._accountNumber = accountNumber;
        this._accountHolderName = accountHolderName;
        this._balance = balance;
    }
 
    showAccountDetails() {
        console.log(`Account Number: ${this._accountNumber}`);
        console.log(`Account Holder Name: ${this._accountHolderName}`);
        console.log(`Balance: ${this._balance}`);
    }
 
    deposit(amount) {
        this._balance += amount;
        this.showAccountDetails();
    }
 
    withdraw(amount) {
        if (this._balance >= amount) {
            this._balance -= amount;
            this.showAccountDetails();
        } else {
            console.log("Insufficient Balance");
        }
    }
}
 
let myBankAccount = new BankAccount("123456", "John Doe", 1000);
myBankAccount.deposit(500); 
// Output: Account Number: 123456 Account Holder Name: 
//John Doe Balance: 150
```
Output
```
Account Number: 123456
Account Holder Name: John Doe
Balance: 1500
```