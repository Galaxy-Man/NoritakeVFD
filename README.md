# NoritakeVFD
Basic template starting point using Noritake VFD Async/SPI connections nusing Arduino UNO.

First VFD I have used is the GU144x40D K610A4 very good cheaply sourced from eBay less than $15.

Other boards I will try this on will be added as I acquire them.

The Arduino sketch is to setup communciations and do some simple stuff on the sceen.

Using the 10 pin connection for serial on the module, connections are as follows

CON1 (this is common througout most Noritake modules)                          
Pin      Async      SPI 
1         5V        5V         
2         Nc         SCK         
3         RXD        /SS         
4         Nc         SIN         
5         0V         0V         
6         Nc         SOUT         
7         TXD        /IRQ         
8         /RES       /RES         
9         MB         MB         
10        HB         N/A       

In Async mode you only need three connections to the Arduino 3 for TX, 5 for /RES and GND for 0V
Use an external power supply as Arduino UNO or other boards may not have enough mA to drive it.
