ETH-AVAX INTERMEDIATE 1

ErrorHandling Contract This is a Solidity smart contract that demonstrates use of assert, revert, and require statements.

License: This contract is using the MIT License.

Prerequisites Solidity ^0.8.18

Here's how the code works:
•	Function names deposit, withdraw, checkBalance are renamed to addFunds, takeFunds, getFunds respectively to make them more intuitive.
•	The balance variable has been renamed to totalFunds to better reflect its purpose.
•	In the takeFunds function, I've introduced a new boolean variable fundsSufficient for better readability.
•	For the getFunds function, we have used an assert statement which checks if our contract's totalFunds is always greater than or equal to 0, as this is what we'd always expect.

In Solidity, error handling is performed using require(), revert() and assert(). 
These are functions used to handle errors and exceptions during contract execution. 
They play an important role in ensuring that a contract functions correctly, and resources are not wasted due to faulty execution.

require(): require() is used to validate inputs and conditions before execution. 
If the condition inside require() fails, then the whole transaction or operation is reverted. 
It consumes less gas, as it doesn't process the entire function before encountering the error.

revert(): revert() is used when a condition fails and an operation needs to be reverted. 
At this point, the state of the blockchain remains unchanged, but all gas consumed till the point of reverting is wasted.

assert(): assert() is used for internal error checking and for conditions that are never supposed to fail. 
If an assert() fails, all gas is consumed and the transaction is compeletly reverted.


Video walkthrough of the code is given as:
https://www.loom.com/share/a64baec3ec0c4aeaa28c242b51ec204d
