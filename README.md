# Wbit Token
This is Solidity token created for project "Create a Token" the token name is set as Wbit.
## Description
For this token we first declare some public variables

```javascript
string public tokenName = "Wbit";
string public tokenAbbrv = "WBIT";
uint public totalSupply = 1;
```
then we declare a public mapping, this will be used to check the supply of a particular address.

```javascript
mapping(address => uint) public balances;
```
then we add the important functions which would allow us to change the supply of out tokens either by mint or burn.

Mint function
```javascript
function mint (address _address, uint _value) public {
   totalSupply += _value;
   balances[_address] += _value;
   
   ```
Burn function
```javascript
function burn (address _address, uint _value) public {
   if (balances[_address] >= _value) {
   totalSupply -= _value;
   balances[_address] -= _value;  }
   ```
## Executing Program
To compile and deploy this program you can use Remix IDE at https://remix.ethereum.org/ .

The file can be save at .sol and should be first compiled by using Solidity Compiler. To complile in Solidity Compiler you navigate to the vertical bar on left and clikc on Solidity compiler below the search button. Here you click "Compile Wbit.sol". The program is now Compiled.

Once compiled you can deploy it by going to Deploy and Run Transactions just below Solidity Compiler. You can deploy by click on the deploy button. Now, the contract is deployed.

The deployed contract and its function can be tested by scrolling down and checking Deployed contracts.

## Created By

Aditya Padwal - Discord - adityx.a #3994
