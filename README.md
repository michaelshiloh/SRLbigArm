# SRLbigArm
Designing a PLC to automate the Big Arm walking

We have the scale model built by Arik

## 12 September 2025

Done
- Labeled joints to correspond with SRL's Big Arm
- Identified which Arduino pin controls which linear actuator
- Tested that the linear actuator is strong enough to lift up the base (it is!)

Arduino pins to joint mapping (with the white tape on the 4 position header socket that connects to the 4 pins on the H-bridge **facing away from the H-bridge**)
- Wrist: Pins 4 and 5
- Elbow: Pins 2 and 3
- Shoulder: Pins 8 and 9
- Pins 6 and 7 are wired to a channel of the H-Bridge but are unused at this time; could be used for rotating or the stabilizing side legs

Sample code to make the shoulder move (either retract or extend)
```
void setup() {
  pinMode (8, OUTPUT);
  pinMode (9, OUTPUT);

// To reverse the direction, change the HIGH to LOW and LOW to HIGH
  digitalWrite (8, LOW);
  digitalWrite (9, HIGH);
}
```
1. Note that this will not stop since there is no command to stop the motors
1. Note that if the actuator is already fully extended or retracted, an internal switch prevents it from further movement and damage

Next steps:
- Schedule with Tony to get trained on the MIG welder, the horizontal band saw, and the metal drill press
- Unscrew the wooden base with all the electronics
- Undo the large bolt under the arm 
- Coordinate with me to remove the arm. This is a two person job to be done safely.
- Take the base down to the Scene Shop and cut off the unused portion (horizontal band saw, I think)
- Drill holes for the casters
- Drill holes on the sides in case we decided to add the stabilizing side legs
- Should we add the rotating part at this time?

#### How to use Github markdown
### This is how you make a header
## This is how you make a bigger header
this is how you make a  paragraph
this is part of the same  paragraph
this is part of the same  paragraph
this is part of the same  paragraph
this is part of the same  paragraph
this is part of the same  paragraph

To start a new paragraph, insert a the blank line after the previous paragraph

- this is how you make a list
- second item
- etc.

More info [here](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) and in many other sources online
