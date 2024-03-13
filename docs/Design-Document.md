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

### Command line interface
The program is required to be run from command line, with 2 arguments - input file and output file. Therefore the very first step of the program should be to capture and parse the command line arguments. This can be done using the `argparse` library. This should be implemented as a separate function, so that it can be easily tested. A unit test should be written to test the parsing of the command line arguments.

### Instantiation of the circuit solver class
The next step is to create an instance of the circuit solver class (see in the outline of functions and classes).



### Unit testing
#### List of unit tests
1. CLI arguments parsing test

## TODO:
 Link the "circuit solver" class to "Instantiation of the circuit solver class"



