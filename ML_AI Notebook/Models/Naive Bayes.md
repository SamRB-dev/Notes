## Naive Bayes ML Model

### Overview
Naive Bayes is a family of simple yet effective probabilistic classifiers based on applying Bayes' theorem with strong (naive) independence assumptions between the features. It's called "naive" because it assumes that all the features are independent of each other, which is rarely true in real-world data. Despite this assumption, Naive Bayes classifiers often perform surprisingly well in various applications.

### Types of Naive Bayes Classifiers
1. **Gaussian Naive Bayes**: Assumes that the features follow a normal distribution.
2. **Multinomial Naive Bayes**: Used for discrete counts, particularly popular for text classification.
3. **Bernoulli Naive Bayes**: Used for binary/boolean features.

### Bayes' Theorem
The foundation of Naive Bayes is Bayes' theorem, which describes the probability of a hypothesis given observed data:

$\[ P(C|X) = \frac{P(X|C) \cdot P(C)}{P(X)} \]$

Where:
- \( P(C|X) \) is the posterior probability of class \( C \) given the features \( X \).
- \( P(X|C) \) is the likelihood of features \( X \) given the class \( C \).
- \( P(C) \) is the prior probability of class \( C \).
- \( P(X) \) is the probability of the features \( X \).

### Naive Bayes Classifier
For a given feature vector $\( X = (x_1, x_2, \ldots, x_n) \)$, the classifier assigns a class label \( C \) that maximizes the posterior probability \( P(C|X) \).

Given the independence assumption, the likelihood \( P(X|C) \) can be decomposed as:

$\[ P(X|C) = P(x_1|C) \cdot P(x_2|C) \cdot \ldots \cdot P(x_n|C) \]$

Thus, the posterior can be written as:

$\[ P(C|X) \propto P(C) \cdot \prod_{i=1}^{n} P(x_i|C) \]$

### Training Naive Bayes
1. **Estimate Priors \( P(C) \)**:
   $\[ P(C) = \frac{\text{count}(C)}{N} \]$
   where \( \text{count}(C) \) is the number of instances of class \( C \), and \( N \) is the total number of instances.

2. **Estimate Likelihoods \( $P(x_i|C)$ \)**:
   - **Gaussian Naive Bayes**: Assume \( x_i \) follows a normal distribution with mean \( \mu \) and variance \( $\sigma^2$ \):
     $\[ P(x_i|C) = \frac{1}{\sqrt{2\pi\sigma_C^2}} \exp\left( -\frac{(x_i - \mu_C)^2}{2\sigma_C^2} \right) \]$
   - **Multinomial Naive Bayes**: Estimate probabilities of features:
     $\[ P(x_i|C) = \frac{\text{count}(x_i, C)}{\sum_{x_i'} \text{count}(x_i', C)} \]$
   - **Bernoulli Naive Bayes**: Estimate probabilities for binary features:
     $\[ P(x_i|C) = \frac{\text{count}(x_i=1, C)}{\text{count}(C)} \]$

### Prediction
To predict the class for a new instance \( X \):
1. Compute the posterior probability for each class:
   $\[ P(C_k|X) \propto P(C_k) \cdot \prod_{i=1}^{n} P(x_i|C_k) \]$
2. Choose the class with the highest posterior probability:
   $\[ \hat{C} = \arg\max_{C_k} P(C_k|X) \]$

### Example: Email Spam Detection (Multinomial Naive Bayes)
1. **Dataset**: Collection of emails labeled as "spam" or "not spam".
2. **Features**: Words in the emails (bag-of-words model).

**Training**:
- $Calculate \( P(\text{spam}) \) and \( P(\text{not spam}) \).$
- Calculate $\( P(\text{word}_i|\text{spam}) \) and \( P(\text{word}_i|\text{not spam}) \)$ for each word.

**Prediction**:
Given a new email with words $\( X = (\text{word}_1, \text{word}_2, \ldots, \text{word}_n) \)$:
1. Compute:
   $\[ P(\text{spam}|X) \propto P(\text{spam}) \cdot \prod_{i=1}^{n} P(\text{word}_i|\text{spam}) \]$
   $\[ P(\text{not spam}|X) \propto P(\text{not spam}) \cdot \prod_{i=1}^{n} P(\text{word}_i|\text{not spam}) \]$
2. Assign the class with the higher probability.

### When to Use Naive Bayes
- **Suitability**: 
  - When the independence assumption approximately holds.
  - For high-dimensional data (text data).
  - When you need a fast, simple, and interpretable model.

- **Tasks**:
  - Text classification (spam detection, sentiment analysis).
  - Document categorization.
  - Medical diagnosis.
  - Real-time prediction systems.

### Summary
Naive Bayes classifiers are powerful tools for various classification tasks, particularly in text and document classification, due to their simplicity, speed, and effectiveness, even with the strong independence assumption. By understanding the underlying math and implementation steps, you can effectively apply Naive Bayes to suitable problems.