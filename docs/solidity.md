# Solidity

> Useful resources:
> - [Solidity Homepage](https://soliditylang.org/)
> - [Solidity for beginners](https://www.tutorialspoint.com/solidity/index.htm)

## Statically typed language

Solidity is a statically typed language, meaning that the 

> Statically typed programming languages perform type checking during the course of compilation rather than during run time, which makes programs written in these languages run much faster.

## A simple smart contract

A basic smart contract structure looks like this:

```
pragma solidity ^0.4.24;
contract TestContract {
    // ...
}
```

In all cases, you must first define the version of Solidity that you wish to use. Note here that the ^ allows only for patch increments in the solidity version. For example, this contract will not compile on versions earlier that 0.4.24 or later that 0.5.0. 

