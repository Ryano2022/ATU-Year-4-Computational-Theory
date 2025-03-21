## Installation pre-requisites:

- Python 3.12 or higher
  - Can be downloaded from [python.org](https://www.python.org/downloads/)
- Jupyter Notebook

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

## Task 3: SHA256

`generatePadding(filePath)` implements the SHA-256 padding scheme:

- Takes a file path as input.
- Calculates message length in bits.
- Adds a single '1' bit.
- Adds '0' bits until length = 448 (mod 512).
- Returns the padded message as a binary string.

The padding ensures the message length is a multiple of 512 bits, with the last 64 bits reserved for the message length.
