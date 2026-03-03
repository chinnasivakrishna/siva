# 📅 DAY 3 - MORNING SESSION
# 🎯 UNIT II & V ESSENTIALS (Strategic Coverage)

---

## UNIT II: SAMPLING & ESTIMATION - KEY FORMULAS ONLY

### Section 2.1: Must-Know Formulas

**CENTRAL LIMIT THEOREM:**
```
For large n (≥30), sampling distribution of x̄ is approximately normal:
x̄ ~ N(μ, σ²/n)

Standard Error: SE = σ/√n
```

**CONFIDENCE INTERVALS (MEMORIZE):**
```
95% CI for μ: x̄ ± 1.96(σ/√n)
99% CI for μ: x̄ ± 2.58(σ/√n)

For proportion:
95% CI for p: p̂ ± 1.96√[p̂(1−p̂)/n]
```

**GROUPED DATA:**
```
Mean: x̄ = Σfᵢxᵢ / N  (where xᵢ = class midpoint)
Variance: σ² = Σfᵢ(xᵢ−x̄)² / N
Standard Deviation: σ = √σ²
```

---

### Section 2.2: One Complete Problem (Memorize Solution Pattern)

**📝 STANDARD CI PROBLEM:**

**Problem:** A sample of 100 students has mean score 67 with SD 15. Find 95% and 99% CI for population mean.

**SOLUTION:**

```
Given: n=100, x̄=67, σ=15

95% CI:
x̄ ± 1.96(σ/√n) = 67 ± 1.96(15/10)
                 = 67 ± 1.96(1.5)
                 = 67 ± 2.94
                 = (64.06, 69.94)

99% CI:
x̄ ± 2.58(σ/√n) = 67 ± 2.58(1.5)
                 = 67 ± 3.87
                 = (63.13, 70.87)

Interpretation: We are 95% confident the true mean lies between 64.06 and 69.94.
```

**THIS PROBLEM TYPE APPEARS IN ALMOST EVERY EXAM**

---

### Section 2.3: Theory Points (For (a) parts)

**When asked "Explain Sampling Distribution":**

```
WRITE:
1. Population has parameters μ, σ
2. Draw samples of size n
3. Calculate x̄ for each sample
4. Distribution of all possible x̄ values = sampling distribution
5. Properties:
   - E(x̄) = μ
   - Var(x̄) = σ²/n
   - SE = σ/√n
6. Central Limit Theorem: For large n, x̄ ~ N(μ, σ²/n)
```

**When asked "Point vs Interval Estimation":**

```
WRITE:
Point Estimation:
- Single value estimate (e.g., x̄ = 50)
- No measure of reliability

Interval Estimation:
- Range of values (e.g., 45 to 55)
- Includes confidence level
- More informative

Example: "μ is between 64 and 70 with 95% confidence"
```

**When asked "Unbiased and Efficient Estimates":**

```
WRITE:
Unbiased Estimator:
- E(θ̂) = θ
- Sample mean x̄ is unbiased for μ
- s² = Σ(xᵢ−x̄)²/(n−1) is unbiased for σ²

Efficient Estimator:
- Has minimum variance among all unbiased estimators
- Called MVUE (Minimum Variance Unbiased Estimator)
- x̄ is efficient for μ
```

---

## UNIT V: GRAPH THEORY - KEY CONCEPTS ONLY

### Section 5.1: Essential Definitions

**BASIC TERMS:**
```
Graph G = (V, E)
V = set of vertices
E = set of edges

Degree of vertex: number of edges incident to it

Path: sequence of vertices connected by edges
Circuit/Cycle: path that starts and ends at same vertex

Connected: path exists between any two vertices
```

**MATRIX REPRESENTATIONS:**

**Adjacency Matrix:**
```
A[i][j] = 1 if edge (i,j) exists
        = 0 otherwise

For undirected graph: symmetric matrix
Sum of row i = degree of vertex i
```

**Incidence Matrix:**
```
M[i][j] = 1 if vertex i is incident to edge j
        = 0 otherwise
```

---

### Section 5.2: Eulerian vs Hamiltonian (Most Asked)

**COMPARISON TABLE (MEMORIZE):**

```
┌──────────────┬─────────────────┬─────────────────────┐
│   Property   │    EULERIAN     │    HAMILTONIAN      │
├──────────────┼─────────────────┼─────────────────────┤
│ Traverses    │ All EDGES       │ All VERTICES        │
│              │ exactly once    │ exactly once        │
├──────────────┼─────────────────┼─────────────────────┤
│ Circuit      │ All vertices    │ All vertices        │
│ Condition    │ have EVEN       │ deg(v) ≥ n/2        │
│              │ degree          │ (Dirac - sufficient)│
├──────────────┼─────────────────┼─────────────────────┤
│ Path         │ Exactly 2       │ No simple           │
│ Condition    │ vertices with   │ necessary &         │
│              │ odd degree      │ sufficient cond.    │
├──────────────┼─────────────────┼─────────────────────┤
│ Complexity   │ Easy (O(E))     │ Hard (NP-complete)  │
│              │ Polynomial      │                     │
└──────────────┴─────────────────┴─────────────────────┘
```

