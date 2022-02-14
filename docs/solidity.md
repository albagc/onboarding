# Solidity

> Useful resources:
> - [Solidity Homepage](https://soliditylang.org/)
> - [Solidity for beginners](https://www.tutorialspoint.com/solidity/index.htm)
> - [Solidity Conference](https://summit.soliditylang.org/), part of the more general Ethereum/Devconnect conference.
> - [A very simple Solidity contract](https://www.tutorialspoint.com/solidity/solidity_first_application.htm)

## Statically typed language

Solidity is a statically typed language. This means that the type of each of the variables should be specified, and variables cannot change type during runtime (e.g. variable `_value` cannot first hold a Boolean and then an integer)

> Statically typed programming languages perform type checking during the course of compilation rather than during run time, which makes programs written in these languages run much faster.

## Solidity Integrated Development Environment (IDE)

The primary Solidity IDE is [Remix](remix.md), which is available both as a web-browser and a desktop application.

Some plug-ins ([Example 1](https://marketplace.visualstudio.com/items?itemName=JuanBlanco.solidity), [Example 2](https://marketplace.visualstudio.com/items?itemName=ConsenSys.Solidity)) for VS Code exist, but none are officially supported and functionality appears limited compare to what Remix offers.

## Specifying the Solidity version

A basic smart contract structure looks like this:

```
pragma solidity ^0.4.24;
contract TestContract {
    // ...
}
```

In all cases, you must first define the version of Solidity that you wish to use. Note here that the ^ allows only for patch increments in the solidity version. For example, this contract will not compile on versions earlier that 0.4.24 or later that 0.5.0. 

## Size of smart contracts

There is a limit to how big smart contracts can be, namely 24.576 kb. If you hit this limit, the best approach is to split your contract among several smaller ones, or to use a library (via [`for`](https://docs.soliditylang.org/en/v0.6.10/contracts.html#using-for)).

## Types of functions

Functions within a Solidty smart contract can have one of four types:

* `public` - all can access
* `external` - Cannot be accessed internally, only externally
* `internal` - only this contract and contracts deriving from it can access
* `private` - can be accessed only from this contract

