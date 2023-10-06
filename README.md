# CommonLit - Evaluate Student Summaries

The data is taken from [kaggle competition](https://www.kaggle.com/competitions/commonlit-evaluate-student-summaries?rvi=1)</br>
The goal is to assess the quality of students summaries by estimating two scores - *wording* and *content*.</br>

1. For **Evaluation** i'm using 4-fold CV, with folds, based on summarie's themes, so the model is tested on theme, which it has never seen.
2. **Architecture** - different LLM's with mean pooling of the last hidden layer. Pooled vector is then concateneted with extracted text features, which have the biggest correlation with scores - number of unique words, number of sentences, cosine simularity of the summary and prompt text etc. Then there is a self attention layer and fully connected regressor.
3. **USED MODELS** - 
For each model I provide a resulting plot for model's CV with train and test values. Validation on test data took place every 10-30 batches.</br>
   - RoBERTa large-uncased model</br>
     
   <img src="https://github.com/shmak2000/CommonLit_competition/assets/109681522/e029db07-74cc-433f-8136-0212c132a0bb"
 width="700">

   - BART-base-model</br>

   <img src="https://github.com/shmak2000/CommonLit_competition/assets/109681522/828f821f-206a-4eba-b589-abbfe6e1e778" width="700"></br>

   - DeBERTa base model</br>

   <img src="https://github.com/shmak2000/CommonLit_competition/assets/109681522/5f028d37-621d-4038-b943-2fac86b6883e" width="700"></br>

Here, I got the best results with RoBERTa model trained for 3 epochs
