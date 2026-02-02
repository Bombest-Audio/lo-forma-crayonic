# Octave Buttons Options  

This document explores two hardware approaches for adding an octave of 12 buttons (for one octave of keys) to Lo-Forma: Crayonic Edition.  

## Option A: Direct GPIO connections  

In this simple approach, each of the 12 buttons is connected to its own GPIO pin on the microcontroller. Each button uses a pull-down or pull-up resistor to provide a stable logic state. When pressed, the microcontroller reads the button state and triggers the corresponding note or parameter.  

Pros:  
- Straightforward wiring and code  
- Low latency: each button state is immediately available  
- Good for prototypes when plenty of GPIO pins are available  

Cons:  
- Uses 12 separate GPIO pins, which may exhaust available pins on the Pico  
- Wiring can become messy with many buttons  

## Option B: Matrix or I²C expander  

To conserve GPIO pins, a 3×4 key matrix or an external I²C GPIO expander can be used. A key matrix arranges the 12 buttons in rows and columns; by scanning rows and columns, the microcontroller can detect which button is pressed using only 7 pins (3 columns + 4 rows). Alternatively, an I²C expander like the PCF8574 or MCP23017 provides 8–16 additional GPIOs controlled over I²C, enabling all 12 buttons to be read via two I²C pins.  

Pros:  
- Conserves microcontroller GPIO pins  
- Cleaner wiring when using a matrix or breakout board  
- Scalable if more buttons or controls are needed later  

Cons:  
- Requires scanning logic or I²C driver in firmware  
- Slightly more complexity in hardware and software  
- Matrix scanning can introduce ghosting without diodes  

Both options can be implemented depending on your design goals. Choose the direct GPIO approach if you value simplicity and have spare pins, or the matrix/expander approach if you need to save pins or plan to expand the control surface.
