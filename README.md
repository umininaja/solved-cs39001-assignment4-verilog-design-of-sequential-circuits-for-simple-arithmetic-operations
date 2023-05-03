Download Link: https://assignmentchef.com/product/solved-cs39001-assignment4-verilog-design-of-sequential-circuits-for-simple-arithmetic-operations
<br>



<ol>

 <li><strong>[Two’s Complement Converter FSM] </strong>Design (using Verilog), simulate (using an appropriate Verilog testbench), and implement (on a FPGA platform supported by your CAD software tool), a simple finite state machine (FSM) that in every clock cycle reads an input bit, and outputs a bit such that the bitstring output till that point is the two’s complement of the binary number read till that point, including the most recently read bit (the number is considered to be input from the LSB side). The FSM has one input control signals which resets it to the initial state. Come up with an appropriate interface for your circuit. [Hint: consider a Mealy machine.] (4 marks)</li>

 <li><strong>[Multiple-of-three Detector FSM] </strong>Design (using Verilog), simulate (using an appropriate Verilog testbench), and implement (on a FPGA platform supported by your CAD software tool), a simple finite state machine (FSM) that in every clock cycle reads an input bit, and outputs a bit which indicates whether the binary number read till that point, including the most recently read bit (the number is considered to be input from the LSB side), is divisible by three. The input number is to be considered an unsigned integer. The FSM has one input control signals which resets it to the initial state. Come up with an appropriate interface for your circuit. [Hint: again, consider a Mealy machine.</li>

</ol>

<ol start="3">

 <li><strong>[Sequential GCD Calculator] </strong>Consider the following C function to calculate the GCD of two positive integer arguments:</li>

</ol>

/* a, b are positive integers, with a &gt;= b */ int gcd (int a, int b) { int temp; while (1) {

while ((temp = a – b) &gt; 0) a = temp; if (!temp) return b; temp = a; a = b; b = temp;

}

}

Design (using Verilog), simulate (using an appropriate Verilog testbench) and implement (on a FPGA platform supported by your CAD software tool) a sequential circuit to execute this scheme and generate the GCD as output. Assume each input operand is a positive 8-bit integer. Come up with an appropriate interface for your circuit. Design the data path and the control path separately, with the control path circuitry generating control signals based on status signals received from the data path circuitry. Design the data path in a <em>bottom-up </em>manner, structurally and hierarchically. In the data path, try to reuse adder/subtractor circuits you have designed in a previous assignment.