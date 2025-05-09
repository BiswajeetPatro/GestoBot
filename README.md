# GestoBot
GestoBot: Your Hand-Controlled Robotic Claw Adventure
Hey there! Welcome to GestoBot, my quirky little project that lets you control a robotic claw and a rover with just a flick of your wrist. It’s like being a sci-fi puppeteer, but with Arduino Nanos and a whole lot of wires. I built this to mess around with gesture control and robotics, and I’m stoked to share it with you!
What’s This All About?
GestoBot is a DIY setup where you strap on some sensors, wave your hand like a wizard, and watch a robotic claw grab stuff while a rover zooms around. It uses two Arduino Nanos, some cool sensors, and a bit of RF magic to make it all happen wirelessly. Perfect for anyone who loves tinkering with robots or just wants to feel like they’re in a Tony Stark workshop.
What Can It Do?

Wave to Win: Your hand gestures control the claw and rover—tilt, flex, and conquer!
Claw Power: The robotic claw can pick up, drop, or twirl small objects.
Rover Rumble: A wooden board with wheels scoots around, carrying the claw like a trusty steed.
Wireless Vibes: No cords tying you down, thanks to the NRF24L01 RF module.
Arduino Awesomeness: Easy to tweak and make your own with dual Nanos.

Stuff You’ll Need
Here’s the gear I used to bring GestoBot to life:

Arduino Nano (2): The brains of the operation.
ADXL345 Accelerometer: Catches your hand tilts.
FS-L-005-253-MP Flex Sensor: Knows when you’re flexing those fingers.
L298 Motor Driver Board: Powers the rover’s DC motors.
NRF24L01 RF Transmitter & Receiver: For that sweet wireless connection.
Robotic Claw: The star of the show, ready to grab.
Servo Motors (4): Make the claw dance.
Rover Setup:
Wooden Board (1): The rover’s body.
DC Motors (4): For zipping around.
Toy Wheels (4): Gotta roll in style.


Jumper wires, breadboard, and a power source (like 9V batteries or USB).

Software You’ll Want

Arduino IDE: Grab it from Arduino’s site.
Libraries (install these in the IDE):
Wire.h (for I2C stuff).
Servo.h (to boss around the servos).
RF24.h (for wireless chit-chat).
Adafruit_ADXL345 (to talk to the accelerometer).
SPI.h (for RF module communication).



Getting Started
Alright, let’s get this bot rolling:

Snag the Code:git clone https://github.com/yourusername/GestoBot.git


Set Up Arduino IDE: Download it, install it, love it.
Add Libraries:
In the IDE, go to Sketch > Include Library > Manage Libraries.
Search for RF24, Adafruit_ADXL345, and grab ’em.


Flash the Nanos:
Plug in one Nano at a time.
Open transmitter.ino and receiver.ino from the GestoBot folder.
Upload each to the right Nano (transmitter for the hand, receiver for the rover).



Hooking It Up
Wiring can be a bit like untangling Christmas lights, but here’s the gist:

Hand Side (Transmitter Nano):
ADXL345 to I2C (A4: SDA, A5: SCL).
Flex Sensor to A0 (use a resistor for a voltage divider).
NRF24L01 to SPI (CE: D9, CSN: D10, MOSI: D11, MISO: D12, SCK: D13).


Rover Side (Receiver Nano):
NRF24L01 to the same SPI pins as above.
L298 to D4-D7 for DC motors, ENA/ENB to D5/D6 for speed.
Servos to D2, D3, D8, D9 for claw action.


Rover Build:
Slap the DC motors and wheels on the wooden board.
Mount the claw on top, connect the servos.


Power everything up—Nanos, servos, and motors need juice!

How to Play

Fire up both Nanos, the rover, and the claw.
Strap the flex sensor and accelerometer to your hand (tape works!).
Start waving:
Tilt your hand to steer the rover.
Bend your fingers to open/close the claw.


Watch the rover cruise and the claw snag stuff, all in real-time.

Wanna Join the Fun?
I’d love for you to jump in and make GestoBot even cooler:

Fork this repo.
Make a branch: git checkout -b my-cool-idea.
Tweak away and commit: git commit -m "Made it awesome".
Push it: git push origin my-cool-idea.
Send me a pull request!

License
This project’s under the MIT License—check out the LICENSE file for the deets.
Shoutouts

Big thanks to the Arduino crew for their libraries and forums.
Inspired by every robot movie I binged as a kid.

Got Questions?
Hit me up on GitHub Issues or shoot an email to biswajeet697@gmail.com. Let’s geek out over robots together!
