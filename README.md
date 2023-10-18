# green-bearcat-banking-app
Banking App from Team Green Bearcat


Data model


Contexts:
Identity
Bank


Models
Identity
	User
		ID

Bank
	Accounts
		Owned by 1 user
		Accessible by multiple users
		Read/Write Access levels
		Balance
	Transactions
		From account
		To account
		Timestamp
		Amount
		Currency
		By User
	
	
Events

	Transactions
		1. Freeze the amount on sender account and remove from balance
		2. Add to receiving account
		3. Deduct from sending account and remove freeze
		4. Validate and log
	Deposit
		1. Add to receiving account
		2. Validate and log
	Withdrawal
		1. Freeze the amount on sender account and remove from balance
		2. Deduct from sending account and remove freeze
		3. Validate and log
	Open account
	Close account
	Prorate
		1. Validate balances
		2. Calculate interest
		3. Add amount to account
		4. Validate and log
