# Number Theory: Subtraction

In this lab you've learned the basics of number theory as it relates to subtraction.

## Rubric

| Item | Description | Value |
| ---- | ----------- | ----- |
| Summary Answers | Your writings about what you learned in this lab. | 25% |
| Question 1 | Your answers to the question | 25% |
| Question 2 | Your answers to the question | 25% |
| Question 3 | Your answers to the question | 25% |

## Names
- Carson Brown & Patrick McClain

## Summary
- In this lab we learned how computers subtract by turning the second number into a negative and adding it. Since A - B is the same as A + (-B), we needed two ways to represent negative numbers in binary so we built three modules in Vivado. Starting with a half subtractor that subtracts one bit from another, a 4bit one's complement adder that used a second row of adders to handle end around carry. Then we built an 8bit two's complement converter that flipped the bits and added 1. We connected them to switches and LED's and tested them on the basys3 board.

## Lab Questions

### 1 - Explain the differences between our Half Adder from last lab and the Half Subtractor from this lab.
- The difference is that carry = AB as opposed to borrow = A'B which turns out to be an extra inverter on A. Both circuits produce the same result (Y=A XOR B).

### 2 - What about the end around carry of One’s Complement makes it hard to use and implement?
- The end around carry is hard because wiring it makes a combinatorial loop which feeds the circuits input with its own output. Fixing that takes another row of adders, doubling the hardware in turn making it slower. Ones complement also has two zeros.

### 3 - What is the edge case and problem with Two’s Complement number representation?
- The edge case is the most negative number and the problem is that in 8 bits, -128 doesn't have a positive version, so taking its two's complement gives the same number (100000000).
