Developed by: PUGAZHALENTHI V

RegisterNumber: 212224100047

# JK FLIPFLOP

**AIM:** 

To implement  JK flipflop using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**JK Flip-Flop**

JK flip-flop is the modified version of SR flip-flop. It operates with only positive clock transitions or negative clock transitions. The circuit diagram of JK flip-flop is shown in the following figure.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/a649c30b-232b-4558-b188-fd6c09845180)


This circuit has two inputs J & K and two outputs Qtt & Qtt’. The operation of JK flip-flop is similar to SR flip-flop. Here, we considered the inputs of SR flip-flop as S = J Qtt’ and R = KQtt in order to utilize the modified SR flip-flop for 4 combinations of inputs. The following table shows the state table of JK flip-flop.

![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/c4360742-e8a8-4937-b089-c46c0433f9a3)

 
Here, Qtt & Qt+1t+1 are present state & next state respectively. So, JK flip-flop can be used for one of these four functions such as Hold, Reset, Set & Complement of present state based on the input conditions, when positive transition of clock signal is applied. The following table shows the characteristic table of JK flip-flop. Present Inputs Present State Next State
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/6c275261-a6d5-4c37-a3a7-1e88ca11c4cd)

By using three variable K-Map, we can get the simplified expression for next state, Qt+1t+1. Three variable K-Map for next state, Qt+1t+1 is shown in the following figure.
 
![image](https://github.com/naavaneetha/JKFLIPFLOP-USING-IF-ELSE/assets/154305477/5174f41b-0ce0-4329-a372-6d1943ea6673)

The maximum possible groupings of adjacent ones are already shown in the figure. Therefore, the simplified expression for next state Qt+1t+1 is Q(t+1)=JQ(t)′+K′Q(t)Q(t+1)=JQ(t)′+K′Q(t)

**Procedure**
step-1 Go to quartus software.
step-2 Set new environment.
step-3 Type the code to implement SR flipflop using verilog and validating their functionality using their functional tables.
step-4 Run the program.
step-5 Give inputs in the waveform table .

step-6 Run the program.


**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming. 

Developed by: PUGAZHALENTHI V

RegisterNumber: 212224100047
```
module exp_jk(q,qb,j,k,clock);
input j,k,clock;
output reg q;
output qb;
always @ (posedge (clock))
begin
   q<=(j&(~q))|((~k)&q);
end
assign qb=(~q);
endmodule
```

**RTL LOGIC FOR FLIPFLOPS**

![image](https://github.com/user-attachments/assets/da5b81c2-b7d4-40ba-97cb-cc22f75ab369)


**TIMING DIGRAMS FOR FLIP FLOPS**

![image](https://github.com/user-attachments/assets/25cd2948-6117-45c1-ba67-57a38fee7f8c)


**RESULTS**

Implementation of JK flipflop using verilog and validating their functionality using their functional tables is executed and the output is verified successfully.
