# Custom_Microprocesor_Design
Microprocessor designed in Digital, tested with Iverilog, with RAM integration and 7-segment display support 
---

## Features

- Supports memory read/write operations
- Reads inputs and drives 7-segment displays
- Fully tested in simulation and on hardware
- Modular design: easy to extend or modify

---

## How to Run with Hardware (FPGA Board w/ 7-segment displays)
- Requires a software called "quartus" 
1. Download:
   -  microprocessor.sdc
   -  microprocessor.tcl
   -  microprocessor.v
   -  ram_vals_1.txt
   -  ram_vals_2.txt
2. open Windows Powershell
3. Copy ram_vals_1.txt to ram_vals.txt with the command:
   -   cp ram_vals_1.txt ram_vals.txt
5. The board attached to the computer should stop flashing and
the seven-segment displays will all be 0. The commands are:
   -   quartus_sh -t .\microprocessor.tcl
   -   quartus_pgm -c1 -mjtag -o”p;microprocessor.sof”