**EXAMPLES:**
```
Complete graph K₅:
- All vertices degree 4 (even) → Eulerian ✓
- All vertices degree 4 ≥ 5/2 → Hamiltonian ✓

Cycle C₆ (hexagon):
- All vertices degree 2 (even) → Eulerian ✓
- Forms a cycle → Hamiltonian ✓

Complete bipartite K₃,₃:
- All vertices degree 3 (odd) → NOT Eulerian ✗
- Bipartite with parts of size 3 → Hamiltonian ✓
```

---

### Section 5.3: Planar Graphs & Euler's Formula

**EULER'S FORMULA (MEMORIZE):**
```
V − E + F = 2

V = number of vertices
E = number of edges
F = number of faces (including outer face)

Valid for connected planar graphs
```

**BOUNDS FOR PLANAR GRAPHS:**
```
E ≤ 3V − 6  (for V ≥ 3)
```

**HOW TO USE FOR NON-PLANARITY:**

If E > 3V−6 → Graph is NOT planar

**Example: K₅**
```
V = 5
E = 10
Check: 3V−6 = 3(5)−6 = 9
Since 10 > 9 → K₅ is NOT planar ✓
```

**KURATOWSKI'S THEOREM:**
Graph is planar ⟺ it contains no subdivision of K₅ or K₃,₃

---

### Section 5.4: Graph Coloring

**KEY FACTS:**
```
Chromatic Number χ(G) = minimum colors needed

FORMULAS:
χ(Kₙ) = n           [complete graph needs n colors]
χ(bipartite) = 2    [2 colors always suffice]
χ(Cₙ) = 2  (n even) [even cycle]
χ(Cₙ) = 3  (n odd)  [odd cycle]
χ(planar) ≤ 4       [Four Color Theorem]
```

**FOUR COLOR THEOREM:**
Any planar graph can be colored with at most 4 colors.

---

### Section 5.5: Spanning Trees & MST Algorithms

**SPANNING TREE:**
- Subgraph that is a tree
- Includes all vertices
- Has exactly n−1 edges (for n vertices)

**KRUSKAL'S ALGORITHM (Greedy - by edge):**
```
1. Sort all edges by weight (ascending)
2. Pick smallest edge that doesn't form cycle
3. Repeat until n−1 edges selected
```

**PRIM'S ALGORITHM (Greedy - by vertex):**
```
1. Start with any vertex
2. Add minimum weight edge connecting tree to new vertex
3. Repeat until all vertices included
```

**📝 STANDARD MST PROBLEM:**

**Graph with edges:**
```
AB=2, AC=3, AD=4
BC=1, BD=5
CD=3
```

**Kruskal's picks in order:** BC(1) → AB(2) → AC(3) or CD(3) → Total = 6

**Prim's from A:** AB(2) → BC(1) → CD(3) → Total = 6

Same result (MST is unique if all edge weights distinct)

---

## 📝 QUICK ANSWER FORMATS FOR DAY 3

### Format for Unit II Question:

**Q: Explain sampling distribution and CLT [8M]**

**Answer:**
```
Sampling Distribution:
- Consider population with mean μ, SD σ
- Draw samples of size n repeatedly
- Calculate x̄ for each sample
- Distribution of x̄ values = sampling distribution

Properties:
E(x̄) = μ
Var(x̄) = σ²/n
SE = σ/√n

Central Limit Theorem:
For sufficiently large n (usually n≥30):
x̄ ~ N(μ, σ²/n)

This holds regardless of population distribution shape.

Applications:
- Makes inference possible
- Justifies use of normal distribution
- Foundation for confidence intervals
```

---

### Format for Unit V Question:

**Q: Define Eulerian graph. State conditions [8M]**

**Answer:**
```
Eulerian Graph:
A graph that contains an Eulerian circuit.

Eulerian Circuit:
A circuit that visits every EDGE exactly once and returns to starting vertex.

Necessary and Sufficient Condition:
A connected graph has an Eulerian circuit if and only if 
EVERY vertex has EVEN degree.

Eulerian Path (not circuit):
Exists if exactly TWO vertices have odd degree.
Path starts at one odd-degree vertex and ends at the other.

Example:
    1 — 2
    |   |
    3 — 4

Degrees: All vertices have degree 2 (even)
∴ Eulerian circuit exists ✓
One circuit: 1-2-4-3-1

Counter-example:
    1 — 2 — 3
        |
        4

Degrees: 1(1), 2(3), 3(1), 4(1) — three odd
∴ No Eulerian circuit or path
```

