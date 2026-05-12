# 📊 Comprehensive Guide to Probability Distributions

A complete reference guide to major probability distributions including explanations, real-world applications, expectation, variance, characteristic functions, and worked examples.
<br>

A quick summary is provided below. See the PDF for a complete version.

## 📑 Contents

- [Discrete Distributions](#discrete-distributions)
- [Continuous Distributions](#continuous-distributions)
- [Quick Reference Table](#quick-reference-table)

## Discrete Distributions

### 1. Bernoulli Distribution
**Single trial with two outcomes: success (1) or failure (0)**

| Property | Value |
|----------|-------|
| Expectation | p |
| Variance | p(1-p) |
| Characteristic Function | 1 - p + pe^(it) |
| Applications | Coin flip, pass/fail test, click/no-click in advertising |

**Example:** Biased coin with p=0.7 of heads  
**Answer:** E[X]=0.7, Var(X)=0.21

---

### 2. Binomial Distribution
**Number of successes in n independent Bernoulli trials**

| Property | Value |
|----------|-------|
| Expectation | np |
| Variance | np(1-p) |
| Characteristic Function | (1-p + pe^(it))^n |
| Applications | Defective items, number of heads in 10 coin flips |

**Example:** Fair coin flipped 10 times, probability of exactly 6 heads  
**Answer:** P(X=6)=0.2051, E[X]=5, Var(X)=2.5

---

### 3. Geometric Distribution
**Number of trials until the FIRST success**

| Property | Value |
|----------|-------|
| Expectation | 1/p |
| Variance | (1-p)/p² |
| Characteristic Function | pe^(it) / (1 - (1-p)e^(it)) |
| Applications | Job interviews until hired, light bulbs until one fails |

**Example:** Winning probability p=0.2  
**Answer:** E[X]=5 games, Var(X)=20

---

### 4. Negative Binomial (Pascal) Distribution
**Number of trials until r successes occur**

| Property | Value |
|----------|-------|
| Expectation | r/p |
| Variance | r(1-p)/p² |
| Characteristic Function | [pe^(it) / (1 - (1-p)e^(it))]^r |
| Applications | Free throws to make 5 shots, patients to see 3 recoveries |

**Example:** Basketball player with p=0.6, make 3 shots  
**Answer:** E[X]=5 attempts, Var(X)=3.33

---

### 5. Poisson Distribution
**Number of events in a fixed interval with constant average rate λ**

| Property | Value |
|----------|-------|
| Expectation | λ |
| Variance | λ |
| Characteristic Function | e^(λ(e^(it)-1)) |
| Applications | Emails per hour, car accidents per day, radioactive decays |

**Example:** Call center with λ=5 calls/minute  
**Answer:** P(X=3)=0.1404, E[X]=5, Var(X)=5

---

### 6. Hypergeometric Distribution
**Number of successes in n draws WITHOUT replacement from finite population**

| Property | Value |
|----------|-------|
| Expectation | n(K/N) |
| Variance | n(K/N)(1-K/N)((N-n)/(N-1)) |
| Applications | Drawing aces in poker, quality control without replacement |

**Example:** 10 items (4 defective), draw 3 without replacement  
**Answer:** P(X=2)=0.3, E[X]=1.2

---

### 7. Discrete Uniform Distribution
**Finite set of equally likely integer outcomes**

| Property | Value |
|----------|-------|
| Expectation | (a+b)/2 |
| Variance | ((b-a+1)² - 1)/12 |
| Characteristic Function | (e^(ita) - e^(it(b+1))) / ((b-a+1)(1 - e^(it))) |
| Applications | Rolling a fair die, random number generation |

**Example:** Roll a fair six-sided die (a=1, b=6)  
**Answer:** E[X]=3.5, Var(X)=2.917, P(4)=1/6

---

## Continuous Distributions

### 8. Uniform (Rectangular) Distribution
**Constant probability density over [a, b]**

| Property | Value |
|----------|-------|
| Expectation | (a+b)/2 |
| Variance | (b-a)²/12 |
| Characteristic Function | (e^(itb) - e^(ita)) / (it(b-a)) |
| Applications | Random arrival time, quantization error |

**Example:** Bus arrives uniformly between 0-10 minutes  
**Answer:** P(X<3)=0.3, E[X]=5 min, Var(X)=8.33

---

### 9. Normal (Gaussian) Distribution
**Symmetric, bell-shaped curve; central limit theorem basis**

| Property | Value |
|----------|-------|
| Expectation | μ |
| Variance | σ² |
| Characteristic Function | e^(iμt - σ²t²/2) |
| Applications | Heights, test scores, measurement errors |

**Example:** IQ scores with μ=100, σ=15  
**Answer:** P(X>130)=0.0228, 90th percentile=119.22

---

### 10. Exponential Distribution
**Time until next event in a Poisson process (memoryless)**

| Property | Value |
|----------|-------|
| Expectation | 1/λ |
| Variance | 1/λ² |
| Characteristic Function | (1 - it/λ)^(-1) |
| Applications | Waiting time for customers, component lifetime |

**Example:** Customer arrivals with λ=0.5 per minute  
**Answer:** P(X>3)=0.2231, E[X]=2 min, Var(X)=4

---

### 11. Gamma Distribution
**Generalization of exponential; time until k events in Poisson process**

| Property | Value |
|----------|-------|
| Expectation | k/θ |
| Variance | k/θ² |
| Characteristic Function | (1 - iθt)^(-k) |
| Applications | Rainfall totals, insurance claim sizes |

**Example:** Shape k=2, rate θ=3  
**Answer:** E[X]=0.667, Var(X)=0.222

---

### 12. Chi-Squared Distribution
**Sum of squares of k independent standard normals**

| Property | Value |
|----------|-------|
| Expectation | k |
| Variance | 2k |
| Characteristic Function | (1 - 2it)^(-k/2) |
| Applications | Goodness-of-fit test, variance estimation |

**Example:** k=5 degrees of freedom  
**Answer:** E[X]=5, Var(X)=10

---

### 13. Beta Distribution
**Distribution on [0,1] with shape parameters α, β**

| Property | Value |
|----------|-------|
| Expectation | α/(α+β) |
| Variance | αβ / ((α+β)²(α+β+1)) |
| Characteristic Function | ₁F₁(α; α+β; it) |
| Applications | Bayesian prior for binomial proportion, PERT analysis |

**Example:** α=2, β=5  
**Answer:** E[X]=0.2857, Var(X)=0.0255

---

### 14. Log-Normal Distribution
**ln(X) is normal; positive-only, right-skewed**

| Property | Value |
|----------|-------|
| Expectation | e^(μ + σ²/2) |
| Variance | (e^(σ²) - 1)e^(2μ + σ²) |
| Characteristic Function | No simple closed form |
| Applications | Stock prices, income distributions |

**Example:** ln(X) ~ N(μ=1, σ²=0.25)  
**Answer:** E[X]=3.077, Var(X)=2.695

---

### 15. Weibull Distribution
**Flexible lifetime distribution; models varying hazard rates**

| Property | Value |
|----------|-------|
| Expectation | λ Γ(1 + 1/k) |
| Variance | λ²[Γ(1+2/k) - Γ²(1+1/k)] |
| Characteristic Function | No simple closed form |
| Applications | Wind speed, reliability engineering |

**Example:** Scale λ=2, shape k=1.5  
**Answer:** E[X]=1.8054, Var(X)=1.7948

---

### 16. Cauchy Distribution
**Heavy tails; no finite mean or variance**

| Property | Value |
|----------|-------|
| Expectation | Undefined |
| Variance | Infinite |
| Characteristic Function | e^(iμt - γ|t|) |
| Applications | Resonant behavior in physics, ratio of normals |

**Example:** Standard Cauchy (median=0)  
**Answer:** Median=0, IQR=2

---

### 17. Laplace (Double Exponential) Distribution
**Sharper peak than normal, heavier tails**

| Property | Value |
|----------|-------|
| Expectation | μ |
| Variance | 2b² |
| Characteristic Function | e^(iμt) / (1 + b²t²) |
| Applications | Differential privacy, financial returns |

**Example:** μ=0, b=1  
**Answer:** P(|X|<1)=0.6321, E[X]=0, Var(X)=2

---

### 18. Pareto Distribution
**Power-law tail; "80-20 rule"**

| Property | Value |
|----------|-------|
| Expectation | (x_m α)/(α-1) for α>1 |
| Variance | (x_m² α)/((α-1)²(α-2)) for α>2 |
| Characteristic Function | α(x_m it)^α Γ(-α, -ix_m t) |
| Applications | Wealth distribution, city populations |

**Example:** x_m=1, α=3  
**Answer:** E[X]=1.5, Var(X)=0.75

---

## Quick Reference Table

| Distribution | Type | Expectation | Variance |
|--------------|------|-------------|----------|
| Bernoulli | Discrete | p | p(1-p) |
| Binomial | Discrete | np | np(1-p) |
| Geometric | Discrete | 1/p | (1-p)/p² |
| Neg. Binomial | Discrete | r/p | r(1-p)/p² |
| Poisson | Discrete | λ | λ |
| Hypergeometric | Discrete | nK/N | n(K/N)(1-K/N)((N-n)/(N-1)) |
| Discrete Uniform | Discrete | (a+b)/2 | ((b-a+1)²-1)/12 |
| Uniform (cont.) | Continuous | (a+b)/2 | (b-a)²/12 |
| Normal | Continuous | μ | σ² |
| Exponential | Continuous | 1/λ | 1/λ² |
| Gamma | Continuous | k/θ | k/θ² |
| Chi-Squared | Continuous | k | 2k |
| Beta | Continuous | α/(α+β) | αβ/((α+β)²(α+β+1)) |
| Log-Normal | Continuous | e^(μ+σ²/2) | (e^(σ²)-1)e^(2μ+σ²) |
| Weibull | Continuous | λΓ(1+1/k) | λ²[Γ(1+2/k)-Γ²(1+1/k)] |
| Cauchy | Continuous | Undefined | Infinite |
| Laplace | Continuous | μ | 2b² |
| Pareto | Continuous | (x_m α)/(α-1) | (x_m² α)/((α-1)²(α-2)) |

---

## 📄 PDF Version

A professionally formatted PDF version is available in this repository as `probability_distributions_guide.pdf`.

## 📝 License

MIT License

---

**Created for the statistics and data science community**
