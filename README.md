# 32-bit_ALU_using_VHDL

Welcome to the 32-bit ALU (Arithmetic Logic Unit) repository! This repository contains the VHDL source code and test benches for a 32-bit ALU implementation. The ALU is designed to perform a variety of arithmetic and logical operations based on a control line (ALU_operation). It also includes a MUX component for selecting the input of the ALU.

## ALU Operations

The ALU supports the following operations:

| ALU_operation | Operation Explanation |
| ------------- | --------------------- |
| 0000          | NOR                   |
| 0001          | AND                   |
| 0010          | NAND                  |
| 0011          | OR                    |
| 0100          | Shift Left            |
| 0101          | Shift Right           |
| 0110          | Rotate Left           |
| 0111          | Rotate Right          |
| 1000          | XOR                   |
| 1001          | XNOR                  |
| 1010          | Set less than         |
| 1011          | ADD                   |
| 1100          | Subtract              |
| 1101          | Multiply              |
| 1110          | Division              |
| 1111          | Modulus               |

The ALU_operation control line selects one of the 16 different instructions, allowing the ALU to perform the corresponding operation.

## ALU Components

The ALU is built using VHDL and consists of the following components:

- Two inputs, A and B, each of which is 32 bits.
- ALU_result, which is the result of the ALU operation and is also 32 bits.
- ZERO flag, a one-bit signal that indicates whether the ALU_result is zero or not. If ALU_result = 0, the ZERO flag is set to 1; otherwise, it is set to 0.

In addition to the ALU, a MUX component is included to select the input of the ALU. The most significant bit of ALU_operation is used as a selector for this MUX.

## Testing

The ALU and MUX components are thoroughly tested using test benches. The test benches ensure that the ALU performs the correct operations for various inputs and control signals. They verify the functionality and correctness of the ALU and MUX components, helping to identify and fix any potential issues.

## Repository Structure

The repository is structured as follows:

- `src/`: This directory contains the VHDL source code for the 32-bit ALU and MUX components.

- `testbench/`: Here, you can find the test benches for the ALU and MUX components. These test benches provide various test cases to validate the functionality of the components.

- `docs/`: This directory contains any additional documentation related to the project, such as a design overview or implementation details.

- `LICENSE`: The license file specifying the terms and conditions for using our project.

- `README.md`: The file you are currently reading, providing an overview of the project, its components, and instructions for getting started.

## Getting Started

To get started with the 32-bit ALU project, please refer to the documentation in the `docs/` directory. It provides detailed instructions on how to use and integrate the ALU and MUX components into your own VHDL designs.

## Contributing

We welcome contributions to our 32-bit ALU project! If you have any ideas, bug fixes, or enhancements, please feel free to open an issue or submit a pull request. We appreciate your interest in improving our project.

We hope you find our 32-bit ALU implementation useful and reliable for your digital logic projects!
