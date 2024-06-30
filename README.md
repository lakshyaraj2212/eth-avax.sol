# eth-avax.sol
#Overview.sol

The FunctionsAndErrors contract is a simple Solidity contract designed to demonstrate the usage of require, assert, and revert statements in Solidity. These statements are used to handle errors and enforce conditions within smart contract functions.

Contract Functions
requireNum(uint256 _num)
This function takes an unsigned integer as an input and checks if it is greater than a specified minimum value (1). If the condition is met, it returns the input number. Otherwise, it throws an error with a custom message.

Parameters:

_num: The input number to check.
Returns:

The input number if the condition is met.
Errors:

Throws an error with the message "Number must be greater than 1" if the input number is not greater than 1.
assertNum(uint256 _num)
This function takes an unsigned integer as an input, adds a specified value (5) to it, and asserts that the result is greater than the original input. If the assertion fails, it causes the contract to revert with an error.

Parameters:

_num: The input number to add to.
Returns:

The result of the input number plus the specified value.
Errors:

Throws an assertion error if the result is not greater than the input number.
revertError()
This function demonstrates the usage of the revert statement. It always reverts the transaction with a custom error message.

Errors:
Throws an error with the message "Transaction reverted."
Usage
To use the FunctionsAndErrors contract, you can deploy it on a compatible Ethereum network and interact with its functions as described. Here are some examples:

Example 1: Calling requireNum
solidity
Copy code
FunctionsAndErrors contract = new FunctionsAndErrors();
uint256 result = contract.requireNum(2); // Should return 2
Example 2: Calling assertNum
solidity
Copy code
FunctionsAndErrors contract = new FunctionsAndErrors();
uint256 result = contract.assertNum(3); // Should return 8 (3 + 5)
Example 3: Calling revertError
solidity
Copy code
FunctionsAndErrors contract = new FunctionsAndErrors();
contract.revertError(); // Should revert the transaction with "Transaction reverted."
