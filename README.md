Human Stopwatch (Evil Edition)
Same idea as a regular stopwatch — press to start, press to stop. Except it won't let you stop that easily.
How it works
Press the button to start the timer. It counts up live on the LCD. When you press to stop, it makes you confirm. Five times. Each press shows a new fragment of "ARE YOU SURE?" while the clock keeps running in the background. Only on the fifth press does it actually stop and show your final time.
Press sequence to stop:
ARE
ARE YOU
ARE YOU SURE
ARE YOU SURE?
Stops and shows final time
After 5 seconds it resets back to the start screen.
Hardware
Arduino Uno
16x2 I2C LCD (address 0x27)
1 push button
Breadboard + jumper wires
Uses INPUT_PULLUP so no resistor needed — wire one leg to pin 2, other leg to GND.
Wiring
I2C LCD → Arduino
```
SDA → A4
SCL → A5
VCC → 5V
GND → GND
```
Button → Arduino
```
One leg → Pin 2
Other   → GND
```
Setup
Install the `LiquidCrystal_I2C` library in the Arduino IDE
Library Manager → search "LiquidCrystal I2C" → install the one by Frank de Brabander
Open `HumanStopwatch.ino`, select your board and port, upload
Wire it up and power via USB
Notes
If the LCD shows nothing, try adjusting the contrast dial on the back of the I2C module
If your I2C address isn't 0x27, run an I2C scanner sketch to find the right one and update line 3
