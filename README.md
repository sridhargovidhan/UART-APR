## AIM:

To implement and design synthesis and simulation for uart using cadence - genus and innovus.

## TOOLS REQUIRED:

Functional Simulation: Incisive Simulator (ncvlog, ncelab, ncsim) Synthesis: Genus Floorplanning: Innovus

## PROCEDURE:

Step 1: Synthesis requires the following files as follows: ◦ Liberty Files (.lib) ◦ VerilogFiles (.v )

### Add Verilog  (.v ) file

### Add Testbench file

### Add run.tcl file

SDC (Synopsis Design Constraint) File (.sdc)

In your terminal type “gedit input_constraints.sdc” to create an SDC File if you do not have one.

The SDC File must contain the following commands; 

### Add SDC file

i→ Creates a Clock named “clk” with Time Period 2ns and On Time from t=0 to t=1. 

ii, iii → Sets Clock Rise and Fall time to 100ps. 

iv → Sets Clock Uncertainty to 10ps. 

v, vi → Sets the maximum limit for I/O port delay to 1ps.

•	The Liberty files are present in the library path,

•	The Available technology nodes are 180nm ,90nm and 45nm.

•	In the terminal, initialise the tools with the following commands if a new terminal is being used. ◦ csh ◦ source /cadence/install/cshrc

•	The tool used for Synthesis is “Genus”. Hence, type “genus -gui” to open the tool.

•	Genus Script file with .tcl file Extension commands are executed one by one to synthesize the netlist. Step 2 : Creating an SDC File Step 3 : Performing Synthesis

### Fig 1: RTL Simulation:
<img width="1600" height="849" alt="image" src="https://github.com/user-attachments/assets/f873eca1-2abb-4f01-b1ba-28f4d18acf0f" />


### Fig 2: Synthesis RTL Schematic:
<img width="1726" height="911" alt="image" src="https://github.com/user-attachments/assets/9ff2114e-3492-4844-87b5-263864298864" />

### Fig 3: Area Report:
<img width="1600" height="813" alt="image" src="https://github.com/user-attachments/assets/d178cd08-66b9-4d60-98b4-6e660c53e8ce" />
### Fig 5: Timing Report:
<img width="1600" height="813" alt="image" src="https://github.com/user-attachments/assets/f998bdc1-da60-415e-b496-4f833b850b61" />


## RESULT:

The functionality of the uart was successfully verified using a testbench and simulated with the nclaunch tool and genus and for innovus creating the physical design.
