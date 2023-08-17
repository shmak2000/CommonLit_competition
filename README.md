# CommonLit - Evaluate Student Summaries competition

[Kaggle competition](https://www.kaggle.com/competitions/commonlit-evaluate-student-summaries?rvi=1)</br>
Notebooks for training LLMs on competition dataset + for evaluating</br>
1. For evaluating models i'm using 4-fold CV, with folds, based on summaries themes, so the model is tested on theme, which model have nbever seen.
2. Architecture - different LLM's with mean pooling of the last hidden layer. Pooled vector is the concateneted with text features, which I found, have the biggest correlation with scores - number of unique words, number of sentences, cosine simularity of the summary and prompt text etc. Then there is a self attention layer and fully connected regressor.
3. Used models:</br>
a) RoBERTa base-uncased model</br>
![image](https://github.com/shmak2000/CommonLit_competition/assets/109681522/a1a28434-ba1e-4694-8bd2-45b2678cb848)

b) RoBERTa large-uncased-model</br>
![image](https://github.com/shmak2000/CommonLit_competition/assets/109681522/004c3a71-c0eb-477d-bbb3-000eaddf3cbd)

c) DeBERTa base model</br>
d) DeBERTa large model</br>
......
