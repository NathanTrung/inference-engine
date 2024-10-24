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
