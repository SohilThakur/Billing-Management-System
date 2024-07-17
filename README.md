# Super Market Billing System

## Project Description

The Super Market Billing System is a C++ console application designed to manage and calculate bills for a supermarket. The application allows users to add items to a bill, update the inventory, and generate a total bill based on the items purchased. The data is stored in a text file to persist between sessions.

## Features

1. **Add Item to Inventory:**
   - Allows the user to add items to the supermarket's inventory.
   - The item details include the item name, rate, and quantity.
   - The details are stored in a file (`Bill.txt`).

2. **Print Bill:**
   - Users can create a bill by specifying items and their quantities.
   - The system checks if the item is available in the required quantity.
   - The bill is displayed along with the total amount.
   - The inventory is updated to reflect the items sold.

3. **Exit:**
   - Allows the user to exit the application.

## Files

- **main.cpp**: Contains the main code for the application.
- **Bill.txt**: Stores the inventory details (item name, rate, and quantity).

## Dependencies

- Windows operating system (for `Sleep` and `system("cls")` functions).
- C++ compiler (such as GCC or Visual Studio).

## How to Use

1. **Compile the Program:**
   - Open a terminal or command prompt.
   - Navigate to the directory containing `main.cpp`.
   - Compile the program using a C++ compiler. For example:
     ```bash
     g++ main.cpp -o SuperMarketBilling
     ```

2. **Run the Program:**
   - Execute the compiled program:
     ```bash
     ./SuperMarketBilling
     ```
   - Follow the on-screen prompts to add items, print bills, or exit the application.

## Functions

### Class: `Bill`

- **Private Members:**
  - `string Item`: Stores the item name.
  - `int Rate`: Stores the rate of the item.
  - `int Quantity`: Stores the quantity of the item.

- **Public Methods:**
  - `Bill()`: Constructor to initialize the item, rate, and quantity.
  - `void setItem(string item)`: Sets the item name.
  - `void setRate(int rate)`: Sets the item rate.
  - `void setQuant(int quant)`: Sets the item quantity.
  - `string getItem()`: Returns the item name.
  - `int getRate()`: Returns the item rate.
  - `int getQuant()`: Returns the item quantity.

### Function: `addItem(Bill b)`

- Adds an item to the inventory.
- Prompts the user for item details and updates the inventory file (`Bill.txt`).

### Function: `printBill()`

- Creates and prints a bill.
- Prompts the user for items and quantities.
- Displays the bill and updates the inventory.

### Function: `main()`

- Main function to drive the program.
- Provides a menu for the user to add items, print bills, or exit the application.

## Notes

- Ensure the file paths in the program are correctly set according to your system.
- The application uses `system("cls")` and `Sleep()` functions which are specific to Windows. For cross-platform compatibility, consider replacing these with appropriate alternatives.
