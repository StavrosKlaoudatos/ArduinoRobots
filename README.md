# ArduinoRobots
This is my RFID Detector Arduino setup.
What you need:
1x Breadboard
1x Arduino Nano
1x RFID-RC522 Component
1x LED
7x Female to Male wires
2x Male to Male wires


Connections:
First connect a ground pin of the arduino to a horizontal in the breadboard. Next, connect to another horizontal the pin 2 of the Arduino. Afterwards, put the one end of the LED on the Ground horizontal, and the other on the pin 2 horizontal.

Nowm, in order to describe the connections directly with the Arduino Uno, I will give two numbers. One number to indicate which pin of the RFID module from left to right in upright position(pins looking down), and one number to indicate in which pin in the arduino uno the other end of the wire goes:

(1,10)
(2,13)
(3,11)
(4,12)
(5,-)
(6,GND or the Ground horizontal in the breadboard)
(7,9)
(8,3.3V)

Now, whenever the module detects the "correct" RFID signal, it will power the 2nd pin.

In order to change the RFID block tha triggers the Light, substitute the correct sequence in the location of the bold letters in the code

 if (mfrc522.uid.uidByte[0] == **0x79** && 
     mfrc522.uid.uidByte[1] == **0xEC** &&
     mfrc522.uid.uidByte[2] == **0x10** &&
     mfrc522.uid.uidByte[3] == **0x88**)
     
     
    