---

---

# 📅 DAY 3 - AFTERNOON SESSION
# 🎯 MOCK PAPERS WITH COMPLETE SOLUTIONS

---

# 📄 MOCK PAPER 1

**Code: MFCS | M.Tech I Semester**
**Time: 3 Hours | Max Marks: 75**
**Answer any FIVE questions, ONE from each Unit**

---

## UNIT-I

**1.** (a) State and prove the Addition Theorem of Probability. Extend to three events. [8M]
      (b) In a class, 70% study Math, 60% study Physics, 40% study both. A student is selected randomly. Find probability that:
          (i) Studies at least one subject
          (ii) Studies exactly one subject
          (iii) Studies neither subject [7M]

**OR**

**2.** (a) Define Random Variable. Distinguish between discrete and continuous random variables. Explain CDF and its properties. [8M]
      (b) A fair coin is tossed 4 times. Let X = number of heads. Find:
          (i) Probability distribution of X
          (ii) E(X) and Var(X)
          (iii) P(X ≥ 2) [7M]

---

## UNIT-II

**3.** (a) Explain the concept of Sampling Distribution. State and explain the Central Limit Theorem with its significance. [8M]
      (b) Calculate mean, variance, and standard deviation for the following grouped data: [7M]

| Class Interval | 0-10 | 10-20 | 20-30 | 30-40 | 40-50 |
|----------------|------|-------|-------|-------|-------|
| Frequency | 5 | 8 | 12 | 10 | 5 |

**OR**

**4.** (a) Define Point and Interval Estimation. Explain Unbiased, Efficient, and Consistent estimators. [8M]
      (b) A random sample of 64 students has mean score 72 with SD 16. Find:
          (i) 95% confidence interval for population mean
          (ii) 99% confidence interval for population mean [7M]

---

## UNIT-III

**5.** (a) Explain the step-by-step procedure for testing of hypothesis. Describe Type I and Type II errors with examples. [8M]
      (b) Distinguish between one-tailed and two-tailed tests. Explain p-value and its role in hypothesis testing. [7M]

**OR**

**6.** A die is rolled 60 times with the following results: [15M]

| Face | 1 | 2 | 3 | 4 | 5 | 6 |
|------|---|---|---|---|---|---|
| Observed | 7 | 11 | 9 | 13 | 10 | 10 |

Test at 5% significance level whether the die is fair. Also find the p-value.

---

## UNIT-IV

**7.** (a) Define Semigroup, Monoid, Group, and Abelian Group. Give one example of each and verify the properties. [8M]
      (b) Define Group Homomorphism and Isomorphism. Prove that if f: G→G' is a homomorphism, then f(e)=e' and f(a⁻¹)=[f(a)]⁻¹. [7M]

**OR**

**8.** (a) State and prove Fermat's Little Theorem. Use it to find:
          (i) 5¹² (mod 13)
          (ii) 2⁵⁰ (mod 11) [8M]
      (b) Explain the Euclidean Algorithm. Use it to find gcd(270, 192). Also find lcm(270, 192). [7M]

---

## UNIT-V

**9.** (a) Define Eulerian and Hamiltonian graphs. State the necessary and sufficient conditions for each with examples. [8M]
      (b) Define Planar Graph. State and prove Euler's formula V−E+F=2. Show that K₅ is non-planar. [7M]

**OR**

**10.** (a) Define Spanning Tree. Explain Kruskal's and Prim's algorithms for finding Minimum Spanning Tree. [8M]
       (b) Explain Graph Coloring and Chromatic Number. State the Four Color Theorem. Find χ(K₅) and χ(K₃,₃). [7M]

---

---

# ✅ MOCK PAPER 1 - COMPLETE SOLUTIONS

---

## SOLUTION 1(a): Addition Theorem [8M]

**ANSWER:**

**Axioms of Probability:**
1. P(A) ≥ 0 for any event A
2. P(S) = 1 where S is sample space
3. For mutually exclusive events A and B: P(A∪B) = P(A) + P(B)

**Addition Theorem for Two Events:**

**Statement:** For any two events A and B:
```
P(A∪B) = P(A) + P(B) − P(A∩B)
```

**Proof:**
Event A∪B can be partitioned into three disjoint parts:
- Part 1: A∩B' (only A)
- Part 2: A'∩B (only B)
- Part 3: A∩B (both)

