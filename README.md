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

Pathlib https://docs.python.org/3/library/pathlib.html

Numpy https://numpy.org

Hvplot https://hvplot.holoviz.org/index.html

Matplotlib https://matplotlib.org

Sklearn https://scikit-learn.org/stable/index.html

---

## Installation Guide

Before running the application first install the following dependencies.
See the associated Screenshot for what to Install 

![imports](https://github.com/seanpatel19/Challenge-14/blob/04817cff05989aea7629b9be2d8c92ca377a00ef/Images/imports%20.jpg)




---

## Evaluation Report

During our evaluation of the current model the following imputs were used.

The first time frame looked at was 3 months.

![original time sample](https://github.com/seanpatel19/Challenge-14/blob/04817cff05989aea7629b9be2d8c92ca377a00ef/Images/time%20sample%20original.png)

The first set of moving averages looked at where 4 days and 100 days 
![original SMAs](https://github.com/seanpatel19/Challenge-14/blob/04817cff05989aea7629b9be2d8c92ca377a00ef/Images/SMA%20original.png)

The original classification report shows that the model should be useful with a weighted average of 77 and very high recall and precision in longing and shorting respectively

![original classification report](https://github.com/seanpatel19/Challenge-14/blob/04817cff05989aea7629b9be2d8c92ca377a00ef/Images/original%20classification%20report%20.png)

While the numbers seem good the performance of this strategy is not desirable as it underperforms 

![original returns graph](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/plotted%20returns.png)

I set out to tune the model to find some better performance.

One of the things I did was to increase the time horizon that was used for testing, from 3 months to 6 months.

This was coupled with adjusting the moving averages used as trading signals. We decided on using a shorter SMA horizon with 14 days being our "Fast" SMA and 30 being our "Slow" SMA 

These changes together produced this classification report which on the surface looks worse than the original classification report with a whole 20 points lower on weighted average and much worse recall and precision.

![new classification report](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/New%20classifciation%20report.png)

Despite this the returns were much better and outperformed. As this new model outperformed on nearly all times frames, I believe that changing the moving averages had a greater effect than increasing the time period that we looked at originally  

![new plotted returns](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/new%20plotted%20returns.png)

Another model was used on the original time frame and original moving averages to see if more performance could be gained. I used Logisitic Regression to see if that created any improvements. 

While the classification report showed a lower weighted average than the previous model with time frame changes, we have seen that better weighted average does not guarantee better trading results 

![logisitic regression classfication report](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/lr%20classifcation%20report.png)

But this model is no good. It lags actual returns to such an extent, I am of the opinion that logistic regression is not suitable for a trading algorithms

![lr returns plotted ](https://github.com/seanpatel19/Challenge-14/blob/ed60de7fdd7d8a0fb77104fb66908e4b54ba3b89/Images/new%20model%20graph.png)


### Conclusions 

I would appear that Support Vector Machine (SVM) learning is suitable for putting together a trading strategy. 

The updated model appears to work well enough, that it should be fitted to other assets to see what sort of performance gains could be found. 

It would also be useful to look at the returns of the model over a very long time horizon to see how well it does. 

During a 6 month timeframe the new 14 and 30 SMA SVM is a winning trading algo.


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
