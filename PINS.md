
So, the Cypress 100 has the following "byte" ports;
 * PA (multifunction)       - Connect to FPGA as a group
 * PB (fifo data low byte)  - FD[0..7]  Connect to FPGA as group with below
 * PC (fifo data high byte) - FD[8..15] Connect to FPGA as group with above
 * PD (GPIF addr)           - Connect to FPGA as a group
 * PE (multifunction)       - Slow speed FPGA JTAG programming (connected as PC use to be connected)

 * RDY[0..5] - Ready flags, connect to FPGA as a group
 * CTL[0..5] - Ctrl flags, connect to FPGA as a group
 * WR# - Write data, connect to FPGA
 * RD# - Read data, connect to FPGA
 * TD[0..2] - Timer output pins, connect **one** to FPGA. Other should be connected to test pins.
 * RXD0 + TXD0 - Hardware UART, connect to FPGA as a UART pair. Both RX and TX lines should have test pins.
 * RXD1 + TXD1 - Hardware UART, connect to FPGA as a UART pair. Both RX and TX lines should have test pins. 
 * INT4 - Pull low with a test contact which pulls high.
 * INT5# - Extra interrupt, connect to FPGA.
 * BKPT - Breakpoint - connect to test pin.

