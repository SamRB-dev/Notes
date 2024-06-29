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

$\[ P(1) + P(2) + P(3) + P(4) + P(5) + P(6) = \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} + \frac{1}{6} = 1 \]$

This sum (1) represents the certainty that one of the six faces will land up.

In the context of probability theory, maintaining the correct sum of probabilities is crucial for the accuracy and reliability of statistical calculations and predictions.

#### **Joint and Disjoint Events in Probability**

**Definition:**
- **Joint Events**: In probability theory, joint events refer to events that occur together or simultaneously. They represent the intersection of two or more events.
- **Disjoint Events**: Disjoint events, also known as mutually exclusive events, are events that cannot occur at the same time. If one event happens, the other(s) cannot happen.

**Simple Explanation:**
- **Joint Events**: Imagine rolling two dice. The event of getting a 3 on the first die and a 4 on the second die is a joint event because it involves both dice simultaneously.
- **Disjoint Events**: Using the same example, the event of getting a 2 on the first die and a 6 on the second die is disjoint with the event of getting a 3 on the first die and a 4 on the second die because they cannot happen simultaneously.

**Formulas and Representations:**
- **Joint Probability**: The probability of the intersection of two events A and B is denoted as P(A ∩ B) or P(A and B). If A and B are independent, the joint probability is calculated as the product of their individual probabilities: P(A ∩ B) = P(A) * P(B).
- **Disjoint Probability**: The probability of the union of two disjoint events A and B is denoted as P(A ∪ B) or P(A or B). For disjoint events, the probability of their union is the sum of their individual probabilities: P(A ∪ B) = P(A) + P(B).

**Use Cases:**
- **Joint Events**: 
  - In genetics, the probability of inheriting certain traits from both parents involves joint events.
  - Weather forecasting may involve joint events, such as the probability of rain and strong winds occurring together.
- **Disjoint Events**:
  - In a card game like poker, the probability of getting a straight flush or a full house are disjoint events because you cannot have both simultaneously.
  - When analyzing outcomes of medical tests, the probability of a positive result for one condition and a positive result for a different condition may be disjoint.

**Mathematical Examples:**
1. **Joint Probability Example**:
   - Suppose you flip a fair coin twice. Let A be the event of getting heads on the first flip, and B be the event of getting tails on the second flip.
     - P(A) = P(B) = 1/2 (since it's a fair coin)
     - P(A ∩ B) = P(A) * P(B) = (1/2) * (1/2) = 1/4

2. **Disjoint Probability Example**:
   - Consider rolling a standard six-sided die. Let A be the event of getting an even number (2, 4, or 6), and B be the event of getting an odd number (1, 3, or 5).
     - P(A) = 3/6 = 1/2 (since there are 3 even numbers out of 6)
     - P(B) = 3/6 = 1/2 (since there are 3 odd numbers out of 6)
     - Since A and B are disjoint, P(A ∪ B) = P(A) + P(B) = 1/2 + 1/2 = 1

In summary, joint events involve the simultaneous occurrence of multiple events, while disjoint events are events that cannot occur together. Understanding these concepts is crucial for analyzing probabilities and making informed decisions in various fields.

#### **Independence in Probability**

**Definition:**
Independence in probability refers to the relationship between two or more events where the occurrence of one event does not affect the probability of the occurrence of the other event(s). In other words, the outcome of one event provides no information about the outcome of the other event(s).

**Simple Explanation:**
Imagine rolling a fair six-sided die twice. The outcome of the first roll (e.g., rolling a 4) does not influence the outcome of the second roll. Whether you roll a 4, a 3, or any other number on the first roll, the probability of rolling a particular number on the second roll remains the same (1/6).

**Formulas and Representations:**
- **Independence of Events A and B**: Two events A and B are considered independent if and only if the probability of their intersection (joint probability) equals the product of their individual probabilities:
  - P(A ∩ B) = P(A) * P(B)

**Use Cases:**
- **Coin Flips**: The outcome of one coin flip is independent of the outcome of any other coin flip. Whether you get heads or tails on the first flip does not affect the outcome of subsequent flips.
- **Dice Rolls**: Rolling a fair die multiple times. The outcome of each roll is independent of the outcomes of previous rolls.
- **Card Draws**: Drawing cards from a well-shuffled deck. The probability of drawing a specific card on one draw does not change based on previous draws, assuming the deck remains well-shuffled.

**Mathematical Examples:**
- Suppose you flip a fair coin twice. Let A be the event of getting heads on the first flip, and B be the event of getting tails on the second flip.
  - P(A) = P(B) = 1/2 (since it's a fair coin)
  - P(A ∩ B) = P(A) * P(B) = (1/2) * (1/2) = 1/4
  - Since P(A ∩ B) = P(A) * P(B), events A and B are independent.

- Consider rolling a fair six-sided die twice. Let A be the event of getting an odd number (1, 3, or 5) on the first roll, and B be the event of getting an even number (2, 4, or 6) on the second roll.
  - P(A) = P(B) = 1/2 (since there are 3 odd and 3 even numbers)
  - P(A ∩ B) = 0 (since an odd number on the first roll ensures an odd number on the second roll, making it impossible for B to occur)
  - Since P(A ∩ B) = 0 = P(A) * P(B), events A and B are independent.

Understanding independence in probability is essential for making accurate predictions and modeling various real-world scenarios. It allows us to analyze the probability of multiple events occurring together without being influenced by each other.

#### *Conditional Probability*
**Definition**: If A and B are two events associated with the same sample space of a random experiment, **the conditional probability of event A given that B has occurred is given by P(A/B) = P( A ∩ B)/ P (B)**, provided P(B) ≠ 0.

**Properties of Conditional Probability**: 
1. Let S be the sample space of an experiment and A be any event. Then $P(S | A) = P(A | A) = 1$.
2. Let S be the sample space of an experiment and A and B be any two events. Let E be any other event such that P(E) ≠ 0. Then $P((A ⋃ B) | E) = P(A | E) + P(B | E) - P((A ∩ B) | E)$.
3. $P(A' | B) = 1 - P(A | B)$, where A' is the [complement of the set](https://www.cuemath.com/algebra/complement-of-a-set/) A.
4. two event A and B are said to be dependent events if one of the conditions is satisfied.
	- P(A ∩ B) = P(A | B) · P(B) (or)
	- P(A ∩ B) = P(B | A) · P(A)
5. two events are said to be independent if $P(A ∩ B) = P(A) · P(B)$. This is also called as multiplication rule of probability.