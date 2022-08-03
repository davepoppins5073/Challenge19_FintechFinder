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
---
## Running The Code (Inspecting Transaction)
### Instructions

1. From your terminal, navigate to the project folder that contains your `.env` file and the `fintech_finder.py` and `crypto_wallet.py` files.
2. To launch the Streamlit application type the following:

 ```python
 streamlit run fintech_finder.py`.
 ```
 
3. On the resulting webpage, select a candidate that you would like to hire. Then, enter the number of hours that you would like to hire them for.
4. Click the Send Transaction button to sign and send the transaction with your Ethereum account information. 
5. Navigate to the Ganache accounts tab and locate your account (index 0).
6. Navigate to the Ganache transactions tab and locate the transaction.

##### Screenshot

<img width="874" alt="Screen Shot 2022-08-02 at 11 36 04 PM" src="https://user-images.githubusercontent.com/101449950/182518723-9465db37-ab2c-4d3d-a8e5-32d490f80ecc.png">


![image](https://user-images.githubusercontent.com/101449950/182516678-c12241e8-01a5-47bf-86aa-388442fc601f.png)



![image](https://user-images.githubusercontent.com/101449950/182516882-d6436b06-fb3d-4dce-85bd-3d1e152a005f.png)
