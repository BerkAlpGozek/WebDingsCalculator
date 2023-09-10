# WebDingsCalculator
WebDings Calculator made for AP CS Principles @ Hisar School 2023-2024


This project is a simple 4-operation calculator with a font called "WebDings." I used this font to give it a more creative look and give it some personality.

This project was made in Playgrounds using SwiftUI. 
![Screenshot 1](https://github.com/BerkAlpGozek/WebDingsCalculator/blob/main/App%20Screenshots/Empty.png)

The Project Recipe:
-

 - Create required variables:
    - A String called `DispText`
      - This is what is displayed on the LCD
    - An Float Called `InPocket`
     - This is the stored variable in the calculator when an operation is made
    - An Int Called `Sign`
       - This states the type of  operation
         - 0: Empty, 1: Addition, 2: Subtraction, 3: Multiplication, 4: Division
    - A bool Called `AskaLnglSryu`
      - This boolean tells the code if it is in repeated calculation mode
    - A String called `ShnjIkri`
      - This is the variable that sets the font for the calculator. 
    - A Float Called `KwruNgsa`
  - Create all the buttons required for this calculator and place them accordingly
    - All number buttons and point buttons add to the end of `DispText`
  - Use a disabled button for the LCD with the alignment Trailing.
    
- Create the Function `FloodTheLCL` with an Int Parameter Called `riAynmi`
  - This function is used with the operator buttons
  - Parameter ´riAynmi´ indicates which button it is 
  - Gives the value inside `DispText` to InPocket with Type Casting to a Float
  - `DispText` is reset
  - `Sign` is given the value in `riAynmi` to
  - `AskaLnglSryu` is set to `false` for the calculator to know it is no longer in repeated calculator mode
  
- Create the function called `HumInstrProj` that returns a float
  - This function is used with the equals button.
  - It has a temp `Float` variable called `gndhIkri`
  - `gndhIkri` is assigned the value inside `DispText` as a float for use in repeated calculation mode.
  - It checks the sign assigned to var ´Sign´ and does the required operations to function as a proper calculator
  - `InPocket` is set to `gndhIkri` for repeated Calculation to work
