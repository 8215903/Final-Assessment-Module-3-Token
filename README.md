# ETH Proof Beginners Course Final Module 3

In this ETH Proof Beginners Course Final Module 3, showcases the deployment of the essential syntax and functionality of Smart Contracts.

## Description

Users can use this program to deploy contracts, calculate their value, and perform mint, burn, and balance transactions. Ethereum Remix IDE is used to launch and test smart contracts that are almost entirely written in Solidity. We could use Solidity Compiler IDE as our compiler as well.


## Getting Started

### Executing program

* After you did some coding or your codes is ready to go, We're using Remix IDE to smoothly run this solidity Program. We could use Solidity Compiler IDE but Remix IDE is more likely to use for our project.
* To be able to get started, make or add a new file to Remix IDE. This is the Compiler we're gonna use to run our code!

//SPDX-License-Identifier: MIT
pragma solidity ^0.8.18;

contract MetaToken {

    // public variables here
    
    string public tokenName = "CentsOfJoy";
    string public tokenAbbrv = "COJ";
    uint public totalSupply = 0;

    // mapping variable here
    
    mapping(address => uint) public balances;

    // mint function
    
    function mint (address _address, uint _value) public {
        totalSupply += _value;
        balances [_address] += _value;
    }

    // burn function
    function burn (address _address, uint _value) public {
    
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }
}



* The SPDX License Identifier specifies the smart contract's legal usage constraints, which are also visible to the compiler, developer, and anyone else reading it. 
* There are numerous licenses available in the realm of software development.
* After you've finished coding, click the Solidity Compiler on the left side of the IDE, followed by the Deploy button under the Solidity Compiler. 
* After you've copied the address, paste it into Mint, Burn, and Balances.
* Before you may burn and collect the balances, you must first deal with the mint. Following that, the uint value or total supply will be presented.


## Authors

Gio Mico

https://www.facebook.com/LifeDeathl


## License

This project is licensed under the [MIT] License - see the LICENSE.md file for details
