# CommonLit - Evaluate Student Summaries competition

[Kaggle competition](https://www.kaggle.com/competitions/commonlit-evaluate-student-summaries?rvi=1)</br>
Notebooks for training LLMs on competition dataset + for evaluating</br>
1. For **Evaluation** i'm using 4-fold CV, with folds, based on summarie's themes, so the model is tested on theme, which it has never seen.
2. **Architecture** - different LLM's with mean pooling of the last hidden layer. Pooled vector is the concateneted with text features, which I found, have the biggest correlation with scores - number of unique words, number of sentences, cosine simularity of the summary and prompt text etc. Then there is a self attention layer and fully connected regressor.
3. **USED MODELS** - 
For each model I provide a resulting figures for model's CV with train and test values. Validation on test data took place every 10-30 batches.</br>
   - _RoBERTa base-uncased model_</br>
     
   <img src="https://github.com/shmak2000/CommonLit_competition/assets/109681522/a1a28434-ba1e-4694-8bd2-45b2678cb848" width="700">

   - _RoBERTa large-uncased-model_</br>

   <img src="https://github.com/shmak2000/CommonLit_competition/assets/109681522/004c3a71-c0eb-477d-bbb3-000eaddf3cbd" width="700">

   - DeBERTa base model</br>

   <img src="https://github.com/shmak2000/CommonLit_competition/assets/109681522/32c03c9f-2139-405f-8976-27c2368c95fd" width="700">

   - DeBERTa large model</br>
......
