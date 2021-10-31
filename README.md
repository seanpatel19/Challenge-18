# Challenge-18

## Block Chain Ledger  

We are Fintech Engineers at a top 5 bank. Our task is to build a blockchain-based ledger system, complete with a user-friendly web interface. This ledger should allow partner banks to conduct financial transactions (that is, to transfer money between senders and receivers) and to verify the integrity of the data in the ledger.

To accomplish this we need to do the following:

Step 1: Create a Record Data Class

Step 2: Modify the Existing Block Data Class to Store Record Data

Step 3: Add Relevant User Inputs to the Streamlit Interface

Step 4: Test the PyChain Ledger by Storing Records


## Create a Record Data Class

Step 1: Define a new class named Record.

Step 2: Add the @dataclass decorator immediately before the Record class definition.

Step 3: Add an attribute named sender of type str.

Step 4: Add an attribute named receiver of type str.

Step 5: Add an attribute named amount of type float.

## Modify the Existing Block Data Class to Store Record Data

Step 1: In the Block class, rename the data attribute to record.

Step 2: Set the data type of the record attribute to Record.

## Add Relevant User Inputs to the Streamlit Interface

Step 1: Delete the input_data variable from the Streamlit interface.

Step 2: Add an input area where you can get a value for sender from the user.

Step 3: Add an input area where you can get a value for receiver from the user.

Step 4: Add an input area where you can get a value for amount from the user.

Step 5: As part of the Add Block button functionality, update new_block so that Block consists of an attribute named record, which is set equal to a Record that contains the sender, receiver, and amount values. The updated Blockshould also include the attributes for creator_id and prev_hash.

## Test the PyChain Ledger by Storing Records

Step 1: In the terminal, navigate to the project folder where you've coded the Challenge.

Step 2: In the terminal, run the Streamlit application by using streamlit run pychain.py.

Step 3: Enter values for the sender, receiver, and amount, and then click the Add Block button. Do this several times to store several blocks in the ledger.

Step 4: Verify the block contents and hashes in the Streamlit drop-down menu. Take a screenshot of the Streamlit application page, which should detail a blockchain that consists of multiple blocks. Include the screenshot in the README.md file for your Challenge repository.

Step 5: Test the blockchain validation process by using the web interface. Take a screenshot of the Streamlit application page, which should indicate the validity of the blockchain. Include the screenshot in the README.md file for your Challenge repository.

---

## Technologies
This application is written in Python 3.7  

this application uses the following packages:

Pandas  https://pandas.pydata.org

dataclasses https://docs.python.org/3/library/dataclasses.html

typing https://pypi.org/project/typing/

hashlib https://docs.python.org/3/library/hashlib.html

streamlit https://streamlit.io



---

## Installation Guide

Before running the application first install the following dependencies.
See the associated Screenshot for what to Install 

![imports](https://github.com/seanpatel19/Challenge-18/blob/bc543fb11ec798be8aaaa07b042917861458499b/images/installs.png)




---

## Proof of Work

Please see the following screenshots of code 

### Creating the fields for the user to input 

![input code](https://github.com/seanpatel19/Challenge-18/blob/bc543fb11ec798be8aaaa07b042917861458499b/images/streamlit%20input%20codes.png)


### Inputs via Streamlit 

![streamlit input](https://github.com/seanpatel19/Challenge-18/blob/bc543fb11ec798be8aaaa07b042917861458499b/images/streamlit%20inputs.png)

Adding to the blockchain 

![block expanded](https://github.com/seanpatel19/Challenge-18/blob/bc543fb11ec798be8aaaa07b042917861458499b/images/block%20expanded.png)


Validated chain 

![valid chain](https://github.com/seanpatel19/Challenge-18/blob/bc543fb11ec798be8aaaa07b042917861458499b/images/chain%20valid.png)







---

## Usage

To use the data simply clone the repository. This can also be used via Google Collab but I chose jupyter notebook 

Different layers could be added as well ad different values of the layers 
```
---

## Contributors

Sean Patel (myself) seanpatel076@gmail.com
---

## License

License is public anyone can use or make changes to this application
