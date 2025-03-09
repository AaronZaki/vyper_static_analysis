# Vyper Static Analysis Tool

This tool is designed to perform static analysis on Vyper smart contract code. It parses Vyper source code, generates various analysis graphs, and saves the results in a JSON format.

## Features
- **AST Generation**: Parses Vyper source code to generate an Abstract Syntax Tree (AST).
- **Control Flow Graph (CFG)**: Generates a basic representation of the control flow in the code.
- **Dependency Graph**: Analyzes dependencies between different parts of the contract.
- **Call Graph**: Tracks the function calls within the contract.
- **Variable Scope Graph**: Identifies variable scopes throughout the contract.
- **Inheritance Graph**: Maps the inheritance relationships between contracts.

## Requirements
- Python 3.12
- `vyper` library: A Python package for working with Vyper source code and ASTs.

You can install the required dependencies using pip:

```bash
pip install vyper
```

## Usage
Command-Line Interface (CLI)

You can run the script from the command line with the following syntax:

python vyper_static_analysis.py <vyper_file> [--output <output_file>]

## Arguments:

    <vyper_file>: The path to the Vyper source code file you want to analyze.
    --output <output_file>: (Optional) The path where the analysis results will be saved. Default is output_analysis.json.

## Example

python vyper_static_analysis.py contracts/MyContract.vy --output analysis_result.json

This will parse the MyContract.vy Vyper contract, generate various analysis graphs, and save the results to analysis_result.json.
Output

The output will be a JSON file containing the following analysis results:

    AST: The abstract syntax tree of the contract.
    CFG: The control flow graph.
    DependencyGraph: The dependency graph showing variable/function dependencies.
    CallGraph: The call graph representing function calls.
    VariableScopeGraph: The graph representing variable scopes.
    InheritanceGraph: The inheritance relationships between contracts.
