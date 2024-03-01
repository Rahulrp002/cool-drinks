**Cool Drinks Festival Contract**

This contract is designed for managing the operations of a cool drinks festival, where participants can purchase cups and consume drinks. Below is a detailed explanation of the contract and its functions:

**Contract Overview:**
- **Language:** Solidity
- **Version:** 0.8.0
- **License:** MIT

**Functions:**

1. **setCupPrice:**  
   - **Description:** Sets the price for a cup that participants need to purchase in order to consume drinks at the festival.
   - **Input:** `_cupPrice` (uint256) - The price of a cup.
   - **Modifiers:** External - The function can be called externally.
   - **Requirements:** The cup price must be greater than zero.
   - **Implementation:** Uses the `require` statement to ensure the cup price meets the specified requirement. Then, sets the cup price accordingly.

2. **DrinksQuantity:**  
   - **Description:** Records the quantity of drinks consumed by participants at the festival.
   - **Input:** `_drinksQuantity` (uint256) - The quantity of drinks consumed.
   - **Modifiers:** External - The function can be called externally.
   - **Special Conditions:**
       - Uses the `assert` statement to ensure that the drinks quantity exceeds 500.
       - Employs the `revert` statement to offer a discount if the drinks quantity equals 1000.
   - **Implementation:** 
       - Utilizes the `assert` statement to validate the drinks quantity.
       - If the drinks quantity is exactly 1000, it reverts the transaction with a message offering a discount on the next cup purchase.
       - Sets the consumed drinks quantity accordingly.

**README Instructions:**

1. **Deployment:**
   - Deploy the contract to a compatible blockchain network using a Solidity compiler.
   - Ensure to set the initial cup price after deployment using the `setCupPrice` function.

2. **Usage:**
   - After deployment, participants can interact with the contract by calling the `setCupPrice` and `DrinksQuantity` functions.
   - The `setCupPrice` function is used to set the price of a cup required for accessing drinks.
   - The `DrinksQuantity` function records the quantity of drinks consumed by participants.

**License:**
- This contract is released under the MIT License, allowing for modification and distribution under certain conditions. See the `LICENSE` file for details.
