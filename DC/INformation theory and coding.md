# Information Theory and Coding

## 8.1 Entropy

**Entropy (H)** is the measure of average information (uncertainty) in a source. It represents the theoretical minimum number of bits required per symbol.

$$H = \sum_{k=1}^{n} p_k \log_2 1/p_k \quad \text{bits/symbol}$$

**Average Code Length:**

$$\bar{L} = \sum_{k=1}^{n} p_k \cdot l_k \quad \text{bits/symbol}$$

**Efficiency:**

$$\eta = \frac{H}{\bar{L}} \times 100\%$$

Higher efficiency means the code is closer to the theoretical minimum. A perfect code has $\eta = 100\%$, meaning $\bar{L} = H$.

---

## 8.2 Source Coding
Source coding is a technique used in information theory to efficiently represent data for transmission, ensuring that the original information can be accurately reconstructed. Without source coding, transmission wastes bandwidth on redundant data.

### Necessity

- Removes redundancy from the source data.
- Reduces average bit rate → less bandwidth required.
- Makes transmission more efficient and storage more compact.


| Fixed Length | Variable Length |
|---|---|
| Same bits for all symbols | Shorter bits for frequent symbols |
| Simple, easy to decode | More complex decoding |
| Wasteful of bandwidth | Bandwidth efficient |
| Example: ASCII (8 bits) | Example: Huffman coding |

### 1. Binary Huffman Coding
Huffman coding is a lossless source coding technique that assigns shorter binary codes to more frequent symbols and longer codes to less frequent symbols, minimizing the average number of bits needed to represent a message. It builds an optimal prefix-free binary tree called the **Huffman tree**.

**Algorithm**
1. List all symbols with their probabilities.
2.  Sort symbols in **decreasing order** of probability.
3.  Take the **two lowest probability nodes**, merge them into a new node with probability equal to their sum.
4.  Insert the new node back and **re-sort**. (If the new probability is same as other, the new probability is given higher priority).
5.  Repeat steps 3–4 until only two branches remains.
6.  Assign **0 to top branch and 1 to the bottom** consistently throughout.
7.  Trace path from **root to each symbol** to get its codeword *and flip the codeword to get the actual one*.

https://www.youtube.com/watch?v=icZ5asGMBEY

---

### 2. Shannon-Fano Coding
Shannon-Fano coding is a lossless source coding technique that assigns shorter
codes to more probable symbols. Unlike Huffman which builds the tree bottom-up,
Shannon-Fano builds the tree **top-down** by recursively splitting symbols into
two groups of nearly equal probability.

**Algorithm**
1. List all symbols in **decreasing order** of probability.
2. Split the list into **two groups** such that the sum of probabilities of each
   group is as nearly equal as possible.
3. Assign **0 to the top group** and **1 to the bottom group**.
4. Recursively repeat steps 2–3 for each group until every group has only
   one symbol.
5. The codeword for each symbol is the sequence of 0s and 1s assigned along
   its path.

https://www.youtube.com/watch?v=U-SpTfzZwFY

---


## 8.3 Hamming Distance
**Hamming Distance** between two codewords is the number of bit positions in which they differ. It is a measure of how different two codewords are from each other.

$$d(x, y) = \text{number of positions where } x \text{ and } y \text{ differ}$$

XOR trick: XOR the two codewords and count the `1`s in the result.

$$10101 \oplus 11100 = 01001 \rightarrow d = 2$$

---

**Minimum Hamming Distance ($d_{min}$)** is the smallest Hamming distance between any two valid codewords in the entire codebook. It is the most important parameter of a code because it directly determines how many errors the code can **detect** and **correct**.

The idea is simple — when a codeword is transmitted and some bits flip due to noise, the received word moves "away" from the original codeword in Hamming space. If the minimum distance between any two valid codewords is large enough, the receiver can tell that an error occurred (detection) or even figure out which codeword was originally sent (correction).

$$d_{min} = \min_{x \neq y} \ d(x, y)$$

| Capability | Requirement |
|---|---|
| Detect up to $e$ errors | $d_{min} \geq e + 1$ |
| Correct up to $t$ errors | $d_{min} \geq 2t + 1$ |

A larger $d_{min}$ means the codewords are more spread apart, giving the code stronger error handling ability. For example, a code with $d_{min} = 3$ can detect up to 2 errors or correct up to 1 error.