By Axiom 3:
```
P(A∪B) = P(A∩B') + P(A'∩B) + P(A∩B)

Also:
P(A) = P(A∩B') + P(A∩B)
P(B) = P(A'∩B) + P(A∩B)

Therefore:
P(A) + P(B) = P(A∩B') + P(A'∩B) + 2P(A∩B)
            = P(A∪B) + P(A∩B)

∴ P(A∪B) = P(A) + P(B) − P(A∩B) ✓
```

**Venn Diagram:** [Draw three overlapping regions]

**Extension to Three Events:**
```
P(A∪B∪C) = P(A) + P(B) + P(C)
          − P(A∩B) − P(B∩C) − P(A∩C)
          + P(A∩B∩C)
```

**[8 marks awarded for: axioms(1), theorem statement(1), proof(4), diagram(1), three-event formula(1)]**

---

## SOLUTION 1(b): Application [7M]

**ANSWER:**

**Given:**
- P(M) = 0.70 (Math)
- P(P) = 0.60 (Physics)
- P(M∩P) = 0.40 (both)

**(i) At least one subject:**
```
P(M∪P) = P(M) + P(P) − P(M∩P)
       = 0.70 + 0.60 − 0.40
       = 0.90

Answer: 0.90 or 90% ✓
```

**(ii) Exactly one subject:**
```
P(only M) = P(M) − P(M∩P) = 0.70 − 0.40 = 0.30
P(only P) = P(P) − P(M∩P) = 0.60 − 0.40 = 0.20

P(exactly one) = 0.30 + 0.20 = 0.50

Answer: 0.50 or 50% ✓
```

**(iii) Neither subject:**
```
P(neither) = P((M∪P)')
          = 1 − P(M∪P)
          = 1 − 0.90
          = 0.10

Answer: 0.10 or 10% ✓
```

**[7 marks: setup(1), part (i)(2), part (ii)(2), part (iii)(2)]**

---

## SOLUTION 2(b): Random Variable [7M]

**ANSWER:**

**Sample Space for 4 tosses:** 2⁴ = 16 outcomes

**(i) Probability Distribution:**

Count outcomes for each value of X:

| X | Outcomes | Count | P(X) |
|---|----------|-------|------|
| 0 | TTTT | 1 | 1/16 |
| 1 | HTTT, THTT, TTHT, TTTH | 4 | 4/16 |
| 2 | HHTT, HTHT, HTTH, THHT, THTH, TTHH | 6 | 6/16 |
| 3 | HHHT, HHTH, HTHH, THHH | 4 | 4/16 |
| 4 | HHHH | 1 | 1/16 |

**Verification:** 1+4+6+4+1 = 16/16 = 1 ✓

**(ii) Expected Value:**
```
E(X) = Σ xᵢP(xᵢ)
     = 0(1/16) + 1(4/16) + 2(6/16) + 3(4/16) + 4(1/16)
     = 0 + 4/16 + 12/16 + 12/16 + 4/16
     = 32/16
     = 2 ✓

E(X²) = 0²(1/16) + 1²(4/16) + 2²(6/16) + 3²(4/16) + 4²(1/16)
      = 0 + 4/16 + 24/16 + 36/16 + 16/16
      = 80/16
      = 5

Var(X) = E(X²) − [E(X)]²
       = 5 − 4
       = 1 ✓
```

**(iii) P(X ≥ 2):**
```
P(X ≥ 2) = P(X=2) + P(X=3) + P(X=4)
         = 6/16 + 4/16 + 1/16
         = 11/16 ✓
```

**[7 marks: distribution(3), E(X)(2), Var(X)(1), probability(1)]**

---

## SOLUTION 3(b): Grouped Data [7M]

**ANSWER:**

| CI | Midpoint xᵢ | fᵢ | fᵢxᵢ | xᵢ−x̄ | (xᵢ−x̄)² | fᵢ(xᵢ−x̄)² |
|----|-------------|----|----|------|---------|-----------|
| 0-10 | 5 | 5 | 25 | −20 | 400 | 2000 |
| 10-20 | 15 | 8 | 120 | −10 | 100 | 800 |
| 20-30 | 25 | 12 | 300 | 0 | 0 | 0 |
| 30-40 | 35 | 10 | 350 | 10 | 100 | 1000 |
| 40-50 | 45 | 5 | 225 | 20 | 400 | 2000 |
| **Total** | | **40** | **1020** | | | **5800** |

**Mean:**
```
x̄ = Σfᵢxᵢ / N = 1020 / 40 = 25.5 ✓
```

**Variance:**
```
σ² = Σfᵢ(xᵢ−x̄)² / N = 5800 / 40 = 145 ✓
```

