
Micro: PIC32MX170F256B

Tools:
MPLAB X IDE v5.10 or above
MCC v3.85.1
XC32 v2.30

MCLR: Pin1
PGED1: Pin4 RB0
PGEC1: Pin5 RB1
TX1: Pin11 RB4
RX1: Pin15 RB6
Output: Pin25 RB14
Input: Pin26 RB15


For MPLAB X Simulator
Enable UART in the Simulator UART1 I/O property
Navigate to the Register Injection tab of Stimulus window
Select the UART receive register (RCREG or RXBUF, etc. depending on your device)
Select Message in Trigger
Select the data file in Data Filename
Select Pkt in Format
Prepare the data file in your favorite editor.

Comment out the led flashing part in main.c, because simulator is slow.
Otherwise it will take long time to start.

Here's an example data file:
////////////////
wait 100 ms
"print('Hello world!')"
wait 100 ms
0D 0A
////////////////