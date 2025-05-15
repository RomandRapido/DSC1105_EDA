# Decision Analysis Problem: Step-by-Step Solution

**Given Information:**
Payoff Table (in dollars):
| Alternative | State S1 | State S2 |
|-------------|----------|----------|
| A1          | 400      | -100     |
| A2          | 0        | 100      |

Prior Probabilities:
$P(S1) = 0.4$
$P(S2) = 0.6$

Research Information:
Cost of research = $100
Let P1 = Research predicts S1, P2 = Research predicts S2.

$P(P1|S1) = 0.60$ (accurately predicts S1)

$P(P2|S1) = 0.40$ (inaccurately predicts S2 when S1 is true)

$P(P2|S2) = 0.80$ (accurately predicts S2)

$P(P1|S2) = 0.20$ (inaccurately predicts S1 when S2 is true)

---

## (a) Given that the research is not done, use Bayes' decision rule to determine which decision alternative should be chosen.

Bayes' decision rule (or Expected Monetary Value criterion) suggests choosing the alternative with the highest expected payoff.

Expected Payoff for A1 (EP(A1)):
$$EP(A1) = \text{Payoff}(A1,S1) \cdot P(S1) + \text{Payoff}(A1,S2) \cdot P(S2)$$
$$EP(A1) = (400 \cdot 0.4) + (-100 \cdot 0.6)$$
$$EP(A1) = 160 - 60 = \$100$$

Expected Payoff for A2 (EP(A2)):
$$EP(A2) = \text{Payoff}(A2,S1) \cdot P(S1) + \text{Payoff}(A2,S2) \cdot P(S2)$$
$$EP(A2) = (0 \cdot 0.4) + (100 \cdot 0.6)$$
$$EP(A2) = 0 + 60 = \$60$$

Comparing the expected payoffs:
$EP(A1) = \$100$
$EP(A2) = \$60$
Since $EP(A1) > EP(A2)$, the decision alternative that should be chosen is **A1**.

The maximum expected payoff without research (EVWOI - Expected Value Without Information) is $\$100$.

---

## (b) Find EVPI. Does this answer indicate that it might be worthwhile to do the research?

Expected Value with Perfect Information (EVwPI):
If we knew S1 would occur, we would choose A1 (payoff 400).

If we knew S2 would occur, we would choose A2 (payoff 100).

$$\text{EVwPI} = (\text{Max Payoff for S1} \cdot P(S1)) + (\text{Max Payoff for S2} \cdot P(S2))$$
$$\text{EVwPI} = (400 \cdot 0.4) + (100 \cdot 0.6)$$
$$\text{EVwPI} = 160 + 60 = \$220$$

Expected Value of Perfect Information (EVPI):
$$\text{EVPI} = \text{EVwPI} - \text{Max EP (without information)}$$
$$\text{EVPI} = \$220 - \$100 \text{ (from part a)}$$
$$\text{EVPI} = \$120$$

The cost of the research is $\$100$. Since EVPI ($\$120$) is greater than the cost of the research ($\$100$), this indicates that perfect information would be worth $\$120$. As the proposed research is imperfect, its value will be less than $\$120$, but since $\$120 > \$100$, it suggests that **it might be worthwhile to do the research**. Further analysis (EVSI) is needed to confirm this.

---

## (c) Given that the research is done, find the joint probability of each of the following pairs of outcomes:

(i) The state of nature is S1 and the research predicts S1 $(P(S1 \cap P1))$:
$$P(S1 \cap P1) = P(P1|S1) \cdot P(S1) = 0.60 \cdot 0.4 = \mathbf{0.24}$$

(ii) The state of nature is S1 and the research predicts S2 $(P(S1 \cap P2))$:
$$P(S1 \cap P2) = P(P2|S1) \cdot P(S1) = 0.40 \cdot 0.4 = \mathbf{0.16}$$

(iii) The state of nature is S2 and the research predicts S1 $(P(S2 \cap P1))$:
$$P(S2 \cap P1) = P(P1|S2) \cdot P(S2) = 0.20 \cdot 0.6 = \mathbf{0.12}$$

(iv) The state of nature is S2 and the research predicts S2 $(P(S2 \cap P2))$:
$$P(S2 \cap P2) = P(P2|S2) \cdot P(S2) = 0.80 \cdot 0.6 = \mathbf{0.48}$$

(Check: Sum of joint probabilities = $0.24 + 0.16 + 0.12 + 0.48 = 1.00$)

---

## (d) Find the unconditional probability that the research predicts S1. Also find the unconditional probability that the research predicts S2.

Unconditional probability that the research predicts S1 $(P(P1))$:
$$P(P1) = P(S1 \cap P1) + P(S2 \cap P1)$$
$$P(P1) = 0.24 + 0.12 = \mathbf{0.36}$$

Unconditional probability that the research predicts S2 $(P(P2))$:
$$P(P2) = P(S1 \cap P2) + P(S2 \cap P2)$$
$$P(P2) = 0.16 + 0.48 = \mathbf{0.64}$$

(Check: $P(P1) + P(P2) = 0.36 + 0.64 = 1.00$)

---

## (e) Given that the research is done, use your answers in parts (c) and (d) to determine the posterior probabilities of the states of nature for each of the two possible predictions of the research.

Case 1: Research predicts S1 (P1)
$$P(S1|P1) = \frac{P(S1 \cap P1)}{P(P1)} = \frac{0.24}{0.36} = \frac{24}{36} = \mathbf{\frac{2}{3}} \text{ (or approx. 0.6667)}$$
$$P(S2|P1) = \frac{P(S2 \cap P1)}{P(P1)} = \frac{0.12}{0.36} = \frac{12}{36} = \mathbf{\frac{1}{3}} \text{ (or approx. 0.3333)}$$
(Check: $P(S1|P1) + P(S2|P1) = \frac{2}{3} + \frac{1}{3} = 1$)

