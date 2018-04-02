# NoritakeVFD
Basic template starting point for Noritake VFD Async/SPI connections using Arduino UNO.
7
The Arduino sketch is to setup communciations and do some simple stuff on the sceen.

**First VFD I have used is the GU144x40D K610A4 very good cheaply sourced from eBay less than $15.**

| Module | Second Header |
| ------------- | ------------- |
| GU280x16G 7000  | Content Cell  |
| GU160x32D 7806A| Content Cell  |
| GU140x32F 7806A | Content Cell  |

Other boards I am working on include...
GU280x16G 7000
GU160x32D 7806A
GU140x32F 7806A

Part number structure...
   GU128X32D-7806A - graphic module example                                CU20025-UW1J - character module example 
   GU prefix = Graphic + Text module                                       CU prefix = Text only
   128x32D = dot format X x Y + dot pitch (D=~0.45mm)                      20025=20x2 with 5mm character height
  -7806A = product range and version                                       UW1J= product range and version


  | Graphic Module Product Series | Main Features |
  | ----------------------------- | ------------------------------------------------------------------------------ |
  | 7806A | LCD 5x7 character emulation plus graphics upgrade, 4/8 bit LCD interface + user ports with SPI /async expansion. |
  |7806A     |LCD 5x7 character emulation plus graphics upgrade, 4/8 bit LCD interface + user ports with SPI /async expansion.|
  |7n00/3  |  Economy text and graphics modules plus scroll, draw and extended fonts. 8 bit parallel, async and sync interfaces.
  |8n00B   |  Hi-Speed, controlled by an ASIC and ideally suited for animations or fast display update. 8 bit parallel and sync int.
  |K61nA8 |  Pixel Flexible, use a RISC processor for individual dot/cursor placement with SPI/I2C/RS485/RS232 + user ports|
  |3900  |     Multi-fonts from Europe and Asia with a wide range of commands including DMA + user ports. RS232 and parallel.|


The Arduino sketch is to setup communciations and do some simple stuff on the sceen.

Using the 10 pin connection for serial on the module, pins are as follows

CON1 (connector 1 this is common througout most Noritake modules) 

| Pin| Async |SPI|
| ------------- | ------------- | ------------- |
| 1 | 5v | 5v|
| 1 | Nc | SCK|
| 1 | RXD | /SS|
| 1 | Nc | SIN|
| 1 | 0v | 0v|
| 1 | Nc | SOUT|
| 1 | TXD | /IRQ|
| 1 | /RES | /RES|
| 1 | MB | MB|
| 1 | HB | n/a|
      
 

In Async mode you need minimum three connections to the Arduino 3 for TX, 5 for /RES and GND for 0V
Use an external power supply as Arduino UNO or other boards may not have enough mA to drive it.
