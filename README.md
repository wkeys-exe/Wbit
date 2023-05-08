# Wbit Token
This is Solidity token created for project "Create a Token" the token name is set as Wbit.
## Description
For this token we first declare some public variables

string public tokenName = "Wbit";
string public tokenAbbrv = "WBIT";
uint public totalSupply = 1;

then we declare a public mapping, this will be used to check the supply of a particular address.

mapping(address => uint) public balances;