**Standard Deviation:**
```
σ = √145 = 12.04 ✓
```

**[7 marks: table setup(2), mean(2), variance(2), SD(1)]**

---

## SOLUTION 4(b): Confidence Intervals [7M]

**ANSWER:**

**Given:** n=64, x̄=72, s=16

**(i) 95% Confidence Interval:**
```
Formula: x̄ ± 1.96(σ/√n)

SE = s/√n = 16/√64 = 16/8 = 2

Margin of Error = 1.96 × 2 = 3.92

95% CI = 72 ± 3.92
       = (68.08, 75.92) ✓
```

**(ii) 99% Confidence Interval:**
```
Formula: x̄ ± 2.58(σ/√n)

Margin of Error = 2.58 × 2 = 5.16

99% CI = 72 ± 5.16
       = (66.84, 77.16) ✓
```

**Interpretation:**
We are 95% confident that the true population mean score lies between 68.08 and 75.92.
We are 99% confident it lies between 66.84 and 77.16.

Note: 99% CI is wider, reflecting higher confidence requires larger interval.

**[7 marks: setup(1), 95% CI(3), 99% CI(2), interpretation(1)]**

---

## SOLUTION 6: Chi-Square Goodness of Fit [15M]

**ANSWER:**

**Step 1: State Hypotheses**
```
H₀: The die is fair (all faces equally likely)
H₁: The die is not fair
```

**Step 2: Significance Level**
```
α = 0.05 (5%)
```

**Step 3: Expected Frequencies**
For a fair die, each face has probability 1/6.
```
E = n × p = 60 × (1/6) = 10 for each face
```

**Step 4: Compute Chi-Square Statistic**

| Face | Observed (O) | Expected (E) | O−E | (O−E)² | (O−E)²/E |
|------|-------------|--------------|-----|--------|----------|
| 1 | 7 | 10 | −3 | 9 | 0.90 |
| 2 | 11 | 10 | 1 | 1 | 0.10 |
| 3 | 9 | 10 | −1 | 1 | 0.10 |
| 4 | 13 | 10 | 3 | 9 | 0.90 |
| 5 | 10 | 10 | 0 | 0 | 0.00 |
| 6 | 10 | 10 | 0 | 0 | 0.00 |
| **Total** | **60** | **60** | | | **χ²=2.00** |

**Step 5: Degrees of Freedom**
```
df = k − 1 = 6 − 1 = 5
```

**Step 6: Critical Value**
```
From χ² table: χ²(0.05, 5) = 11.07
```

**Step 7: Decision**
```
χ²_calculated = 2.00 < 11.07 (critical value)

∴ FAIL TO REJECT H₀
```

**Step 8: Conclusion**
At 5% significance level, there is insufficient evidence to conclude that the die is unfair. The observed frequencies are consistent with a fair die.

**Step 9: p-value**
```
For χ² = 2.00 with df=5:
From χ² table: p-value > 0.25

Since p-value > 0.05, we fail to reject H₀ (consistent with our decision)
```

**[15 marks: hypotheses(2), expected freq(2), chi-square calc(5), df(1), critical value(1), decision(2), conclusion(1), p-value(1)]**

---

## SOLUTION 8(a): Fermat's Little Theorem [8M]

**ANSWER:**

**Theorem Statement:**
If p is a prime number and gcd(a,p) = 1, then:
```
a^(p−1) ≡ 1 (mod p)

Equivalently: aᵖ ≡ a (mod p) for all a
```