Case 2: Research predicts S2 (P2)
$$P(S1|P2) = \frac{P(S1 \cap P2)}{P(P2)} = \frac{0.16}{0.64} = \frac{16}{64} = \mathbf{\frac{1}{4}} \text{ (or 0.25)}$$
$$P(S2|P2) = \frac{P(S2 \cap P2)}{P(P2)} = \frac{0.48}{0.64} = \frac{48}{64} = \mathbf{\frac{3}{4}} \text{ (or 0.75)}$$
(Check: $P(S1|P2) + P(S2|P2) = \frac{1}{4} + \frac{3}{4} = 1$)

---

## (f) Given that the research predicts S1, use Bayes' decision rule to determine which decision alternative should be chosen and the resulting expected payoff.

If research predicts S1, we use the posterior probabilities $P(S1|P1) = \frac{2}{3}$ and $P(S2|P1) = \frac{1}{3}$.

$$EP(A1 | P1) = \text{Payoff}(A1,S1) \cdot P(S1|P1) + \text{Payoff}(A1,S2) \cdot P(S2|P1)$$
$$EP(A1 | P1) = (400 \cdot \frac{2}{3}) + (-100 \cdot \frac{1}{3}) = \frac{800}{3} - \frac{100}{3} = \frac{700}{3} \approx \$233.33$$

$$EP(A2 | P1) = \text{Payoff}(A2,S1) \cdot P(S1|P1) + \text{Payoff}(A2,S2) \cdot P(S2|P1)$$
$$EP(A2 | P1) = (0 \cdot \frac{2}{3}) + (100 \cdot \frac{1}{3}) = 0 + \frac{100}{3} = \frac{100}{3} \approx \$33.33$$

Comparing $EP(A1|P1)$ and $EP(A2|P1)$: $\$233.33 > \$33.33$.
The decision alternative chosen is **A1**.
The resulting expected payoff given the research predicts S1 is $\mathbf{\frac{700}{3}}$ (or approximately $\$233.33$).

---

## (g) Repeat part (f) when the research predicts S2.

If research predicts S2, we use the posterior probabilities $P(S1|P2) = \frac{1}{4}$ and $P(S2|P2) = \frac{3}{4}$.

$$EP(A1 | P2) = \text{Payoff}(A1,S1) \cdot P(S1|P2) + \text{Payoff}(A1,S2) \cdot P(S2|P2)$$
$$EP(A1 | P2) = (400 \cdot \frac{1}{4}) + (-100 \cdot \frac{3}{4}) = 100 - 75 = \$25$$

$$EP(A2 | P2) = \text{Payoff}(A2,S1) \cdot P(S1|P2) + \text{Payoff}(A2,S2) \cdot P(S2|P2)$$
$$EP(A2 | P2) = (0 \cdot \frac{1}{4}) + (100 \cdot \frac{3}{4}) = 0 + 75 = \$75$$

Comparing $EP(A1|P2)$ and $EP(A2|P2)$: $\$25 < \$75$.
The decision alternative chosen is **A2**.
The resulting expected payoff given the research predicts S2 is $\mathbf{\$75}$.

---

## (h) Given that research is done, what is the expected payoff when using Bayes' decision rule?

This is the Expected Value With Sample Information (EVWSI) or Expected Payoff With Sample Information (EPWSI). It is calculated before deducting the cost of research.
$$\text{EVWSI} = (\text{Max EP | P1}) \cdot P(P1) + (\text{Max EP | P2}) \cdot P(P2)$$
$$\text{EVWSI} = (\frac{700}{3} \cdot 0.36) + (75 \cdot 0.64)$$
$$\text{EVWSI} = (\frac{700}{3} \cdot \frac{36}{100}) + (75 \cdot \frac{64}{100})$$
$$\text{EVWSI} = (\frac{700 \cdot 12}{100}) + (\frac{4800}{100})$$
$$\text{EVWSI} = \frac{8400}{100} + \frac{4800}{100}$$
$$\text{EVWSI} = 84 + 48 = \mathbf{\$132}$$

---

## (i) Use the preceding results to determine the optimal policy regarding whether to do the research and the choice of the decision alternative.

To determine the optimal policy, we compare the expected payoff if research is done (net of cost) with the expected payoff if research is not done.

1.  **Expected Payoff if Research is NOT done (EVWOI):**
    From part (a), the maximum expected payoff without research is $\$100$ (by choosing A1).

2.  **Expected Payoff if Research IS done (net of cost):**
    The gross expected payoff if research is done (EVWSI) is $\$132$ (from part h).
    Cost of research = $\$100$.
    Net Expected Payoff if research is done = EVWSI - Cost of Research
    Net Expected Payoff if research is done = $\$132 - \$100 = \$32$.

Alternatively, we can calculate the Expected Value of Sample Information (EVSI):
$$\text{EVSI} = \text{EVWSI} - \text{EVWOI}$$
$$\text{EVSI} = \$132 - \$100 = \$32$$
Since EVSI ($\$32$) is less than the Cost of Research ($\$100$), the research is not economically worthwhile.

**Comparing the net payoffs:**
-   Expected Payoff (Not Do Research) = $\$100$
-   Expected Payoff (Do Research, net of cost) = $\$32$

Since $\$100 > \$32$, the optimal decision is to **not do the research**.

**Optimal Policy:**
1.  **Regarding whether to do the research:** The optimal policy is **not to do the research**.
2.  **Choice of the decision alternative:** Since the research is not done, we refer to the decision made in part (a). The optimal decision alternative is **A1**.

The overall expected payoff of this optimal policy is $\$100$.