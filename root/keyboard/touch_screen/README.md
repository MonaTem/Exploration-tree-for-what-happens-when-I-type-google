# Touch screen operations

- When the user puts their finger on a modern capacitive touch screen, a tiny amount of current gets transferred to the finger. This completes the circuit through the electrostatic field of the conductive layer and creates a voltage drop at that point on the screen. The screen controller then raises an interrupt reporting the coordinate of the key press.
- Then the mobile OS notifies the current focused application of a press event in one of its GUI elements (which now is the virtual keyboard application buttons).
- The virtual keyboard can now raise a software interrupt for sending a 'key pressed' message back to the OS.
- This interrupt notifies the current focused application of a 'key pressed' event.
