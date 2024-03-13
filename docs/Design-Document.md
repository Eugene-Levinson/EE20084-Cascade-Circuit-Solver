<h1 style="text-align: center;">Cascade Circuit Solver - Design Document</h1>
<h3 style="text-align: center;">Eugene Levinson (el769)</h3>
<h3 style="text-align: center;">March 2024</h3>

### Table of Contents

1. [Stuff Here](#stuff-here)
2. [More Stuff Here](#more-stuff-here)
3. [Even More Stuff Here](#even-more-stuff-here)
4. [Stuff Here](#stuff-here)
5. [More Stuff Here](#more-stuff-here)



##

### Project Overview and Definition of Done
The goal of this cascade circuit solver is run a simulation of a circuit and output the results. The program must read the input file as specificed in the project definition file. Correctly interprite the circuit to be analaysed from the input file, and other meta data. Then correctly calculate the results of the circuit and output the results to the output file.

The project is considered done when all of the following are met:
1. The program can be launched from the command line in the following manner: `python app.py <input file> <output file>`

2. The program can read and create correct outputs for all test cases provided. This includes circuits of varying complexity and size.

3. The program produces and empty output if the input file is not valid.

4. All parts of the program are covered by unit tests.

<br>

## Design Overview
The program is designed to be modular, with each part of the program being implemented as a separate class (where it makes sense). This will allow for easy testing and debugging. The program will be implemented in a test-driven manner, with unit tests being written before the implementation of the program. The unit tests should define the expected behaviour of a given function or class, including all edge cases and the implementation should then be written to satisfy the tests. Unit tests should be written using the `pytest` library.

The program utilises a "fail fast" approach, where the program will exit as soon as an error is encountered. This is to prevent the program from continuing to run in an invalid state, which could lead to further errors and make debugging more difficult. In the cases of errors, an empty output file should be created to comply with the project definition.

The overall program flow will be as follows:

1. The program is launched from the command line with 2 arguments - input file and output file.

2. The command line arguments are parsed. This should be implemented as a separate function, so that it can be easily tested. The cli parser should check if the input file exists and if the output file is writable. If not, the program should exit with an error message.

3. The CircuitSimulation class is the instantilised. This is the main interface of the program.

4. The input file is parsed using a `parse` method of the `CircuitSimulation` class. During parcing several atributes of the `CircuitSimulation` class are set. The **CIRCUIT**, **OUTPUT** and **TERMS** blocks are indentified. Each block is parsed seperately and the data is stored in the `CircuitSimulation` class. The **CIRCUIT** block is parsed into a graph data structure, which is used to represent the circuit, where each node is an instance of a `Component` class. The **OUTPUT** block is parsed into a list of dictionaries. The **TERMS** is parsed and `Source` and `Load` classes are instantiated.

5. The circuit is solved using the `solve` method of the `CircuitSimulation` class. The circuit is solved with matrix multiplication and linear algebra using the "Chain Matrix Analysis" method. Numpy is used to perform all maths operations to increase performance.

6. The solving step maybe be repeated several times for different frequnecy and paramattric sweeps. The results are stored in the `CircuitSimulation` class.

7. The results are formatted and written to the output file with the `write_output` method of the `CircuitSimulation` class.

8. The program exits.

## Design Implementation

### 

## Unit testing
#### List of unit tests
1. CLI arguments parsing test

## Style and organisation

## TODO:
 Link the "circuit solver" class to "Instantiation of the circuit solver class"



