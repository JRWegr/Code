# Prediction vs. Inference: does the best model depend on the goal?

For Module 02, I wanted to see whether the module's idea, that prediction and inference can disagree, also applies to choosing between model types, not just to omitting a variable.

I simulated house prices with a known square footage effect (0.1 per sq ft) and made the effect of age curved instead of linear. Then I fit OLS and a k-nearest neighbors model (both written in numpy, no sklearn) and scored them two ways: test RMSE for prediction, and how close each model's estimate of the square footage effect was to 0.1 for inference. For KNN I estimated the effect by adding 100 sq ft to every test house and averaging the change in predicted price.

| Model | Test RMSE | Sq ft effect (true = 0.1) |
|-------|-----------|---------------------------|
| OLS   | 16.99     | 0.101                     |
| KNN   | 8.18      | 0.096                     |

KNN predicts much better because it can follow the curve in age. OLS gets the square footage effect a little closer to the truth, and it gives me that effect as a single coefficient, while KNN has no coefficient at all. The inference gap is small here, so the main difference is that OLS is easy to interpret and KNN isn't.