**Proof:** (Outline using Fermat's method)

Consider the set S = {1, 2, 3, ..., p−1}

Multiply each element by a (where gcd(a,p)=1):
aS = {a, 2a, 3a, ..., (p−1)a}

**Claim:** These are all distinct modulo p and form a permutation of S.

Proof of claim:
- If ia ≡ ja (mod p) for i≠j, then p|(i−j)a
- Since gcd(a,p)=1, p must divide (i−j)
- But 1 ≤ i,j ≤ p−1, so |i−j| < p
- Contradiction unless i=j
- Therefore all elements are distinct modulo p

Product of original set:
```
1 × 2 × 3 × ... × (p−1) ≡ (p−1)! (mod p)
```

Product of multiplied set:
```
a × 2a × 3a × ... × (p−1)a ≡ a^(p−1) × (p−1)! (mod p)
```

Since they're the same set modulo p:
```
(p−1)! ≡ a^(p−1) × (p−1)! (mod p)
```

Since gcd((p−1)!, p) = 1, we can divide:
```
a^(p−1) ≡ 1 (mod p) ✓
```

**Applications:**

**(i) Find 5¹² (mod 13):**
```
p = 13 (prime)
gcd(5, 13) = 1 ✓

By Fermat's Little Theorem:
5^(13−1) ≡ 1 (mod 13)
5¹² ≡ 1 (mod 13) ✓

Answer: Remainder = 1
```

**(ii) Find 2⁵⁰ (mod 11):**
```
p = 11 (prime)
gcd(2, 11) = 1 ✓

By Fermat: 2¹⁰ ≡ 1 (mod 11)

50 = 10×5

2⁵⁰ = (2¹⁰)⁵ ≡ 1⁵ = 1 (mod 11) ✓

Answer: Remainder = 1
```

**[8 marks: theorem statement(1), proof(4), problem (i)(1.5), problem (ii)(1.5)]**

---

## SOLUTION 8(b): Euclidean Algorithm [7M]

**ANSWER:**

**Euclidean Algorithm:**

To find gcd(a,b), repeatedly apply:
```
a = bq + r  (0 ≤ r < b)
Replace (a,b) with (b,r)
Continue until r = 0
```

**Find gcd(270, 192):**

```
STEP 1:
270 = 192 × 1 + 78
        ↑      ↑
       q=1    r=78

Now find gcd(192, 78)

STEP 2:
192 = 78 × 2 + 36
       ↑     ↑
      q=2   r=36

Now find gcd(78, 36)

STEP 3:
78 = 36 × 2 + 6
      ↑     ↑
     q=2   r=6

Now find gcd(36, 6)

STEP 4:
36 = 6 × 6 + 0
     ↑     ↑
    q=6   r=0

STOP! Last non-zero remainder is 6

∴ gcd(270, 192) = 6 ✓
```

**Find lcm(270, 192):**

Using the formula:
```
lcm(a,b) × gcd(a,b) = a × b

lcm(270, 192) = (270 × 192) / gcd(270, 192)
              = 51840 / 6
              = 8640 ✓
```

**Verification:**
```
270 = 6 × 45 ✓
192 = 6 × 32 ✓
gcd(45, 32) = 1 (coprime) ✓

8640 = 270 × 32 = 192 × 45 ✓
```

**[7 marks: algorithm explanation(1), gcd steps(4), lcm formula(1), lcm calculation(1)]**

---

## SOLUTION 9(a): Eulerian and Hamiltonian Graphs [8M]

**ANSWER:**

**EULERIAN GRAPH:**

**Definition:** A graph that contains an Eulerian circuit.

**Eulerian Circuit:** A circuit that traverses every EDGE of the graph exactly once and returns to the starting vertex.

**Necessary and Sufficient Condition:**
A connected graph G has an Eulerian circuit if and only if EVERY vertex has EVEN degree.

**Eulerian Path (not circuit):**
A connected graph has an Eulerian path (but not circuit) if and only if it has EXACTLY TWO vertices of odd degree.

**Example of Eulerian Graph:**
```
    1 — 2
    |   |
    3 — 4

Degree of each vertex: deg(1)=2, deg(2)=2, deg(3)=2, deg(4)=2
All even → Eulerian circuit exists ✓

One such circuit: 1→2→4→3→1
```

---

**HAMILTONIAN GRAPH:**

**Definition:** A graph that contains a Hamiltonian circuit.

**Hamiltonian Circuit:** A circuit that visits every VERTEX of the graph exactly once (except starting vertex visited twice) and returns to start.

**Conditions:**
- **No simple necessary and sufficient condition** (NP-complete problem)
- **Dirac's Theorem (sufficient condition):**
  If G has n vertices (n≥3) and every vertex has degree ≥ n/2, then G is Hamiltonian.
- **Ore's Theorem (sufficient condition):**
  If deg(u)+deg(v) ≥ n for every pair of non-adjacent vertices u,v, then G is Hamiltonian.

**Example of Hamiltonian Graph:**
```
    1 — 2
   /|   |\
  5 |   | 3
   \|   |/
    4 — 3

Complete graph K₅
Every vertex has degree 4 ≥ 5/2 → Hamiltonian by Dirac's theorem ✓

One Hamiltonian circuit: 1→2→3→4→5→1
```

---

**COMPARISON:**

| Property | Eulerian | Hamiltonian |
|----------|---------|-------------|
| Focus | All EDGES | All VERTICES |
| Necessary & Sufficient Condition | All even degrees | No simple condition |
| Complexity | Polynomial time | NP-complete |

**[8 marks: Eulerian def(2), Eulerian condition(1), example(1), Hamiltonian def(2), Hamiltonian condition(1), example(1)]**

---

## SOLUTION 9(b): Planar Graphs & Euler's Formula [7M]

**ANSWER:**

**Planar Graph:**
A graph that can be drawn on a plane such that no two edges cross each other.

**Euler's Formula for Planar Graphs:**

**Statement:**
For any connected planar graph:
```
V − E + F = 2

where:
V = number of vertices
E = number of edges
F = number of faces (including the outer/unbounded face)
```

**Proof:**
(Proof by induction on number of edges)

**Base case:** E=0
- Graph is a single vertex
- V=1, E=0, F=1
- V−E+F = 1−0+1 = 2 ✓

**Inductive step:**
Assume formula holds for all planar graphs with < E edges.

Consider graph with E edges:

**Case 1:** Graph is a tree (no cycles)
- Tree with V vertices has E=V−1 edges
- Only one face (the outer face): F=1
- V−E+F = V−(V−1)+1 = 2 ✓

**Case 2:** Graph has a cycle
- Remove one edge e from a cycle
- This merges two faces into one: F decreases by 1
- E decreases by 1
- V unchanged
- By induction: V−(E−1)+(F−1) = 2
- Therefore: V−E+F = 2 ✓

---

**Showing K₅ is Non-Planar:**

**Method:** Use the bound E ≤ 3V−6 for planar graphs (V≥3)

For K₅ (complete graph on 5 vertices):
```
V = 5
E = C(5,2) = 5×4/2 = 10

Check planarity bound:
3V − 6 = 3(5) − 6 = 15 − 6 = 9

Since E = 10 > 9, the graph CANNOT be planar.

∴ K₅ is non-planar ✓
```

**Alternative (Kuratowski):**
K₅ is one of the two fundamental non-planar graphs (along with K₃,₃). Any graph containing K₅ as a subdivision is non-planar.

**[7 marks: planar def(1), Euler formula(1), proof(3), K₅ non-planarity(2)]**

---

*[Continue with remaining mock papers...]*

# 📄 MOCK PAPER 2 - KEY QUESTIONS ONLY

**Focus: Different Problem Types**

---

## Selected High-Value Questions:

**UNIT I - ALTERNATIVE:**
Bag I: 4 red, 3 white. Bag II: 3 red, 4 white. Bag chosen randomly, 2 balls drawn (without replacement) both red. Find P(from Bag I).

**UNIT II - ALTERNATIVE:**
MLE approach: Given sample {2, 3, 5, 7, 8} from exponential distribution f(x) = λe^(−λx), find MLE of λ.

**UNIT III - ALTERNATIVE:**
Two-sample Z-test: Sample 1 (n=50, x̄=85, s=10), Sample 2 (n=60, x̄=80, s=12). Test if μ₁ = μ₂ at 5% level.

**UNIT IV - ALTERNATIVE:**
Calculate φ(360) and use Euler's theorem to find 7^φ(360) (mod 360).

**UNIT V - ALTERNATIVE:**
Given graph with edges and weights, find MST using both Kruskal and Prim. Verify both give same weight.

---

# 🎯 HOW TO RECOGNIZE PROBLEM PATTERNS

## Pattern Recognition Guide:

### UNIT I PATTERNS:

**Pattern 1: "At least one"**
→ Use P(A∪B) = P(A)+P(B)−P(A∩B)

**Pattern 2: "Exactly one"**
→ Calculate P(A∩B') + P(A'∩B)

**Pattern 3: "Given that" or "if we know"**
→ Use conditional probability P(A|B) = P(A∩B)/P(B)

**Pattern 4: Multiple causes, one effect, "came from" or "produced by"**
→ BAYES' THEOREM

**Pattern 5: "Tossed n times, number of heads"**
→ Create distribution table, calculate E(X) and Var(X)

---

### UNIT II PATTERNS:

**Pattern 1: "Find 95%/99% confidence interval"**
→ x̄ ± z(σ/√n) where z=1.96 or 2.58

**Pattern 2: "Grouped data, find mean/variance"**
→ Use class midpoints, Σfᵢxᵢ/N

**Pattern 3: "Explain Central Limit Theorem"**
→ State: x̄ ~ N(μ, σ²/n) for large n

---

### UNIT III PATTERNS:

**Pattern 1: "Test if mean = [value]"**
→ Z = (x̄−μ₀)/(σ/√n), compare with ±1.96 or ±2.58

**Pattern 2: "Die/coin fair?" or "follows distribution?"**
→ CHI-SQUARE GOODNESS OF FIT: χ² = Σ(O−E)²/E

**Pattern 3: "Are two variables independent?" or contingency table given**
→ CHI-SQUARE TEST OF INDEPENDENCE

**Pattern 4: "Claim ≥80%" or directional claim**
→ ONE-TAILED test

**Pattern 5: "Mean different from 100?" or "has changed?"**
→ TWO-TAILED test

---

### UNIT IV PATTERNS:

**Pattern 1: "Verify (set, operation) is group/monoid"**
→ Check CAIG: Closure, Associative, Identity, Inverse

**Pattern 2: "Find inverse of each element"**
→ For (ℤₙ, +ₙ): inverse of a is n−a

**Pattern 3: "Is f a homomorphism?"**
→ Check if f(a*b) = f(a)*f(b)

**Pattern 4: "Find gcd(a,b)"**
→ EUCLIDEAN ALGORITHM (always show all steps)

**Pattern 5: "Find aⁿ (mod p)" where p is prime**
→ FERMAT'S LITTLE THEOREM: reduce using a^(p−1) ≡ 1

**Pattern 6: "Find aⁿ (mod m)" where m is composite**
→ EULER'S THEOREM: reduce using a^φ(m) ≡ 1

**Pattern 7: "Calculate φ(n)"**
→ Factor n, use φ(pᵏ) = pᵏ−pᵏ⁻¹, multiply

---

### UNIT V PATTERNS:

**Pattern 1: "Does graph have Eulerian circuit?"**
→ Check if ALL vertices have EVEN degree

**Pattern 2: "Is graph planar?"**
→ Check if E ≤ 3V−6

**Pattern 3: "Verify V−E+F=2"**
→ Count carefully, include outer face in F

**Pattern 4: "Find MST" or "minimum spanning tree"**
→ Apply Kruskal (sort edges) or Prim (grow from vertex)

**Pattern 5: "Find chromatic number"**
→ Use formulas: Kₙ→n, bipartite→2, planar→≤4

---

# 📊 FINAL EXAM STRATEGY

## Time Management (180 minutes):

```
0-10 min:   Read all questions, mark your 5
10-40 min:  Answer 1st question (Unit III - usually easiest)
40-65 min:  Answer 2nd question (Unit I - formulas)
65-90 min:  Answer 3rd question (Unit IV - theorems)
90-115 min: Answer 4th question (Unit II or V)
115-140 min: Answer 5th question (remaining unit)
140-165 min: Review all answers, add diagrams
165-180 min: Final check, ensure all labeled
```

## Answer Writing Tactics:

1. **Always start with definitions** (even if not asked)
2. **Number your steps clearly** (Step 1, Step 2...)
3. **Draw diagrams/tables** wherever possible
4. **Show ALL working** in numerical problems
5. **State formulas before using them**
6. **Box final answers**
7. **Write conclusion statements**

## Mark Optimization:

- **8M questions:** Write 4-5 points with sub-points (2M each)
- **7M questions:** Write 3-4 points with examples (1.5-2M each)
- **15M questions:** Treat as 8M+7M combined

## If You're Stuck:

- **Can't do (b)?** → Do (a) fully, attempt (b) with definitions
- **Don't know theorem proof?** → State theorem, give example, get partial marks
- **Forgot formula?** → Derive from first principles, show logic
- **No time left?** → Write point-form answers, better than blank

---

# ✅ 3-DAY COMPLETION CHECKLIST

## Day 1: ☐ Unit I + Unit III
- [ ] Read all Unit I theory
- [ ] Solve 3 Bayes' problems
- [ ] Read all Unit III theory
- [ ] Solve 2 Chi-square problems
- [ ] Write 1 complete hypothesis test

## Day 2: ☐ Unit IV
- [ ] Memorize CAIG table
- [ ] Solve 3 Euclidean algorithm problems
- [ ] Solve 3 Fermat/Euler problems
- [ ] Practice homomorphism proofs

## Day 3: ☐ Unit II + V + Mock Tests
- [ ] Memorize CI formulas (1.96, 2.58)
- [ ] Solve 1 grouped data problem
- [ ] Memorize Euler's formula V−E+F=2
- [ ] Memorize Eulerian condition (all even)
- [ ] Attempt Mock Paper 1 timed (3 hours)
- [ ] Review solutions
- [ ] List formulas on one page

## Exam Eve:
- [ ] Review formula sheet
- [ ] Skim all solved examples
- [ ] Sleep well (7-8 hours)
- [ ] Don't study new content

---

# 🎯 FINAL CONFIDENCE BOOSTER

**You will score 40+ if you:**

✓ Memorize the Bayes' factory problem
✓ Can do one full Chi-square test
✓ Remember Fermat's theorem and Euclidean algorithm
✓ Know the CI formulas (1.96, 2.58)
✓ Can state Euler's formula and Eulerian condition

**These 5 topics alone can give you 35-40 marks.**

**Add partial marks from other attempts → Easy 45-50 marks!**

---

**Good luck! You've got this! 💪🔥**

*Remember: It's not about perfection, it's about scoring 40+. Strategic preparation beats exhaustive preparation.*
