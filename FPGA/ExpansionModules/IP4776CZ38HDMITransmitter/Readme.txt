IP4776CZ38 HDMI Transmitter Expansion Module demo code
Numato Lab
http://www.numato.com
http://www.numato.cc

This package contains source and other files necessary to build 
IP4776CZ38 HDMI Transmitter Expansion Module demo for the following boards.

1. Mimas V2 Spartan 6 FPGA Development Board with DDR SDRAM
   http://numato.com/mimas-v2-spartan-6-fpga-development-board-with-ddr-sdram.html  

2. Saturn Spartan 6 FPGA Development Board with DDR SDRAM
   http://numato.com/saturn-spartan-6-fpga-development-board-with-ddr-sdram.html

3. Waxwing Spartan 6 FPGA Development Board
   http://numato.com/waxwing-spartan-6-fpga-development-board.html
   
4. Neso Artix 7 FPGA Module
   https://numato.com/neso-artix-7-fpga-development-board/

5. Skoll Kintex 7 FPGA Module
   https://numato.com/skoll-kintex-7-fpga-development-board/   
   
The IP4776CZ38 HDMI Transmitter Expansion Module used to test this code is available at
 http://numato.com/fpga-boards/expansion-modules.html

IO Breakout Boards make it easier to attach expansion modules to Saturn. Please see 
links to IO Breakout boards below.
http://numato.com/fpga-boards/expansion-modules/io-breakout-module-for-saturn.html

----------------------------------------------------------------------------------------------------------------
Spartan 6 Series:
 
There are two ways to build this project. Either using Xilinx ISE or running 
easy to use batch files. ISE Webpack must be installed with proper license in 
either case. By default the project is configured to build for XC6SLX45. To 
build for a different device you need to open IP4776CZ38ExpansionModuleTransmitter.xise
in ISE and change the device in project properties and rebuild.

1. Building the project using Xilinx ISE
   Open the project file IP4776CZ38ExpansionModuleTransmitter.xise using ISE. Right 
   click on the "Generate Programming Files" process in the process window and
   select "Rerun all". You may need to add appropriate user constraints file to
   the project depending on which board you are building the project for. User
   Constraints Files for all supported boards can be found inside "ucf" folder.
   
2. Building the project using Command Line Window
   Open command line window and navigate to the folder where the project files
   are located. Invoke the batch file and give necessary input asked. Make sure
   all build steps finish successfully. You will need to register the path to Xilinx
   build tools (usually C:\Xilinx\xx.xx\ISE_DS\ISE\bin\nt) in PATH environment
   variable for the batch files to work.
   
ISE Webpack software and license is available for free at http://www.xilinx.com
   
When the build finishes successfully a .bin and a .bit file should be created in
the folder name binary.

----------------------------------------------------------------------------------------------------------------
Artix and Kintex 7 Series:

There is a "IP4776CZ38ExpansionModuleTransmitter.xpr" vivado project file. Just open it by double
clicking. By default the project is configured for Skoll. Click "Generate Bitstream"
and choose Yes in any subsequent dialog windows. For building for Neso, change the
FPGA device to XC7A100T-CSG324 from "Project Settings" and set the "Neso" constraints 
set to "Active". You may now select "Generate Bitstream" to build the project.

----------------------------------------------------------------------------------------------------------------
Sr No.  Numato Lab's FPGA Board       Header Used
        
1           Elbert V2                 Not Available
2           Mimas*                    Not Available
3           Mimas V2                  P7
4           Saturn LX16**             P7
5           Saturn LX45**             P7
6           Waxwing Carrier           Not Available
7           Waxwing Dev Board         P5
8           Neso(IO Expansion on P5)  P8-P10
9           Skoll(IO Expansion on P5) P12-P6

*  Mimas Expansion Connector connected to Header P1 of Mimas.
** Saturn Expansion Connector connected to Header P2 of Saturn Spartan 6 Development Board.
