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
1.Define Module: Define a Verilog module for the D flip-flop with inputs (D, CLK) and outputs (Q, Q_bar).

2.Declare Inputs and Outputs: Declare input and output ports for the module.

3.Implement Flip-Flop Logic: Write Verilog code to implement the D flip-flop logic based on its functional table. Use a synchronous always @(posedge CLK) block to trigger the flip-flop on the positive edge of the clock signal.

4.Simulate Using Testbench: Write a Verilog testbench to simulate the behavior of the D flip-flop under different input conditions.

5.Apply Input Stimuli: In the testbench, apply various combinations of input stimuli (D, CLK) to cover all possible input states.

6.Verify Output Behavior: Verify that the output behavior of the D flip-flop matches the expected behavior defined by its functional table.

7.Check for Race Conditions: Ensure that there are no race conditions or undefined states in the design by analyzing the timing and sequence of input changes.



**PROGRAM**

```




/* Program for flipflops and verify its truth table in quartus using Verilog programming.
   Developed by:Goutham.K
   RegisterNumber:212223110019
*/
module DFlipflop(D,Clock,Q,Qbar);
input D,Clock;
output reg Q,Qbar;
always @ (negedge Clock)// use negative edge clock for triggereing condition 
//compute D flipflop logic here
begin
 	Q=D;
Qbar=~D;
end
 endmodule

```

**RTL LOGIC FOR SISO Shift Register**
![327045389-7a423a42-c099-4a2f-b7d2-a4c95bfae8b0](https://github.com/Goutham2306/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/138971154/36a6e23a-83a6-4376-9553-edf6f5acfc38)

**TIMING DIGRAMS FOR SISO Shift Register**
![327045453-87033859-6e8d-4fd1-b5b8-5b8e6cc24d57](https://github.com/Goutham2306/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/138971154/0da295a5-9609-442a-bf1b-723081286b4c)

**RESULTS**
Thus the program to implemention of D flipflop using verilog and validating their functionality using their functional tables are executed successfully.



