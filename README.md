## Installation pre-requisites:

* Python 3.12 or higher
  * Can be downloaded from [python.org](https://www.python.org/downloads/)
* Jupyter Notebook

You can install Jupyter Notebook using pip:

```bash
pip install notebook
```

## Usage

1. Start Jupyter Notebook:

```bash
jupyter notebook
```

2. Open `tasks.ipynb` in the Jupyter Notebook interface
3. Run the cells to test the different functions.

## Task 1: Binary Representations

`rotl(x, n)` rotates the integer `x` left by `n` bits.  
`rotr(x, n)` rotates the integer `x` right by `n` bits.  
`Ch(x, y, z)` chooses bits from `y` or `z` based on `x`.  
`Maj(x, y, z)` calculates the majority value for each bit position of the three integers.

## Task 2: Hash Functions

`hash(s)` converts strings in to a numeric value.  
`31` is used as a multiplier. `101` is the size of the hash table.
