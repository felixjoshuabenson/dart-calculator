# dart-calculator
A Dart calculator project for Flutter mobile app development beginners.
This is a beginner-friendly console-based calculator built in Dart. It is designed to help new Flutter and Dart developers understand fundamental programming concepts. The project demonstrates key Dart features such as variables, built-in types, operators, and control flow, which are essential for building Flutter mobile applications. By exploring this project, you'll see how these concepts are applied in a practical, interactive program that performs basic arithmetic operations.

This project is perfect for those new to Dart and Flutter, as it introduces core programming ideas in a simple, easy-to-follow way. The code is well-commented and aligns with the Dart basics covered in my [LinkedIn post on Dart Basics](https://linkedin.com/in/felix-joshua-benson-2a9547146/)..

# Features
The Dart Calculator:
- Accepts two numbers as input from the user.
- Supports six operations: addition (`+`), subtraction (`-`), multiplication (`*`), division (`/`), modulus (`%`), and exponentiation (`**`).
- Handles errors, such as division by zero, with clear user feedback.
- Allows users to exit the program at any time by typing `exit`.
- Returns to the main menu after each operation, enabling multiple calculations in one session.

# Learning Objectives
This project is designed to help you understand the following Dart concepts, as outlined in the Dart Programming Notes:

1. Variables:
   - The calculator uses `double` variables to store user inputs (e.g., `firstNum` and `secondNum`), demonstrating how to declare and initialize variables.
   - The `late` keyword is used for instance fields (`num1` and `num2`) in the `Calc` class, showing how to initialize variables later.
   - Example: `late double num1;` is initialized in the constructor, aligning with the note's explanation of `late` variables.

2. Built-in Types:
   - The project uses `double` for numerical inputs (floating-point numbers), `String?` for user input (nullable strings), and `bool` for conditional checks.
   - Example: `String? firstInput` is nullable, reflecting Dart's null safety feature (as noted in "From Dart 2.12, variables are non-nullable by default unless marked with ?").

3. Operators:
   - Arithmetic operators (`+`, `-`, `*`, `/`, `%`) are implemented in methods like `add`, `subtract`, `multiply`, `divide`, and `modulus`.
   - The exponentiation operation (`**`) uses the `pow` function from `dart:math`, showcasing how to handle advanced arithmetic.
   - Example: `double divide(double firstNum, double secondNum) { return firstNum / secondNum; }` uses the division operator (`/`).

4. Control Flow:
   - A `switch` statement handles user-selected operations, demonstrating how to manage multiple conditions based on a single value (as described in the notes).
   - Exception handling with `try`, `catch`, and `if` checks prevents division by zero, aligning with the note's explanation of exception handling.
   - Example: The `switch (operator)` block uses `case` and `break` to execute the chosen operation, and `if (secondNum == 0)` prevents invalid division.

# Project Structure
- main.dart: The entry point of the program, which calls the `wholeThing` method to start the calculator.
- calc.dart: Contains the `Calc` class with methods for arithmetic operations and the main logic for user interaction.

# Prerequisites
To run this project, you need:
- Dart SDK installed (version 2.12 or later for null safety support).
- A code editor like Visual Studio Code or IntelliJ with the Dart extension.
- Basic familiarity with Dart syntax (refer to the Dart Programming Notes for guidance).

## How to Run
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/your-username/dart-calculator.git
   ```
2. Navigate to the project directory:
   ```bash
   cd dart-calculator
   ```
3. Run the program using the Dart CLI:
   ```bash
   dart run main.dart
   ```
4. Follow the on-screen prompts to:
   - Enter two numbers.
   - Choose an operation (`+`, `-`, `*`, `/`, `%`, or `**`).
   - Type `exit` to quit or continue with more calculations.

# Code Walkthrough
Here’s a quick overview of how the code ties to Dart basics:

- Class and Variables:
  - The `Calc` class uses `late double` instance fields (`num1`, `num2`) to store numbers, initialized in the constructor.
  - Example: `Calc calc1 = new Calc(firstNum, secondNum);` creates an instance with user-provided numbers.

- Input Handling:
  - The program uses `stdin.readLineSync()` to read user input as `String?`, which is then parsed to `double` using `double.parse()`.
  - Null safety is handled with the `!` operator (e.g., `double.parse(firstInput!)`) after checking for `exit`.

- Arithmetic Operations:
  - Methods like `add`, `subtract`, `multiply`, `divide`, `modulus`, and `exponentiate` use Dart’s arithmetic operators.
  - Note: The method `expontentiate` in the code should be corrected to `exponentiate` for clarity (a typo in the original code).

- Control Flow:
  - The `switch` statement in `wholeThing` selects the operation based on user input.
  - Division by zero is checked with an `if` condition, displaying an error message if `secondNum == 0`.
  - The `backToMainMenu` method loops back to the start, demonstrating recursion for repeated calculations.

- Error Handling:
  - The program checks for invalid inputs (e.g., non-numeric input via `double.parse`) and division by zero, aligning with the note’s exception handling section.

# Example Usage
```plaintext
Welcome to the Dart Calculator!

=============================== 

This calculator performs operations on two numbers. 
Please type your first number 
Type 'exit' to exit at anytime! 

10
Great! Now input your second number.

5
Awesome! Now, choose the operation you want.

Type + for addition
Type - for subtraction
Type * for multiplication
Type % for modulus
Type ** to raise the first number to the power of the second
Type / to divide
+
10.0 plus 5.0 equals = 15.0
Returning to main menu...
```

# Learning Extensions
To deepen your understanding, try these exercises:
1. Add input validation to handle non-numeric inputs using `try`/`catch` (see the note’s section on exception handling).
2. Extend the calculator to support additional operations, like square root (using `dart:math`).
3. Modify the program to store calculation history in a `List<double>` (see the note’s section on Lists).
4. Convert this console app into a Flutter mobile app with a UI, using TextFields for input and Buttons for operations.

# Contributing
This project is open for contributions! If you’re a beginner, try fixing bugs (e.g., handling invalid inputs better) or adding features. Submit a pull request with your changes, and include a brief description of what you’ve added or improved.
