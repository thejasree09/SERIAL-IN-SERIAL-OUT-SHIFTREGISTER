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

Define module with inputs (clk, rst, serial_in) and output (serial_out).

Use a register array to store shift register bits (e.g., reg [3:0] shift_reg).

Shift data on each positive clock edge if reset is not active.

Assign serial_out as the last bit of the shift register.

Create a testbench to apply input sequences and compare outputs with functional table.

**PROGRAM**

![program](https://github.com/user-attachments/assets/0cb24f90-ab15-4b2f-ae0c-d34319cb245f)


**RTL LOGIC FOR SISO Shift Register**

![simulation](https://github.com/user-attachments/assets/eabe5546-777b-47ea-b1b6-a2e825216411)

**TIMING DIGRAMS FOR SISO Shift Register**

![waveform](https://github.com/user-attachments/assets/30188131-a468-4afb-9459-5a2941469c2d)


**RESULTS**

SISO Shift Register correctly shifts input bits serially through the register, matching the expected functional table outputs.
