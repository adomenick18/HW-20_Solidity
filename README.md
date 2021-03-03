# HW-20_Solidity

## Contract number 1:

Due to time constraints with work, I was only able to complete the first contract before the HW due date.  Nevertheless, it's a tremendous contract!  

The way that the contract works is that the user deposits ether from a sender address and equal amounts get sent to three other wallets.  Any left over ether gets sent back to the sender's wallet.  The use case for this contract is for Associates to split company profits equally when they are paid.

Three payable addresses were created; employee one, employee two and employee three.  The deposit function is where the contract gets executed.  Initially, we required the msg.value to be greater than 0 because we don't want the Associates to get no payout.  The value is then divided by three and transferred to each employee.  Finally, if there is any remainder, that amount is sent back to the sender.

In addition to the contract logic, we added a fallback function to call the deposit function if ether is sent to the contract with no other information.

Prior to the contract deposit I had three accounts with amounts shown below.

![pic-1](ganache_b4_tx.jpg)

Below is how the contract is executed using remix.  The user enters the amount in the "value" field circled in red and presses the "deposit" button, also circled in red.

![pic-2](remix_value_input.jpg)

The user needs to confirm the transaction using their metamask extension as shown below.

![pic-3](metamask_confirm.jpg)

Once confirmed the deposited amount is split between the three wallets!

![pic-3](ganache_after_tx.jpg)

