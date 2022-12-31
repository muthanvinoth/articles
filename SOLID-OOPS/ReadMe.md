# S.O.L.I.D principles & OOPS

I am writing this article to showcase my understanding of solid principles and oops principles.
 I prefer C# as the programming language for all examples below. 
 
 Let's assume we are building a simple banking application, Deposit and Withdraw are the only primary functions of this imaginary bank account. 
 
 ## Problem Statement

 Below problem statement has three different types of bank accounts.

```
 
Bank Accounts
	* Deposit
	* Withdraw

1) Savings account, for people who do not have a regular income or who wish to maintain a secondary account for day-to-day purposes 
	- Deposit : Any deposit above $10,000 will attract tax.
	- withdraw : Can withdraw till 0 balance but a nominal charge will be applied if the balance is below $1000

2) Salary account, for salaried employees, whose wages will be deposited by the employer directly
	- deposit : Any deposit above $10,000 will attract tax.
	- withdraw : Can withdraw till 0, no charges

3) Current account , for business 
	- deposit : none
	- withdraw : can withdraw  negative -$10000  

```

## Deposit

The above problem statement has three different 
