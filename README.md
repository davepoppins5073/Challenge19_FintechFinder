# Challenge19_FintechFinder
![19-4-challenge-image](https://user-images.githubusercontent.com/101449950/182271347-b5fd5856-a53d-4612-b32c-3c1f444a9dd3.png)


## User Story
<p>You work at a startup that is building a new and disruptive platform called Fintech Finder. Fintech Finder is an application that its customers can use to find fintech professionals from among a list of candidates, hire them, and pay them. As Fintech Finder’s lead developer, you have been tasked with integrating the Ethereum blockchain network into the application in order to enable your customers to instantly pay the fintech professionals whom they hire with cryptocurrency. In this Challenge, you will complete the code that enables your customers to send cryptocurrency payments to fintech professionals</p>

## Directions
There are two files in the repo:
1. fintech_finder.py - contains web interface code for the  application. 
3. crypto_wallet.py -  contains the Ethereum transaction functions

Using import statements, the crypto_wallet.py script will be integrated into the Fintech Finder interface program in fintech_finder.py file. Integrating these two files will allow you to automate the tasks associated with generating a digital wallet, accessing Ethereum account balances, and signing and sending transactions via a personal Ethereum blockchain called Ganache.

### To-Do

1. Generate a new Ethereum account instance by using the mnemonic seed phrase provided by Ganache.
2. Fetch and display the account balance associated with your Ethereum account address.
3. Calculate the total value of an Ethereum transaction, including the gas estimate, that pays a Fintech Finder candidate for their work.
4. Digitally sign a transaction that pays a Fintech Finder candidate, and send this transaction to the Ganache blockchain.
5. Review the transaction hash code associated with the validated blockchain transaction.

--- 

## Code

### Imports
```python
# Imports

import streamlit as st
from dataclasses import dataclass
from typing import Any, List
from web3 import Web3

w3 = Web3(Web3.HTTPProvider('HTTP://127.0.0.1:7545'))

# From `crypto_wallet.py 
# import functions: generate_account, get_balance, send_transaction

from crypto_wallet import generate_account,get_balance,send_transaction
```
