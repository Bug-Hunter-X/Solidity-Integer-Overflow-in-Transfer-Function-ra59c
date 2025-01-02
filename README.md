# Solidity Integer Overflow Vulnerability

This repository demonstrates a common integer overflow vulnerability in Solidity smart contracts. The `transfer` function in the `bug.sol` file is susceptible to underflow if the `amount` to be transferred exceeds the sender's balance. This can lead to unexpected and potentially harmful consequences.

The `bugSolution.sol` file provides a corrected version of the `transfer` function that uses SafeMath to prevent integer overflow and underflow.

## How to Reproduce

1. Compile both `bug.sol` and `bugSolution.sol` using a Solidity compiler.
2. Deploy the contract to a test network or local blockchain.
3. Attempt to transfer an amount larger than the sender's balance. Observe that the `bug.sol` contract will allow the transaction to succeed, while `bugSolution.sol` will revert.

## Mitigation

The best way to mitigate integer overflow vulnerabilities is to use SafeMath library.  SafeMath provides functions that perform arithmetic operations with overflow/underflow checks.