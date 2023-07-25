To run the program, simply hit the play button in an iPython Notebook, or hit 'shift' + 'Enter' for each cell

# SVM vs Baseline
The SVM model keeps pace with the baseline DMAC algorithm for around half the testing period before it starts outperforming it fairly consistently. The returns between the two algorithms isn't huge but it is substantial enough, and the SVM is simply the smarter algorithm to choose for this dataset.
The SVM model itself predict able to predict buy signals with very high recall, but struggles with sell signals.

# Tuned model
To attempt tuning the model for better performance, the training period was increased from 3 months to 5 months. This resulted in drastic overfitting of the model. This can be seen in the plot, where the tuned model severely underperforms the baseline in the second half of the testing period.
The accuracy and recall of the buy and sell signals remains relatively stagnant when doing this, and given the plot, we can see that the classification report can be a bit misleading when comparing the 3 month training period and the 5 month one.

For the next attempt, the training period was reset to 3 months, but the short window was increased to 7 days from 4. This resulted in a model that follows very closely with the baseline, however begins to underperform toward the end of the testing period.
The model had a higher precision predicting sell signals, but the recall was 0. Overall, the model is worse than the baseline DMAC.

Inevitably, the baseline model performed better without any tuning.

# AdaBoost model
The AdaBoost model is much better at predicting sell signals than the SVM. Compared to the baseline, it follows it very closely for the first half, with the second half having some variation, but most of the time it outperforms the baseline. There is a period from 2020-2021 where the model substantially
outperforms the baseline, where the baseline returns pale in comparison to the AdaBoost results. There is some level of uncertainty based on the plot, but overall it is safe to assume the model will outperform the baseline.

# Summary
In summary, the machine learning models provide effective ways to create trading strategies better than a traditional DMAC for this stock. Becuase the SVC follows so closely with the DMAC, it is a better algorithm for a more risk averse investor, whereas an investor willing to take on more risk is likely to
succeed with the AdaBoost classifier. While the AdaBoost has some more uncertainty and at times underperforms compared to the baseline, though not by much, it is also capable of overperforming by a significant margin and can yield more profit. Both the SVC and the AdaBoost are thus better tools than a simple
DMAC based on this analysis.
