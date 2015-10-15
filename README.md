# lego_mindstorms_nxt_controller
Instructions for cheap, fun, and easy way to control a computer (with keystrokes and mouse) wirelessly from an NXT Joystick using bluetooth, conductors/wires/alligator clips, and a board such as a MakeyMakey or Arduino Leonardo (or a modified Arduino Uno).


Goal: 
Use a lego mindstorms joystick to send keystrokes to a computer with USB connectivity without expensive hardware such as a BrickPi/Arduino NXT Shield and only using the basic NXT-G software that comes with the NXT.


Difficulty:
Ages 8+ for construction with adult help and use with a MakeyMakey, 12+ for modifying the design and programming to customize further, and 15+ to use non-MakeyMakey boards (will require non-graphical programming knowledge and possibly flashing board firmware at your own risk)


Steps: 

1: Acquire supplies: 2 Lego Mindstorms NXT's (v1.2 or v2.0), 4 mindstorms NXT/EV3 motors and cables, 1 NXT v1.2 or v2.0 touch sensor and cable, a MakeyMakey (or other board as mentioned above), a lego kit with similar/actual parts included in the NXT/EV3 kits, alligator clips (6-10), rubber bands, breadboard jumper wires (6-10, but may not be neccessary), aluminum foil, and masking tape. 

2: Assemble the Joystick based on these instructions: http://www.philohome.com/nxtjoystick/joystick.htm

3: Download the joystick.rbt to the joystick and reciever.rbt to the other NXT brick to be used as a bluetooth reciever.

4: Put aside the joystick and grab the reciever NXT

5: Construct 2 motors with aluminum foil contacts on the sides and a aluminum foil toggle (see pictures) in the middle connected to the motor shaft. Each motor creates one axis of movement (foward/backward or side/side) by creating one circuit at a time while toggling back and forth and using rubber bands to reset it in the middle. The middle toggle will be hooked up to ground/earth and will complete the circuit with the outer contacts (hooked up to arrow keys or wasd on the makey makey/other board) using the aluminum foil to activate one key at a time by completing a circuit. This ensures that only forward or backward is pressed at a time and won't screw up the input. With two motor toggle setups, the joystick can send forward/backward (A motor port) and left/right (B motor port) or w/s and a/d depending on how it is connected to the board.

6: To connect the MakeyMakey, ensure it works, and if not install the drivers from here: https://learn.sparkfun.com/tutorials/makey-makey-quickstart-guide

7: Connect the middle toggle's aluminum foil from both motors to the earth connectors on the makey makey. Then, connect the two side contacts on A with alligator clips to the Forward/Backward arrows (or w/s but jumper wires are neccessary) and the port b motor's side contacts to Left/Right (or a/s but jumpers are needed).

8: Connect the NXT's via bluetooth and run the reciever program on the reciever and the joystick program on the joystick and press the touch sensor on the joystick once you have centered it. Try individual movements and reverse alligator clips if any of the movements are reversed.

9: For other boards, you will have to write custom code to take in the input, debounce it and send a keystroke. The Arduino leonardo supports keyboard emulation natively but to get an Uno to work, one must reflash it to make it act as a HID device. Here are some good guides: http://mitchtech.net/arduino-usb-hid-keyboard/ http://wiki.sgmk-ssam.ch/index.php?title=Arduino_Uno_R3_as_HID 
