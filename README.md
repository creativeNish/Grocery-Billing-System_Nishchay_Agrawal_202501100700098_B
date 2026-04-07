Problem Statement:
Design and implement a Smart Payment Processing System using Object-Oriented Programming (OOP) concepts in Python. The system should allow users to make payments using different methods such as Credit Card, UPI, PayPal, and Digital Wallet. Each payment method follows a common interface but implements its own business logic for computing the final payable amount.

Requirements:

Abstract base class Payment:


Stores the user name.

Declares abstract method pay(amount).

Contains concrete method generate_receipt().

Payment Types:

CreditCardPayment:

2% gateway fee + 18% GST on fee.

Final amount = original + fee + GST.

UPIPayment:

Cashback ₹50 if amount > 1000.

Final amount = original - cashback.

PayPalPayment:

3% international fee + ₹20 conversion fee.

Final amount = original + fees.

WalletPayment:

Maintains wallet balance.

Deducts amount if balance sufficient, else fails.

Function process_payment(payment, amount):


Accepts any payment object.

Calls pay() method.

Demonstrates runtime polymorphism.

Approach:

Abstraction: Payment as abstract base class.

Inheritance: Specialized payment classes inherit Payment.

Polymorphism: process_payment() adapts to different payment types.

Encapsulation: User details and transaction logic secured in classes.

Sample Output:

UPI Payment:

Processing UPI Payment... No Cashback Applied

------ PAYMENT RECEIPT ------ 

User Name : Nishchay Agrawal

Original Amount : ₹500.0

Final Amount : ₹500.0

Credit Card Payment:

Processing Credit Card Payment...

Gateway Fee: ₹10.0 GST on Fee: ₹1.8


------ PAYMENT RECEIPT ------ 

User Name : Nishchay Agrawal

Original Amount : ₹500.0 

Final Amount : ₹511.8

PayPal Payment:

Processing PayPal Payment... 

Transaction Fee: ₹15.0 

Conversion Fee: ₹20.0


------ PAYMENT RECEIPT ------ 

User Name : Nishchay Agrawal

Original Amount : ₹500.0 

Final Amount : ₹535.0

Wallet Payment:

Processing Wallet Payment... 

Transaction Successful! 

Remaining Balance: ₹1500.0


------ PAYMENT RECEIPT ------ 

User Name : Palak Pandey 

Original Amount : ₹500.0 

Final Amount : ₹500.0


Key Concepts Demonstrated:

Abstraction

Inheritance

Polymorphism

Encapsulation
