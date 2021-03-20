## Xgboost

XGBoost is one of the most powerful ML algorithm from tree ensemble group. XGboost based on the decision tree answer search and its using GradientBoosting framework. Before going into XG boost it is necessary to look at the other similar ensemble machine learning algorithms where the result is calculated as a function of several insividual predictors.<p>

*There are 2 main types of decision tree ensemble:*<p>

1. **Bagging**
2. **Boosting**

Using both bagging and boosting several weak learners can be combined together to become a strong learner. For eample a coin having a bias of 51 heads in 100 toss of coin probability of majority head is only 51 percent but when the same coin is tossed 10000 times the probability of majority head becomes nearly 97 percent. This is known as law of Large numbers.<p> 

In Bagging we combine predictors from multiple-decision trees through a majority voting mechanism. A simple random forest may be an example of the bagging ensemble. Random forest uses bootstapping and bagging to arrive at the result. It also adds extra randomness by selecting the best freature among the random subset of features.<p>

In Boosting we build models sequentially by minimizing the error from previous models while increasing (or boosting) influence of high performance models. Examples of boosting are Ada Boost where the algorithm first trains a base classifier and uses it to make prediction on the training set. The algorithm then increases the relative weight of the misclassified  training instances, then train the second classifier using the updated weights and again make prediction on the training set. It stops after the specified level or no error is seen in the next stage. The output is decided then as a combination from all these classifiers according to their amount of say.<p>

A special case of Boosting in which the error is minimized is Gradient Descent Algorithm (GDA-optimization algorithm)-in case of recruitment process- the least qualified candidates are eliminated as early as possible.
Just like AdaBoost, Gradient boosting works by sequentially adding predictors to an ensemble, each one correcting its predecessor. However changing the instant weight at every iteration like AdaBoost does. This method tries to fit the new predictor to the residual errors made by the previous predictor.<p>

XGBoost and Gradient Boosting Machines (GBMs) are both ensemble tree methods that apply the principle of boosting weak learners (CARTs generally) using the gradient descent architecture. However, XGBoost improves upon the base GBM framework through systems optimization and algorithmic enhancements.<p>

XGBoost aquires this high optimisation using the techniques of<p>

1. **Parallelization**: XGBoost approaches the process of sequential tree building using parallelized implementation. This is possible due to the interchangeable nature of loops used for building base learners<p>

2. **Tree Pruning**: The stopping criterion for tree splitting within GBM framework is greedy in nature and depends on the negative loss criterion at the point of split. XGBoost uses ‘max_depth’ parameter as specified instead of criterion first, and starts pruning trees backward<p>

3. **Hardware Optimization**: This algorithm has been designed to make efficient use of hardware resources. This is accomplished by cache awareness by allocating internal buffers in each thread to store gradient statistics. Further enhancements such as ‘out-of-core’ computing optimize available disk space while handling big data-frames that do not fit into memory.<p>

It also enhances the algorathmic performance by the methods of :<p>

1. ***Regularization***: It penalizes more complex models through both LASSO (L1) and Ridge (L2) regularization to prevent overfitting.<p>

2. ***Sparsity Awareness***: XGBoost naturally admits sparse features for inputs by automatically ‘learning’ best missing value depending on training loss and handles different types of sparsity patterns in the data more efficiently.<p>

3. ***Weighted Quantile Sketch***: XGBoost employs the distributed weighted Quantile Sketch algorithm to effectively find the optimal split points among weighted datasets.<p>

4. ***Cross-validation***: The algorithm comes with built-in cross-validation method at each iteration, taking away the need to explicitly program this search and to specify the exact number of boosting iterations required in a single run.<p>
    
    
Due to all these reasons XGBoost is the one of the best ensemble mothod of machine learning currently available and it is widely used in the impovement of model performance. It offers high accuracy without compromising the time of modeling and complexity.
