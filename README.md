# Inference Engine

This project implements various algorithms to check if a given query can be inferred from a set of logical clauses in a knowledge base. The algorithms included are:
- **Backward Chaining**
- **Forward Chaining**
- **Truth Table Checking**

The engine processes a knowledge base of logical implications and a query to determine whether the query is entailed by the knowledge base using one of the specified inference methods.

## Features

- **Backward Chaining**: Recursively checks if the query can be derived from the knowledge base by working backward from the query.
- **Forward Chaining**: Derives new facts by working forward from the knowledge base until the query is reached.
- **Truth Table Checking**: Generates all possible models to check if the query is true in every model that satisfies the knowledge base.

## File Structure

- `BackwardChaining.py`: Contains the `BackwardChaining` class implementing the backward chaining algorithm.
- `ForwardChaining.py`: Contains the `ForwardChaining` class implementing the forward chaining algorithm.
- `TruthTable.py`: Contains the `TruthTable` class implementing the truth table checking algorithm.
- `Clause.py`: Defines the `Clause` class representing a logical clause with antecedents and a consequent.
- `KnowledgeBase.py`: Defines the `KnowledgeBase` class, which stores the logical clauses and unique symbols.
- `iengine.py`: Main entry point for the inference engine. Parses the input file and invokes the chosen inference method.

## Usage

### Command Line
  ```bash
  python iengine.py <filename> <method>
  ```
<filename>: Path to the input file containing the knowledge base and query.
<method>: The inference method to use, which can be one of the following:
        - `tt: Truth Table`
        - `fc: Forward Chaining`
        - `bc: Backward Chaining`

Input Format

The input file should follow this format:

    The knowledge base is preceded by TELL and consists of semicolon-separated clauses.
    The query is preceded by ASK.

Example Input

mathematica

TELL
A & B => C; D => E; A;
ASK
E

Example Execution

bash

python iengine.py input.txt bc

This will run the backward chaining algorithm using the knowledge base and query defined in input.txt.
Algorithms
1. Backward Chaining (bc)

    Starts with the query and recursively checks if it can be deduced from the knowledge base.
    Returns YES with the entailed symbols if the query is deduced, otherwise NO.

2. Forward Chaining (fc)

    Starts with facts (clauses with no antecedents) and iteratively derives new facts until the query is reached.
    Returns YES with the entailed symbols if the query is entailed, otherwise NO.

3. Truth Table (tt)

    Evaluates the query by generating all possible models for the symbols in the knowledge base.
    Returns YES with the count of models that satisfy the query if it's entailed in all models, otherwise NO.

Installation
Clone the repository:

bash

git clone https://github.com/NathanTrung/inference-engine.git

Navigate into the project directory:

bash

cd inference-engine

Run the engine using the command line as described above.
License

This project is licensed under the MIT License.

vbnet


This version is formatted properly and ready to be used in your repository's `README.md` file. Let me know if further adjustments are needed!
