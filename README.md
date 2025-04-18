## Installation pre-requisites:

- Python
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

- Returns the binary string representation of the rotated value.

`rotr(x, n)` rotates the integer `x` right by `n` bits.

- Returns the binary string representation of the rotated value.

`ch(x, y, z)` chooses bits from `y` or `z` based on `x`.

- For each bit position i: if x[i] is 1, choose y[i]; if x[i] is 0, choose z[i].
- Implemented as (x & y) ^ (~x & z).
- Returns the binary string representation of the result.

`maj(x, y, z)` calculates the majority value for each bit position of the three integers.

- For each bit position, the result is 1 if the majority of the three bits is 1.
- Implemented as (x & y) ^ (x & z) ^ (y & z).
- Returns the binary string representation of the result.

## Task 2: Hash Functions

`hash(s)` converts strings into a numeric value using a polynomial rolling hash algorithm.

- Uses `31` as a multiplier for the polynomial hash calculation.
- Returns a value modulo `101` (the size of the hash table).
- For each character in the input string, the hash is updated as: hashval = ord(char) + 31 \* hashval.

## Task 3: SHA256

`generatePadding(filePath)` implements the SHA-256 padding scheme:

- Takes a file path as input.
- Calculates message length in bits.
- Adds a single '1' bit.
- Adds '0' bits until length = 448 (mod 512).
- Appends the original message length as a 64-bit big-endian integer.
- Returns the padded message as a hexadecimal string.

The padding ensures the message length is a multiple of 512 bits, with the last 64 bits reserved for the message length.

## Task 4: Prime Numbers

`findPrimesEratosthenes(n)` finds all prime numbers up to `n` using the [Sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes) algorithm:

- The Sieve of Eratosthenes is an ancient algorithm for finding prime numbers.
- It works by starting at two, the first prime number, and then crossing out all multiples of two.
- Then you go to the next unmarked number (your next prime) and then repeat.
- All unmarked numbers are primes.

`findPrimesSundaram(n)` finds all prime numbers up to `n` using the [Sieve of Sundaram](https://en.wikipedia.org/wiki/Sieve_of_Sundaram) algorithm:

- The Sieve of Sundaram is an algorithm for finding prime numbers.     
- It works by eliminating numbers that can be expressed as `i + j + 2ij` where `i`, `j` are positive integers and `i ≤ j`.     
- The remaining numbers are doubled and incremented by one to generate all odd prime numbers.     
- This method is efficient for generating primes up to a given limit.
