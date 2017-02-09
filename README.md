# StradivaRIOs_Display

Overview
The StradivaRIOs is a proof-of-concept physical digital audio controller that emulates the way multiple instruments are played in different modes of operation. This controller communicates with a computer to produce sound. In order to interface with a user, two different sensors are used: an infrared distance sensor (IR sensor) to track the distance from a user’s hand to the device, and an array of capacitive touch sensors which function like a touchscreen. This data is then transformed into a protocol called Open Sound Control (OSC) within a National Instruments myRIO microcontroller. Finally, data from the myRIO is sent via UDP (User Datagram Protocol) packets over a private network to a laptop computer, which processes the data in a sound synthesis program to produce audio signals. 


Tools Employed
Code Composer Studio – This program was used to code and debug the MSP430 processors in both the preliminary testing as well as the final application programming and testing. 

LabVIEW -  LabVIEW was used to handle the majority of the processing. It held the state machine that handled input from the MSPs and formatted the processed data in the correct way for output via UDP. This was, by far, the easiest paradigm for coding the myRIO, which was our master processor. LabVIEW made many potentially difficult aspects of this project (SPI, UDP, OSC) much simpler than they would have been otherwise. 

Multisim – Multisim was used to design the schematic for the capacitive touch printed circuit boards that the MSPs controlled as well as the schematic for the printed circuit board that connected the 6 MSPs to our myRIO. Although the group had used Multisim many times in the past, this project allowed us to learn more about the process of finding and creating footprints that were usable in real life situations.

Ultiboard – This program was used to create and trace the layout for our two sets of printed circuit boards. This was a tool that no one in our group had used much before. Using it required consulting professors and independent learning in order to build PCBs at the quality and precision that was required.

Max – This program was used to produce sounds on a laptop in response to the data being communicated from the device. A specific max program was created to work with the unique StradivaRIOs data protocol.

