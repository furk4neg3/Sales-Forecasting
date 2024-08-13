Walmart Sales Forecasting
🐈 In this notebook, I've tried to predict Walmart's upcoming sales using various data and models.

🫒 Dataset has Store, Dept, Date, IsHoliday, Temperature, Fuel_Price, CPI, Unemployment and Type as extra features, and I've used all of those in my models. Additionally, I've added Year, Month and Day attributes as features to data too.

🫒 All data operations are done by me, and to be honest, hardest part of this notebook was organizing the data in the way that I wanted to use it. So I recommend checking these parts too.

🫒 First model is naive model which predicts that the next week's sales will be the same as previous week's sales. In general, that's a tough model to beat.

🫒 Second model is a simple dense model. This model predicts next weeks sales using extra informations.

🫒 Before third model, I've done windowing. With that, third model predicts next week's sales usign extra informations and last 7 weeks sales. Model architecture is the same as model 2.

🫒 You can ask, why 7 weeks? To be honest, that's force of habit. When working with daily data, we use last week's (7 days) data to predict next day's data. I've done the same thing for weeks. In the following model, same "force of habit" goes on, like using 30 weeks to predict 7 weeks. As you can predict, that's habit of predicting next week using last month.

🫒 In fourth model, I've changed window size and horizon again. This model predicts next 7 weeks sales based on last 30 weeks sales. This model performed much better than previous ones.

🫒 Fifth model is an LSTM model with average pooling and dense layers. Window size and horizon is the same.

🫒 Last model is a GRU model with the same architecture as model 5, only feature that changed is that I've used GRU instead of LSTM.

🫒 At the end of the notebook, performance of models are visualized for comparison.
