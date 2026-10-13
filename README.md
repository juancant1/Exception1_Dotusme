# Exception1_Dotusme

1. The Custom Exception (InvalidCargoException) For the first requirement, I created a custom checked exception by extending the base Exception class. Basically, I set up a constructor that takes a string message so that whenever an invalid cargo slot is requested, it can pass a clear error description up the chain. 

2. Array Validation (inspectCargoSlot) I initialized a static array called cargoWeights with four preset values. The inspectCargoSlot method takes the slot index you type in and checks if it's less than 0 or bigger than the array's length. If it is out of bounds, it throws my InvalidCargoException. If it's valid however, it just prints out the weight at THAT specific slot. 

3. Flight Efficiency Calculation (calculateEfficiency) For this part, this method divides the total energy used by the distance traveled. I didn't put a try-catch block inside this method; instead, I explicitly checked if the distance is 0.0. If it is, I throw an ArithmeticException so it bubbles straight up to the main menu loop instead of handling it locally. 

4. The Main Console Loop (main) Everything runs inside a while loop using a Scanner so the menu keeps popping up until you choose to exit. I used a switch statement to handle the user's menu choices. I also wrapped the calls to inspectCargoSlot and calculateEfficiency in try-catch blocks. That way, if a custom exception or an arithmetic exception gets thrown, the program catches it, prints the error message, and goes right back to the menu.

