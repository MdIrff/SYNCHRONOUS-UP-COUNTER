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
~~~
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
end endmodule
~~~


/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by:Muhammad Irfan M RegisterNumber:25014471
*/

**RTL LOGIC UP COUNTER**
<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e79c2d72-82f3-4f71-89b8-5a897f145c4e" />


**TIMING DIAGRAM FOR IP COUNTER**
<img width="757" height="502" alt="image" src="https://github.com/user-attachments/assets/43283a35-5e38-45ac-8f0b-da5b3dedb092" />


**TRUTH TABLE**
<img width="609" height="411" alt="image" src="https://github.com/user-attachments/assets/f13b7a6d-4d7f-4493-8357-2ec2c9c084c2" />


**RESULTS**

Thus the truth table of logic gates in Quartus II using Verilog programming is studied and verified successfully
