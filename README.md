# ArduinoRobots
This is my RFID Detector Arduino setup.<br/>
What you need:<br/>
1x Breadboard<br/>
1x Arduino Nano<br/>
1x RFID-RC522 Component<br/>
1x LED<br/>
7x Female to Male wires<br/>
2x Male to Male wires<br/>


Connections:<br/>
First connect a ground pin of the arduino to a horizontal in the breadboard. Next, connect to another horizontal the pin 2 of the Arduino. Afterwards, put the one end of the LED on the Ground horizontal, and the other on the pin 2 horizontal.<br/>

Now, in order to describe the connections directly with the Arduino Uno, I will give two numbers. One number to indicate which pin of the RFID module from left to right in upright position(pins looking down), and one number to indicate in which pin in the arduino uno the other end of the wire goes:<br/>

(1,10)<br/>
(2,13)<br/>
(3,11)<br/>
(4,12)<br/>
(5,-)<br/>
(6,GND or the Ground horizontal in the breadboard)<br/>
(7,9)v
(8,3.3V)<br/>

Now, whenever the module detects the "correct" RFID signal, it will power the 2nd pin.<br/>

In order to change the RFID block tha triggers the Light, substitute the correct sequence in the location of the bold letters in the code<br/>

 if (mfrc522.uid.uidByte[0] == **0x79** && <br/>
     mfrc522.uid.uidByte[1] == **0xEC** &&<br/>
     mfrc522.uid.uidByte[2] == **0x10** &&<br/>
     mfrc522.uid.uidByte[3] == **0x88**)<br/>
     
     
    
