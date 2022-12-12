# Artemis Styling Guide

This is the place where can check for Smart Contract coding best practices, a styling standard approved by the Artemis education team. This is heavily inspired on the [Bophades Coding Standard](https://github.com/OlympusDAO/olympus-v3/blob/master/CODE_STD.md) from the Olympus v3 repo.

## Basic Principles
- Aim for clear and succinct code
- Explicit over implicit
- Write code PRIMARILY for humans, not machines
- Comment on WHY, not WHAT. Code should be able to explain "what". AKA READABLE
- Aim to write code that is self-documenting
- Meaning clear function names and variables
- Overall readability will bring auditability, which in turn bring security
- Aim for gas-efficiency, but with above constraints

## Actual coding tips
- External/public functions and variables are `lowerCamelCase`
    - ex. function `deposit()`
    - ex. variable `totalDebt`
- Internal/private functions should be `_prefixed` and `lowerCamelCase`
    - ex. `_checkApproval()`
- Contract names are `UpperCamelCase`
    - ex. `OlympusTreasury`
- Function arguments can be `suffixed_` to easily differentiate them from state variables
    - `_issueReward(address to_)`
- Regular Comments use `//`, and should be added only when readable variables and code don't suffice
    - `// My meaningful comment`
- NatSpec comments use `///`. But please don't bloat every single solidity line with natspec comments...
    - `/// @notice Natspec comment`
- Consider denoting sections of your code in some way, e.g. with single line headers: 
```// ========= HEADER ========= // ```
