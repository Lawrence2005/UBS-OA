**Data Analytics Problem**\
This test is from agency algorithmic trading quant team. Our team work on agency eletronic trading execution.

The main task of a trading algo is to buy/sell a certain amount of stock shares within some given horizon. For example, buy 10000 shares of 0700.HK before 3:50 p.m. Instead of manually submitting orders, we do it through a trading program with minimal human intervention. With these algos, we are able to execute thousands of orders for our clients at the same time.

This problem descibes a simplified version of a typical problem we face in our daily work.

Imagining having two trading algorithms, algo_1 and algo_2, and we would like to assess their performance. In this problem, we focus on IS Slippage (Arrival Slippage), which is defined as IS_slippage = 10000*(side)*(Execution Price - Arrival Mid Price)/Arrival Mid Price.

 - For a buy order we have side = 1, and for sell and short sell orders we have side = -1. 
 - Arrival Mid Price is the mid price at order arrival.
 - These orders are fully filled.

We have a few additional measurements.
- **Volatility**: The estimated daily volatility in basis points
- **Average Spread**: The average spread, defined as (best ask - best bid)/mid in basis points
- **Order Size**: size of the order / daily volume in basis points. E.g. ordersize = 10 means the order size is 10bps = 0.1% of the traded volume on that day.
- **Duration**: Order Duration / (Close Auction Time - Open Auction Time). duration = 1 means the order lasted for a full day.
- **Notional**: Size of the order in some currency, e.g. CNY.



**Requirements:**

- You have 2 days for this problem. Please submit a report in ipynb/pdf/doc etc. 
- **PLEASE INCLUDE YOUR NAME** in the final uploaded zip/pdf file. E.g. yourName_UBS_Quant.zip
- Please ensure that every question is answered with both words and code. Avoid submitting a notebook that contains only code without any explanation. \
**Format example:** \
Q1:How would you compare the IS slippage of algo_1 and algo_2？Which one do you think performs better (smaller IS slippage)? Why? \
**Markdown Cell**: Your written answer To Q1. There are 3 question marks in Q1, so you should have answers to each of these questions.\
**Code Cells**: Your code / charts

- If you do not know to to solve a particular problem, please write down what your thoughts are.
- Please feel free to use any tool available to you including AI. If you are using AI, please demonstrate how you prompt & any validations on the AI's response.
- The data is in TCA_problem.csv


**Problems:**
1. How would you compare the IS slippage of algo_1 and algo_2？Which one do you think performs better (smaller IS slippage)? Why?
2. Compute the notional weighted IS slippage of both algos. How would you interpret this number? What is its economic interpretation? How would you measure a single order's contribution to the notional weighted average?
3. Plot and describe the disitrbution of the 'features'. i.e. Volatility, Average Spread, Order Size and Duration.
4. What do you think is the relationship between the features and IS slippage? (You could start with monotonicity) Model IS slippage as a random variable whose parameters depend on the features. Explain how you determine your model. 
5. Fit your model if possible. How would you interpret your fitting results? Which algo do you think is better? Why?
6. [Optional] What if some orders are partially filled? (Hint: Construct an algo that may not fully fill but always beats arrival mid) How would you compare two algos when one algo requires fully fill while the other does not?
7. [Optional] Describe how you would tackle this problem if you have access to more features. What features do you think might help?
8. [Optional] Any feedback on this problem is welcome.
9. When are you available for the internship, and how many days can you come to office per week? (e.g., from Jan 1 to Apr 30, 5 days/week)