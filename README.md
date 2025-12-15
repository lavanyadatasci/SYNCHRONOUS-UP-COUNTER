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

/*1.Open Quartus Prime software.


2. Create a new project using New Project Wizard.


3. Select Empty Project and choose device.


4. Create a new Verilog HDL file.


5. Write the JK flip-flop code.


6. Save file and set as top-level entity.


7. Compile the project to verify errors.


8. Observe output using RTL Viewer / Simulation.
 
*/

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 
DOWN COUNTER
module ex12(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out-1;
end
endmodule
UP COUNTER
module ex11(out,clk,rst);
input clk,rst;
output reg [3:0]out;
always @ (posedge clk)
begin
   if(rst)
     out<=0;
   else 
     out <= out+1;
end
endmodule


Developed by:Lavanya A RegisterNumber:25007878
*/

**RTL LOGIC UP COUNTER**
<img width="1918" height="1022" alt="Screenshot 2025-12-15 114310" src="https://github.com/user-attachments/assets/cd8f023a-a843-42cb-9208-03ada6a68838" />
<img width="1919" height="1018" alt="Screenshot 2025-12-15 131252" src="https://github.com/user-attachments/assets/7dac0aba-7d90-4e3a-b55a-3a311744b091" />



**TIMING DIAGRAM FOR IP COUNTER**
<img width="1908" height="1010" alt="Screenshot 2025-12-15 114510" src="https://github.com/user-attachments/assets/7152f4c1-6db0-4dd3-91da-8afa1ddcf227" />
<img width="1914" height="1018" alt="Screenshot 2025-12-15 131451" src="https://github.com/user-attachments/assets/f17522d9-9d85-4a1a-a9b4-08edd4378c68" />


**TRUTH TABLE**
<img width="682" height="344" alt="Screenshot 2025-12-15 134112" src="https://github.com/user-attachments/assets/f3f90ec2-a5e3-4909-8ac5-bbdfe153fd74" />

**RESULTS**
To implement 4 bit synchronous up counter,down counter and validate functionality is done.
