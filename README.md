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

**Procedure**<br>
1.Type the program in Quartus software.<br>

2.Compile and run the program.<br>

3.Generate the RTL schematic and save the logic diagram.<br>

4.Create nodes for inputs and outputs to generate the timing diagram.<br>

5.For different input combinations generate the timing diagram.<br>

/* write all the steps invloved */

**PROGRAM**<br>
module exp10(clk, sin, q);<br>
 input clk;<br>
 input sin; <br>
 output [3:0] q;<br>
 reg [3:0] q;<br>
 always @(posedge clk)<br>
 begin <br>
 q[0] <= sin;<br>
 q[1] <= q[0];<br>
 q[2] <= q[1];<br>
 q[3] <= q[2];<br>
 end<br>
 endmodule<br>

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by: Lokesh M RegisterNumber:24900227

*/

**RTL LOGIC FOR SISO Shift Register**<br>

![Screenshot 2024-12-23 133625](https://github.com/user-attachments/assets/bb79f780-cd2d-464a-bff4-8c5a42cbdd35)




**TIMING DIGRAMS FOR SISO Shift Register**<br>

![Screenshot 2024-12-23 133658](https://github.com/user-attachments/assets/cb1bb1be-6548-4dd2-abb1-77802acb3618)


**RESULTS**<br>
To implement SISO Shift Register using verilog and validating their functionality using their functional tables is verified successfully.
