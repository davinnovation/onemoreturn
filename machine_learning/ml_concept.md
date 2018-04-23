# Machine Learning Concept

## ML Algorithm

y = f(x) + error : real world can be represented by this function

(x, y) : training data
h(x|theta) : hypotheses of real world

### top ML algorithm at 2006 (selected by ICDM)
- C4.5 : classification
- CART : classification/regression
- Support Vector Machine (SVM) : classification/regression
- AdaBoost : classification/regression
- kNN : classifciation/regression
- Naive Bayes : classification
- k-Means : clustering
- Apriori : association
- Expectation Maximization : parameter estimation
- PageRank : web search

## ML components
- Model ( Representation ) : how to represent knowledge ( SVM, NN ..)
- Evalutation : evaluate hypotheses ( squared error, likelihood, posterior probability... )
- Optimization : search good theta for hypotheses ( combinational optimization, convex optimization ... )

## Way to start ML

1. Understand the domain, prior knowledg and goals
2. Data integration, selection, cleaning, pre-processing
3. Learning models
    - model selection
    - feature selection

4. go to 1... loop forever

## Reducible and Irreducible Error

E(y-Y)^2 = E[f(x) + error - h(x)]^2 <br>
= [f(x)-h(x)]^2 + E(error^2) - [E(error)]^2 <br>
= [f(x) - h(x)]^2 + Var(error) <br>
= Reducible error + Irreducible error

- Reducible eror : Epistemic uncertainty
- Irreducible error : Aleatoric uncertainty

## Bias-Variance Tradeoff

![b-v-tradeoff](http://scott.fortmann-roe.com/docs/docs/BiasVariance/biasvariance.png)

### Bias
how closely a model reality (goodness of fit)

### Variance
how much a model dependent on data

### Relation Bias-Variance
more complex model == low bias == over fitted
more simple model == low variance ( robustness )

## Training, Validation, Test

`training set` : used for fit parameters of model
`validation set` : used for tune hyperparameters ( part of training )
`test set` : measure preformance of model

- k-fold cross validation
    
    1. split dataset : K set
    2. Training Phase 
        - Train Set ( 1, 2, ... K-1 ) / Test : ( K )
        - Train Set ( 1, 2, ... K-2, K ) / Test : ( K-1 )
        - ... K Sets

- Leave-one-out cross validaton
    - extreme case of k-fold CV ( k is datasize! )

- Bootstrapping
    - randomly select M sample from dataset for training set, rest data use for test set

## Ref
- http://scott.fortmann-roe.com/docs/BiasVariance.html