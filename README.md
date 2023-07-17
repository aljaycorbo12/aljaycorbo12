Solidity Assessment


This Solidity program is a simple "get_a_token" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

DESCRIPTION 

This project is for the completion of the Solidity Beginner in Metacrafter. It has a coded that intended to be used as a kind of practice in making my own token. Although it might not have anything special in particular. It includes an external mint and burn function that takes two parameters: address and value. It was made to be external to limit the access only to other contracts and also to have a cheaper gas usage as public will consume more gas. The mint function meant to perform increase in the amount of total supply and the balances of the sender of token. The burn function meant to perform deduction in the amount of total supply and the balances of the sender will then be deducted from that amount. It has condition that the burn function will only perform if the balances of address of sender is greater than or equal to the amount supposed to be burned. It will not perform as long as the balances of the sender is less than to avoid getting all balances burned.

EXECUTING PROGRAM
To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (Solidity Assessment.sol). Copy and paste the following code into the file:


    string public tokenName = "TOKEN";
    string public tokenAbbrv = "TKN";
    uint public totalSupply = 0;

    
    mapping (address => uint) public balances;

  
    function mint (address _address, uint _value) external  {
        totalSupply += _value;
        balances[_address] += _value;
    }

  
    function burn (address _address, uint _value) external  {
        if (balances[_address] >= _value) {
            totalSupply -= _value;
            balances[_address] -= _value;
        }
    }

}
To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.4" (or another compatible version), and then click on the "Compile Solidity Assessment.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "Solidity Assessment" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can paste the link in account and paste to "burn" and type the value
click the transact and finally retrieve the ammount 

AUTHORS 

aljaycorbo 




