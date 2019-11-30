# Fintech_project
Progress about project
### first commit -- vittoriocolombo11

The code inside Insurance.txt is the first raw version of the Police Report. The contract contains information such as:
  - first vehicle
  - second vehicle
  - who's fault is
  - damage amount
  - the owner of the contract (aka the police)
  - the time in which the contract was deployed
  
Only the Police can modify the existing contract, I have done it via the modfifier OnlyOwner. In fact, if you deploy the contract 
using one account, and then switch to another and try to modify values stored inside it, it will raise an error.
