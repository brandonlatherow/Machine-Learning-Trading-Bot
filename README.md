# Machine Learning Trading Bot

![Decorative image.](Images/14-challenge-image.png)

Now, it's time to take what you've learned about machine learning and apply it to new situations. For this optional assignment, you'll create an algorithmic trading bot that learns and adapts to new data and evolving markets. Be sure to give it your all -- as the skills you hone will become powerful tools in your FinTech tool belt.

## Background

In this Challenge, you’ll assume the role of a financial advisor at one of the top five financial advisory firms in the world. Your firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, your firm has heavily profited by using computer algorithms that can buy and sell faster than human traders.

The speed of these transactions gave your firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. You’re thus planning to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, you’ll enhance the existing trading signals with machine learning algorithms that can adapt to new data.


## Baseline ML Model

![Baseline](images/baseline.png)

Up until around 2019, the actual returns were about the same as the strategy returns. During the latter half of 2018 and going into 2019, the strategy returns started to perform better than the actual returns. Overall, although the strategy returns did start to perform better than the actual returns at a certain poinnt - it can be concluded that this algorithm does need some tweaking. In an algorithm, we do not want strategy returns to only be better sometimes, we want them to be better throughout the entire time.

## Evaluating Decreased Date Offset

![Two Months](images/two_months.png)

For this model, I kept everything the same other than decreasing the offset for the training data from 3 months to 2 months. The resulting model was slightly worse, with the strategy returns being higher than actual returns during similar periods - but generally by a smaller margin.

## Evaluating Altered Date Windows

![SMA Change](images/sma_long_90_short_10_1_month.png)

For this model, I changed the short window from 4 to 10, the long window from 100 to 90, and the offset date to 1 month. The model was worse than the previous two. Strategy returns were only better than actual returns for a short period of time between 2019 and 2020. Other than that, Strategy and Actual returns were relatively the same.

## Evaluating New Logistic Regression ML Model

![Updated Algorithm](images/new_ml.png)

This new model has some of the same issues as the last one, but slightly worse. During the beginning of the period, the strategic and actual returns stayed about the same, until the actual returns started performing even better than the strategic returns. Around 2019, the strategic returns began performing better than the actual returns, but then began performing worse again near the end of 2020 and start of 2021. 


## Conclusion

After doing some trial and error on my own, I found that a 1 month offset date was best, with the short window altered to 30, and the long window altered to 60. Throughout my trial and error, I even tried differentiating between days instead of months, but found that did not make as much of a difference as I would have hoped. 

![Final ML Model](images/final_ML_model.png)





© 2022 edX Boot Camps LLC. Confidential and Proprietary. All Rights Reserved.
