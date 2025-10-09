# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */Procedure:

1. Connect four D flip-flops in series as shown in the circuit diagram.


2. Apply a common clock signal to all flip-flops.


3. Connect Q output of each flip-flop to the D input of the next flip-flop.


4. Apply the serial input data (either 0 or 1) to the D input of the first flip-flop.


5. Initially clear all flip-flops to logic ‘0’.


6. Apply clock pulses one by one and observe the output of each flip-flop after every pulse.


7. Note how the input bit moves through each flip-flop stage and finally appears at the serial output.



**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.
SERIAL IN SERIAL OUT SHIFT REGISTER

module EXP10(clk, sin, q);
input clk;
input sin;
output [3:0] q;
reg [3:0] q;
always @(posedge clk)
begin
q[0] <= sin;
q[1] <= q[0];
q[2] <= q[1];
q[3] <= q[2];
end
endmodule
Developed by: RegisterNumber:25018184 sharmila.R

*/

**RTL LOGIC FOR SISO Shift Register**
<img width="1790" height="963" alt="Screenshot 2025-10-08 110402" src="https://github.com/user-attachments/assets/e0093b55-3bac-411e-acaa-9deba33a7672" />

**TIMING DIGRAMS FOR SISO Shift Register**
<img width="1764" height="979" alt="Screenshot 2025-10-08 112352" src="https://github.com/user-attachments/assets/1c83580c-1238-48cf-a43b-8fbd9f760833" />

**RESULTS**
