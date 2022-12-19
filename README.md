# 2022-fall-ADM-hw02-starter
In this homework assignment, you will extend your hw01 by adding the Neural Collaborative Filtering [1]. You will test your new implementation using the same Netflix Prize data.

1. Read the paper [1]
2. Transform the Neflix data into implicit data in a way similar to the MovieLens used in the paper (see Section 4.1).
3. Implement the following 3 models and compare their performance with the best model from your previous assignment (hw01). The previous best model will serve as a baseline, and the 3 new models are described in the paper [1].
    * (B1) your best model from hw01
    * (N1) GMF (section 3.2)
    * (N2) MLP (section 3.3)
    * (N3) NeuMF (section 3.4): You can do it with or without pre-training. According to the paper, NeuMF with pre-training performed better, but it may not hold for different implementations.

   **Note:** The author published a GitHub repository using tensorflow (keras) [2], and there are also implementations using PyTorch [3-5]. Do not rely on existing implementations; try to implement your own models without looking at these repositories. You will compare your own implementation with one of these existing implementations. Pick one of these repositories (and indicate which one you pick) as your reference repository. Create the following reference models using the reference repository:

    * (R1) GMF
    * (R2) MLP 
    * (R3) NeuMF 
4. Compare the 7 models and report the performance comparison in terms of HR and NDCG. Use the same 80-20 split as in hw01 for training and testing data. You can design any experiments to train your classifiers using the training set -- as long as you don't touch the testing set. Report the performance for factors=16, 32, 64 for the 7 models, in terms of HR@10 and NDCG@10. The performance can be shown in two tables, one for HR and one for NDCG.

   **Note:** You can adopt the evaluation code from existing repositories, e.g., [evaluation.py](https://github.com/hexiangnan/neural_collaborative_filtering/blob/master/evaluate.py) from the author's repository [1].

5. Generate a reproducible notebook to report your work in this assignment. Create a "Result Summary" section (at the beginning or the end of your report. This section should have four parts:
    1) Performance table(s) to show the final results on the test set, for the 7 models, in terms of the two performance metrics.
    2) Create 2 plots similar to Fig 4(a)(b). Plot performance over factors (=16, 32, 64) for the 7 models testing on Netflix data.
    3) Create 2 plots similar to Fig 5(a)(b). Plot performance over K (=1, 3, 5, 7, 9) for the 7 models testing on Netflix data.
    4) In 1-2 paragraphs, summarize the model performance based on the tables and plots (e.g., which one performs the best, the worse, and how).
    5) Compare your implementation with the reference repository, and discuss how your implementation differs from that. You are allowed to fail in your own implementation or to implement not-so-great models. In this case, discuss how you fail or did worse. Finally, summarize what you learn from this assignment.


## References
[1] He, X., Liao, L., Zhang, H., Nie, L., Hu, X., & Chua, T. S. (2017, April). Neural collaborative filtering. In Proceedings of the 26th international conference on world wide web (pp. 173-182). [paper](https://dl.acm.org/doi/abs/10.1145/3038912.3052569?casa_token=5_HZO-oED74AAAAA%3Aet4MxQdQ5yw62O_XlPpKxhxrmRAbdM70bFuMyHDzITrSCr3cG_64Yl855vMIsDxx7EAs46u4jfW9fQ)

[2] https://github.com/hexiangnan/neural_collaborative_filtering

[3] https://github.com/pyy0715/Neural-Collaborative-Filtering

[4] https://github.com/yihong-chen/neural-collaborative-filtering

[5] https://github.com/guoyang9/NCF
