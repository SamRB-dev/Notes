### Basics of Probability

Probability is a fundamental concept in statistics and mathematics that measures the likelihood of an event occurring. It ranges from 0 (the event never occurs) to 1 (the event always occurs).

#### 1. Definition
Probability can be defined as the ratio of the number of favorable outcomes to the total number of possible outcomes in an experiment.

#### Formula
$\[ P(A) = \frac{\text{Number of favorable outcomes}}{\text{Total number of possible outcomes}} \]$

#### 2. Types of Probability
- **Classical Probability**: Used when all outcomes are equally likely, such as flipping a fair coin.
- **Empirical Probability**: Based on observations or experiments (e.g., the probability of raining based on historical weather data).
- **Subjective Probability**: Based on intuition or reasoning (not formal calculations).

#### 3. Key Concepts
- **Random Experiment**: An experiment or process for which the outcome cannot be predicted with certainty.
- **Sample Space (S)**: The set of all possible outcomes of a random experiment.
- **Event**: A subset of the sample space.

#### Examples
1. **Coin Toss**: When tossing a fair coin, there are two possible outcomes - Heads (H) or Tails (T). Thus, the probability of getting a head is:
   $\[ P(\text{Heads}) = \frac{1}{2} \]$

2. **Rolling a Die**: When rolling a fair six-sided die, the probability of rolling a 4 is:
   $\[ P(4) = \frac{1}{6} \]$

#### 4. Compound Probability
- **Independent Events**: Two events are independent if the occurrence of one does not affect the occurrence of the other.
- **Dependent Events**: Two events are dependent if the occurrence of one affects the occurrence of the other.

#### Formulas
- **Addition Rule**: 
  $\[ P(A \text{ or } B) = P(A) + P(B) - P(A \text{ and } B) \]$
- **Multiplication Rule for Independent Events**:
  $\[ P(A \text{ and } B) = P(A) \times P(B) \]$
- **Conditional Probability**:
  $\[ P(A|B) = \frac{P(A \text{ and } B)}{P(B)} \]$

#### Examples
1. **Drawing Cards**: If you draw two cards from a deck, the probability of the first card being an Ace and the second card being a King (assuming you don't replace the first card) is:
   $\[ P(\text{Ace then King}) = \frac{4}{52} \times \frac{4}{51} \]$

2. **Rolling Dice**: The probability of rolling a 4 on a die and then rolling a 3 on another die (independent events) is:
   $\[ P(4 \text{ and } 3) = \frac{1}{6} \times \frac{1}{6} \]$

#### 5. Bayes' Theorem
Bayes' Theorem is a way of finding a probability when we know certain other probabilities. It’s written as:
$\[ P(A|B) = \frac{P(B|A) \times P(A)}{P(B)} \]$

#### Example
Suppose 1% of people have a certain disease (A), and the test for this disease is 90% accurate (B). If a person tests positive, Bayes' Theorem can be used to find the probability that they actually have the disease.

### The Complement Rule in Probability

The complement rule is a fundamental concept in probability theory. It states that the probability of an event not occurring is equal to one minus the probability of the event occurring.

#### Formula
If \( P(A) \) is the probability of event \( A \), then the probability of event \( A \) not occurring, denoted as \( P(A') \) or \( P(\text{not } A) \), is:
$\[ P(A') = 1 - P(A) \]$

#### Explanation
- The probabilities of an event and its complement always add up to 1.
- This is based on the idea that an event either happens or it doesn't - these are the only two possibilities.

#### Examples

1. **Coin Toss**:
   - Suppose \( A \) is the event of getting a head when tossing a fair coin. Since $\( P(A) = \frac{1}{2} \)$, the probability of not getting a head (getting a tail) is:
     $\[ P(A') = 1 - \frac{1}{2} = \frac{1}{2} \]$

2. **Drawing a Card from a Deck**:
   - Let \( A \) be the event of drawing an Ace from a standard deck of cards. There are 4 Aces in a deck of 52 cards, so $\( P(A) = \frac{4}{52} = \frac{1}{13} \)$.
   - The probability of not drawing an Ace is:
     $\[ P(A') = 1 - \frac{1}{13} = \frac{12}{13} \]$

3. **Rolling a Die**:
   - Let \( A \) be the event of rolling a 6 on a six-sided die. $\( P(A) = \frac{1}{6} \).$
   - The probability of rolling any number other than 6 is:
     $\[ P(A') = 1 - \frac{1}{6} = \frac{5}{6} \]$

#### Real-World Application
- **Weather Forecasting**: If a weather forecast states there's a 30% chance of rain tomorrow (event \( A \)), the complement (not raining) has a 70% chance:
  $\[ P(\text{not rain}) = 1 - 0.3 = 0.7 \]$

#### Sum of Probability
The sum of probabilities refers to adding the probabilities of different outcomes or events. In a well-defined probability model, there are a few key principles regarding the sum of probabilities:

1. **Probability of the Entire Sample Space**: The sum of the probabilities of all possible outcomes in a sample space is always equal to 1. For instance, in a coin toss, the probability of getting either heads or tails is 1 (P(Heads) + P(Tails) = 1).

2. **Mutually Exclusive Events**: For mutually exclusive events (events that cannot happen at the same time), the probability of any one of the events occurring is the sum of their individual probabilities. If A and B are mutually exclusive, P(A or B) = P(A) + P(B).

3. **Non-Mutually Exclusive Events**: If the events are not mutually exclusive (they can occur together), the probability of either event occurring is the sum of their individual probabilities minus the probability of both occurring. In this case, P(A or B) = P(A) + P(B) - P(A and B).

4. **Complementary Events**: The sum of the probabilities of an event and its complement is 1. For an event A, P(A) + P(Not A) = 1.

### Example
Consider rolling a six-sided die. The probability of each side (1 through 6) landing up is 1/6. The sum of the probabilities for all sides is:

\[ P(1) + P(2) + P(3) + P(4) + P(5) + P(6) = \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} = 1 \]

This sum (1) represents the certainty that one of the six faces will land up.

In the context of probability theory, maintaining the correct sum of probabilities is crucial for the accuracy and reliability of statistical calculations and predictions.