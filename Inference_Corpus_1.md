
# **Confidence Intervals, Estimation, and Hypothesis Testing**  
*A consolidated and structured set of lecture notes*

---

## **1. Margin of Error and Estimation**

### **1.1 Margin of Error**
The **margin of error** reflects the uncertainty around a point estimate. It is computed as:

\[
\text{Margin of Error} = \text{Quantile} \times \text{Standard Error}
\]

- A wider interval indicates greater uncertainty.  
- The only practical way to reduce the margin of error is to **increase sample size**.

---

## **2. Estimating a Proportion**

### **2.1 Point Estimate Example**
A survey of 160 programmers found that 56 use Python as their primary language.

\[
\hat{p} = \frac{56}{160} = 0.35 = 35\%
\]

### **2.2 Confidence Interval for a Proportion**

**Step 1: Quantile**  
- 95% confidence → \( Z = 1.96 \) (sample size > 30)

**Step 2: Standard Error**

\[
SE(\hat{p}) = \sqrt{\frac{35 \times 65}{160}} = 3.77\%
\]

**Step 3: Interval**

\[
35\% \pm (1.96 \times 3.77\%) = (27.6\%, 42.4\%)
\]

---

## **3. The Student’s t‑Distribution**

Used when:
- Sample size \( n \leq 30 \)
- Population standard deviation \( \sigma \) is **unknown**

Key properties:
- Accounts for extra uncertainty in small samples  
- Degrees of freedom: \( df = n - 1 \)  
- Approaches the Z‑distribution as \( n \to \infty \)

> In large samples, using \( df = \infty \) (Z‑distribution) yields nearly identical results.

---

## **4. Confidence Intervals for Means**

### **4.1 General Form**
\[
\bar{x} \pm t_{\alpha/2, df} \cdot \frac{s}{\sqrt{n}}
\]

### **4.2 Worked Example**
Mercury measurements (ng/ml):  
23.3, 22.5, 21.9, 21.5, 19.9, 21.3, 21.7, 23.8, 22.6, 24.7

To compute a **99% CI**:
1. Compute \( \bar{x} \) and \( s \)  
2. Use \( df = 9 \) and the 99% t‑quantile  
3. Apply the formula above

---

## **5. Hypothesis Testing: Core Framework**

Hypothesis testing evaluates evidence against a null hypothesis \( H_0 \) in favour of an alternative \( H_1 \).

> “The process by which we use data to answer questions about parameters is very similar to how juries evaluate evidence about a defendant.” – Geoffrey Vining (1998)

### **5.1 The Four Steps**

1. **State the Hypotheses**  
   - \( H_0 \): status quo  
   - \( H_1 \): new claim or difference  

2. **Compute the Test Statistic**  
   - Use Z or t depending on sample size and known/unknown variance  

3. **Determine the Critical Value**  
   Depends on:  
   - Sample size → degrees of freedom  
   - Significance level \( \alpha \)  
   - One‑tailed vs two‑tailed test  

4. **Decision Rule**  
   - Reject \( H_0 \) if \( | \text{test statistic} | \) exceeds the critical value  

---

## **6. One‑Tailed vs Two‑Tailed Tests**

- **One‑tailed**: directional alternative (greater/less)  
- **Two‑tailed**: non‑directional (“not equal to”)  
- Two‑tailed tests are more common in standard procedures  

---

## **7. Hypothesis Testing for Proportions**

Covers:
- Confidence intervals for a proportion  
- One‑sample proportion tests  
- Two‑sample proportion tests  
- Margin of error estimation for proportions  

(Your earlier example fits directly into this framework.)

---

## **8. Comparing Two Populations**

### **8.1 Independent Samples**
Two samples are independent if selecting one does not influence the other.

Notation:  
- Means: \( \mu_1, \mu_2 \)  
- SDs: \( \sigma_1, \sigma_2 \)  
- Sample sizes: \( n_1, n_2 \)  
- Sample means: \( \bar{x}_1, \bar{x}_2 \)  
- Sample SDs: \( s_1, s_2 \)

### **8.2 Standard Error of the Difference**
\[
SE(\bar{x}_1 - \bar{x}_2) = \sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}
\]

### **8.3 Example (Known Variances)**
Male height: 69 in, \( \sigma = 2.5 \)  
Female height: 65 in, \( \sigma = 2.5 \)  
\( n_1 = n_2 = 50 \)

Use the Z‑test for difference in means:

\[
Z = \frac{(\bar{x}_1 - \bar{x}_2) - (\mu_1 - \mu_2)}{\sqrt{\frac{\sigma_1^2}{n_1} + \frac{\sigma_2^2}{n_2}}}
\]

---

## **9. F‑Test for Equality of Variances**

\[
F = \frac{S_X^2}{S_Y^2}
\]

- Tests \( H_0 \): variances are equal  
- Compare to F‑distribution critical values with \( n_1 - 1 \) and \( n_2 - 1 \) df  

---

## **10. Statistical Significance**

- Significance level \( \alpha \) is the probability of a **Type I error**  
- Typical values: 0.05 (95% confidence), 0.01 (99% confidence)  
- A result is **statistically significant** if \( p \leq \alpha \)

Example:  
If \( t = 0.03 \) and \( p < 0.05 \), reject \( H_0 \) and conclude a difference exists.

> “Significant” in statistics does **not** mean “important”.

---

## **11. Fractional Factorial Designs (Summary)**

Used to study multiple factors with fewer runs than a full factorial.

### **Key Terms**
- **Generator**: defines how the fraction is constructed  
- **Defining relation**: lists confounded effects  
- **Confounding**: when effects cannot be distinguished  
- **Resolution**: smallest order of interaction confounded with a main effect  

### **Resolution V**
- Main effects unconfounded with two‑factor interactions  
- Two‑factor interactions may be confounded with each other  
- Often preferred for screening experiments  

---
