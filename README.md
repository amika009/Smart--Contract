Assessment Contract


This contract is a simple banking system that allows the owner to deposit and withdraw funds. It also provides functions to retrieve the current balance, gas price of the transaction, and the current block number.



Functions
Constructor
constructor(uint initBalance) payable: Initializes the contract with an initial balance set by the owner.




Deposit
function deposit(uint256 _amount) public payable: Allows the owner to deposit funds into the contract. Emits a Deposit event with the deposited amount.




Withdraw
function withdraw(uint256 _withdrawAmount) public: Allows the owner to withdraw funds from the contract. Reverts with a custom InsufficientBalance error if the balance is insufficient. Emits a Withdraw event with the withdrawn amount.




Get Balance
function getBalance() public view returns(uint256): Returns the current balance of the contract.




Get Gas Price
function getgasPriceTransaction() public view returns(uint): Returns the gas price of the current transaction.





Get Current Block
function getCurrentBlock() public view returns(uint): Returns the current block number.





Events
Deposit
event Deposit(uint256 amount): Emitted when a deposit is made, with the deposited amount as an argument.




Withdraw
event Withdraw(uint256 amount): Emitted when a withdrawal is made, with the withdrawn amount as an argument.
Error





InsufficientBalance

error InsufficientBalance(uint256 balance, uint256 withdrawAmount): Custom error thrown when the balance is insufficient for a withdrawal, with the current balance and requested withdrawal amount as arguments.
error InsufficientBalance(uint256 balance, uint256 withdrawAmount): Custom error thrown when the balance is insufficient for a withdrawal, with the current balance and requested withdrawal amount as arguments.
