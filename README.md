# ADCP_misalignment_Error
Compute the error due to the ADCP misalignment 

1. **Imports**: 
    - `import PySimpleGUI as sg`: This imports the PySimpleGUI library and gives it the alias `sg`.
    - `import numpy as np`: This imports the NumPy library and gives it the alias `np` which is used for numerical calculations.

2. **Function `calculate_parameters`**:
    - This function takes in the values of \( u \), \( v \), \( w \), \( q \), and \( f \) and calculates the total kinetic energy (\( q \)) and the misalignment angle (\( \alpha_t \)).
    - It follows the calculations as per the provided equations.
    - Returns the calculated values of \( \alpha_t \) and \( q \).

3. **Layout**:
    - `layout`: This variable defines the layout structure of the GUI window.
    - It consists of input fields for \( u \), \( v \), \( w \), \( q \), and \( f \), 'Calculate' and 'Exit' buttons, and an output text box.

4. **GUI Window**:
    - `window = sg.Window('Calculate Parameters', layout)`: This creates a GUI window with the specified title and layout structure.
    - The window contains input fields for users to enter values of \( u \), \( v \), \( w \), \( q \), and \( f \), as well as 'Calculate' and 'Exit' buttons.

5. **Event Loop**:
    - The program enters a while loop to continuously handle events from the GUI window until the window is closed or the 'Exit' button is clicked.
    - Inside the loop, it waits for events to occur.

6. **Event Handling**:
    - If the 'Exit' button is clicked or the window is closed, the loop breaks, and the program exits.
    - If the 'Calculate' button is clicked:
        - The input values are retrieved from the input fields.
        - The `calculate_parameters` function is called with the input values.
        - The calculated values of \( \alpha_t \) and \( q \) are displayed in the output text box.
        - If the input values are not valid (i.e., not numeric), an error popup is displayed.

7. **Window Closure**:
    - Once the event loop breaks (either due to window closure or clicking 'Exit'), the window is closed.

Overall, this code creates a GUI using PySimpleGUI where users can input values for \( u \), \( v \), \( w \), \( q \), and \( f \), and then calculate the total kinetic energy (\( q \)) and misalignment angle (\( \alpha_t \)) based on those inputs.
