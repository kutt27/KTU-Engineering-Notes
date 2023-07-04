### Explanation types questions:

1. Explain the algorithm for multiplication of binary numbers.
2. Describe the algorithm for division using the restoring method for binary numbers.
3. What is an array multiplier? Explain its working.
4. How does Booth's multiplication algorithm work? Discuss its advantages and disadvantages.
5. What are the basic principles of pipelining? How does pipelining improve performance in computer systems?
6. In Lecture 1, what are the different classifications of pipeline processors? Discuss each classification in detail.
7. In Lecture 2, what are the additional classifications of pipeline processors? Explain each classification and their significance.
8. Explain the concept of instruction pipelines. How do they enhance the efficiency of instruction execution in a computer system?
9. What are arithmetic pipelines? Discuss their purpose and benefits.
10. What are hazards in pipeline processing? How are they detected and resolved in computer systems?

### Problems based question:

1. Problem: Multiply the following binary numbers using the algorithm for multiplication:
   a) 1011 * 1101
   b) 1110 * 1001

2. Problem: Divide the following binary numbers using the restoring method:
   a) 101101 / 110
   b) 111010 / 1011

3. Problem: Implement an array multiplier to multiply the binary numbers 1011 and 1101.

4. Problem: Apply Booth's multiplication algorithm to multiply the binary numbers 1010 and 1101.

5. Problem: Given a computer system with a 5-stage pipeline (Fetch, Decode, Execute, Memory, Write-back), determine the number of clock cycles required to execute a program with 20 instructions, assuming there are no hazards.

6. Problem: In Lecture 1, classify the following pipeline processors as scalar or superscalar:
   a) Processor A can execute one instruction per clock cycle.
   b) Processor B can execute two instructions per clock cycle.

7. Problem: In Lecture 2, classify the following pipeline processors as in-order or out-of-order:
   a) Processor A follows the order of instructions and does not execute them out of order.
   b) Processor B uses techniques like branch prediction and speculative execution to execute instructions out of order.

8. Problem: Design an instruction pipeline for a simple processor architecture. Specify the stages involved and briefly describe the purpose of each stage.

9. Problem: Identify and explain the data hazards in the following pipeline:
   a) IF (Instruction Fetch) - ID (Instruction Decode) - EX (Execution) - MEM (Memory Access) - WB (Write-back)
   b) ID (Instruction Decode) - EX (Execution) - MEM (Memory Access) - WB (Write-back)

10. Problem: Given a pipeline with hazard detection and resolution techniques, analyze a sequence of instructions to identify any potential hazards and explain how they can be resolved.