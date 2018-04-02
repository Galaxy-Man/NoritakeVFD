# Noritake VFD
Basic template starting point for Noritake VFD Async/SPI connections using Arduino UNO.

The Arduino sketch is to setup communciations and do some simple stuff on the sceen.

**First VFD used is the GU144x40D K610A4 very good cheaply sourced from eBay less than $15.**


Other boards I am working on include...

| Module | Second Header |
| ------------- | ------------- |
| GU280x16G-7000  | Content Cell  |
| GU160x32D-7806A| Content Cell  |
| GU140x32F-7806A | Content Cell  |


Part number structure...

| GU128X32D-7806A - graphic module example | CU20025-UW1J - character module example  |
| ----------------------------- | ------------------------------------------------------------------------------ |
|   GU prefix = Graphic + Text module                        |               CU prefix = Text only|
|  128x32D = dot format X x Y + dot pitch (D=~0.45mm)         |             20025=20x2 with 5mm character height|
| -7806A = product range and version                         |              UW1J= product range and version|


  | Graphic Module Product Series | Main Features |
  | ----------------------------- | ------------------------------------------------------------------------------ |
  | 7806A | LCD 5x7 character emulation plus graphics upgrade, 4/8 bit LCD interface + user ports with SPI /async expansion. |
  |7806A     |LCD 5x7 character emulation plus graphics upgrade, 4/8 bit LCD interface + user ports with SPI /async expansion.|
  |7n00/3  |  Economy text and graphics modules plus scroll, draw and extended fonts. 8 bit parallel, async and sync interfaces.
  |8n00B   |  Hi-Speed, controlled by an ASIC and ideally suited for animations or fast display update. 8 bit parallel and sync int.
  |K61nA8 |  Pixel Flexible, use a RISC processor for individual dot/cursor placement with SPI/I2C/RS485/RS232 + user ports|
  |3900  |     Multi-fonts from Europe and Asia with a wide range of commands including DMA + user ports. RS232 and parallel.|
  |800  |    Hi-Speed, controlled by an ASIC and ideally suited for animations or fast display update. 8 bit parallel and sync int.|

The Arduino sketch is to setup communciations and do some simple stuff on the sceen.

Using the 10 pin connection for serial on the module, pins are as follows

CON1 (connector 1 this is common througout most Noritake modules) 

| Pin| Async |SPI| Pin  | Async | SPI |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| 1 | 5v | 5v| 2 | Nc | SCK|
| 3 | RXD | /SS| 4 | Nc | SIN|
| 5 | 0v | 0v| 6 | Nc | SOUT|
| 7 | TXD | /IRQ| 8 | /RES | /RES|
| 9 | MB | MB| 10 | HB | n/a|

      
 

In Async mode you need minimum three connections to the Arduino 3 for TX, 5 for /RES and GND for 0V
Use an external power supply as Arduino UNO or other boards may not have enough mA to drive it.
