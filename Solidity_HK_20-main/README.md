# Solidity_Homework_20

## 1.) Associate Profit Splitter Contract 

--- 
--- 

The Associate Profit Splitter contract transfers an equal amount of Ether to three Associate-level employees within the company, with each of the employees  set as payable addresses variables so that the Ether can be transfered into each account. The Constructor funtion is used in order to call each of the employee addresses for Ether to be transfered. With the Balance fucntion, we return the current balance of the contract and return any remainders back to the sender. 

---

The Deposit function is executed in order to verify that the Ether is sent to the contract and returns zero. The function can only be called by the owner to transfer any funds to the employees. This used the Inject Web3 to deploy by connecting to Ganache and the localhost MetaMast 8485 and using the accounts available on Ganache for testing. After this, the Fallback function sends the Ether to the contract and tests the deposit, which Ganache verifies that each account received a third of each of the Ether. 

---
---
---

## 2.) Tiered Profit Splitter Contract 

--- 
--- 

The Tiered Profit Splitter contract transfers profits to the CEO, CTO, and Bob into three different Tiers for each employee. The Tiers for each of the employees are set at 60, 25, and 15. The profits are distributed as a percent based on each of the employees Tiers, and the amount to transfer to the employee is added to a total. The balance function will send the remianing balance to employee_one with the highest percentage tier. 

---

The deposit function is also uses the Inject Web3 to deploy by connecting to Ganache and the localhost MetaMast 8485 and using the accounts available on Ganache for testing and a value set at zero for each employee. After this, the Fallback function sends the Ether to the contract and tests the deposit, which Ganache verifies that each account received their proportion of the Ether based on their designated Tiers (60%, 25%, and 15%). 

---
---
---

## 3.) Deferred Equity Plan Contract 

---
---

The Deffered Equity Plan contract manages an employees' incentive plan by distributing 1000 shares equally over a 4 year period. The variables are set so that the distribution allocate 250 shares to the employee yearly. However, it will not allocate shares that exceed 1000 total shares, and it will not be distributed if the employee does not meet the time frame for the shares to be allocated. 

---

The distribute function will calculate the total shares that have been distributed over the period calculated from the start_time and used to calculate the unlock_time for next year's shares to be allocated. With the if statement, shares will not be released if it has been less than one year since the last allocation or if the total shares distributed will surpass 1000. 
