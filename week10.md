https://youtu.be/2FuPAq_Y4e0
For this week's assignment, Bato and I made a music instrument on our Arduino board. We used an analog sensor (a potentiometer) to control the notes, and a switch to turn the instrument on and off. We first tried to use the distance measuring sensor (Ultrasonic sensor), but decided to go with this one since we’ve already tried that in class.

We added a new file on arduino for the pitches, and selected seven notes (C4 - B4) from the pitches to include in our code. These seven notes are known as the Diatonic scale (Do, Re, Mi, Fa, So, La, Ti, Do)  in Music theory. 

Then, we used if and else if statements to assign each note to a position on the dial of the potentiometer, so the notes play consecutively as the dial is turned.To do this, we divided the Potentiometer’s Input value (1023) into 8 different sections.

We then included the switch as another digital input, and had the speaker play the notes when the switch (buttonValue) was HIGH. We struggled with adding the switch, and so to troubleshoot, we used Serial.print and tested each aspect of our circuit to make sure everything worked on its own. Once we had everything running, we found that the notes sounded very garbled. We fixed this by changing the frequency of each note from 8 to 1000, which made the notes sound very clear.
