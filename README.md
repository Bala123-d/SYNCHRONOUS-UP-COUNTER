### SYNCHRONOUS-UP-COUNTER

**AIM:**

To implement 4 bit synchronous up counter and validate functionality.

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**4 bit synchronous UP Counter**

If we enable each J-K flip-flop to toggle based on whether or not all preceding flip-flop outputs (Q) are “high,” we can obtain the same counting sequence as the asynchronous circuit without the ripple effect, since each flip-flop in this circuit will be clocked at exactly the same time:

![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/d5db3fa0-e413-404c-b80e-b2f39d82e7e8)


![image](https://github.com/naavaneetha/SYNCHRONOUS-UP-COUNTER/assets/154305477/52cb61eb-d04b-442d-810c-31185a68410b)

Each flip-flop in this circuit will be clocked at exactly the same time.
The result is a four-bit synchronous “up” counter. Each of the higher-order flip-flops are made ready to toggle (both J and K inputs “high”) if the Q outputs of all previous flip-flops are “high.”
Otherwise, the J and K inputs for that flip-flop will both be “low,” placing it into the “latch” mode where it will maintain its present output state at the next clock pulse.
Since the first (LSB) flip-flop needs to toggle at every clock pulse, its J and K inputs are connected to Vcc or Vdd, where they will be “high” all the time.
The next flip-flop need only “recognize” that the first flip-flop’s Q output is high to be made ready to toggle, so no AND gate is needed.
However, the remaining flip-flops should be made ready to toggle only when all lower-order output bits are “high,” thus the need for AND gates.

**Procedure**

/* write all the steps invloved */

**PROGRAM**
```
**UP Counter**
module ex11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @(posedge clk)
begin
   if (!rstn)
	    out<=0;
	else
	    out<=out+1;
end
endmodule
**DOWN COUNTER**
module unit11(out,clk,rstn);
input clk,rstn;
output reg [3:0]out;
always @(posedge clk)
begin
   if (!rstn)
	    out<=0;
	else
	    out<=out-1;
end
endmodule
/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:D.BALA SUBRAMANYAM RegisterNumber:24002856
*/
```
**RTL LOGIC UP COUNTER**
![image](https://github.com/user-attachments/assets/54ba1730-7b20-4b72-a338-0ae866c45f0f)
![image](https://github.com/user-attachments/assets/a7fa91f6-f0a7-432a-ae38-cd847e00551f)

**TIMING DIAGRAM FOR IP COUNTER**
![image](https://github.com/user-attachments/assets/0365be5a-4f92-4f02-9cd1-dc9c726cc71b)
![image](https://github.com/user-attachments/assets/92623a80-655a-45d3-a261-c29fbc1d67c2)

**TRUTH TABLE**

![image](https://github.com/user-attachments/assets/c9a98d98-5d9d-47ab-973d-60132fa22299)

**RESULTS**
Thus the 4 bit synchronous up counter and down counter are verified and the logic diagrams are designed the truth tables are verified .
