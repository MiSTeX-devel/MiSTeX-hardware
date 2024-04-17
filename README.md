# MiSTeX-hardware

## Current
### MiSTeX baseboard for QMTech form factor FPGA boards
The ![QMTech-MiSTeX](https://github.com/MiSTeX-devel/MiSTeX-hardware/tree/main/QMTech-MiSTeX)
baseboard is the current recommended platform. It can be used with Raspberry Pi Zero
form factor SBCs and QMTech form factor core boards.
Status: The `rev2` revision has been manufactured and tested working.

![QMTech-MiSTeX Baseboard](https://github.com/MiSTeX-devel/MiSTeX-hardware/assets/148607/ed7ece81-8ff8-4c6d-8d95-ff311336d44a)

### Using the Raspberry Pi Zero with MiSTeX, with a generic FPGA board
To connect the Raspberry Pi Zero to the FPGA board of your choice,
the pin mappings can be found in two places:
1. On the FPGA board side the pin mappings are defined in the board support file in MiSTeX-boards:
   ![FPGA pin mapping](https://user-images.githubusercontent.com/148607/277517494-eea3227b-9b3b-425d-9ee6-c806567e1ec3.png)
2. On the Raspberry Pi Zero side, the pin mappings of the GPIO control signals are defined in Main_MiSTeX in fpga_io.cpp:
   ![RPi Zero pin mapping](https://user-images.githubusercontent.com/148607/277518229-199cf3d3-1ec9-4b59-a263-b62d0fe51ac1.png)
   
   And the SPI bus is the SPI0 on the Raspberry Pi header:
   ![RPi SPI pins](https://user-images.githubusercontent.com/148607/280917900-2e73a808-b7a4-495d-a1b5-7b27b0a97bc1.png)

## Obsolete
### MiSTeX Pmod
Status: Manufactured, waiting for arrival. Obsolete, Sipeed Lich

![image](https://user-images.githubusercontent.com/148607/231954815-cf86b118-08cb-40bb-a646-8fff4d7f693a.png)

![image](https://user-images.githubusercontent.com/148607/232922043-c58138c2-cd65-49cd-bb5b-cd18d380f105.png)

### MiSTeX cape for the Terasic DECA board
Status: Manufactured and tested working.

![image](https://user-images.githubusercontent.com/148607/222578200-f00b5eb2-d352-4595-b834-59ee57191b28.png)

![image](https://user-images.githubusercontent.com/148607/231960472-29968781-754c-4d0a-a33a-23db4b70e573.png)
