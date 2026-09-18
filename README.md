# Math Learning & Assessment Portal 📐🔢

A standalone, responsive, client-side web application suite for learning, practicing, and testing foundational middle-school mathematics, specifically **Number Systems**, **Factors & Multiples**, **Prime Factorisation**, and **HCF & LCM**.

Zero dependencies, zero build steps, zero server requirements. Open [index.html](index.html) in any modern browser to get started.

---

## 🚀 Live Portal Hub: `index.html`

The homepage organizes the suite into three core sections:

### 1. 📚 Learning Materials
Interactive study sheets and concept reference notes accessible via modal cards:
* **🔢 Number System**: Number families ($\mathbb{N}, \mathbb{W}, \mathbb{Z}, \mathbb{Q}$, irrationals), definitions, hierarchies, and divisibility rules ($2, 3, 5, 9, 10$).
* **🧮 Factors**: Factors, factor pairs, multiples, prime vs composite classifications, and the special properties of $0, 1,$ and $2$.
* **🔢 Prime Factorisation**: The Fundamental Theorem of Arithmetic, factor trees, repeated division ladder method, and index/exponential notation ($2^3 \times 3^2$).
* **➗ HCF & LCM**: Conceptual meanings, prime power selection rules (lowest powers for HCF, highest powers for LCM), worked examples, and the product identity $a \times b = \text{HCF}(a,b) \times \text{LCM}(a,b)$.

---

### 2. 📝 Practice
Self-paced interactive visualizers and generated practice rounds:
* **Factors Practice** ([`factors-practice.html`](factors-practice.html)): 50-question dynamic practice round across 5 progressive difficulty tiers. Questions test prime factorisation, LCM, and HCF with instant feedback and a post-session scorecard.
* **2-Number HCF & LCM Explorer** ([`hcf_lcm_2_number_interactive.html`](hcf_lcm_2_number_interactive.html)): Interactive prime-factor visualizer for two numbers. Move sliders ($1–200$) to view prime factor partitions (shared factors vs unique factors) and dynamically computed HCF and LCM formulas.
* **3-Number HCF & LCM Explorer** ([`hcf_lcm_3_number_interactive.html`](hcf_lcm_3_number_interactive.html)): Interactive prime-factor visualizer for three numbers ($A, B, C$). Visualizes pairwise and 3-way shared prime factors with step-by-step calculations.

---

### 3. 🎯 Tests
Formal, timed assessments with full scoring and review:
* **Number System Test** ([`Number_System_Practice-2.html`](Number_System_Practice-2.html)):
  * **Format**: 50 questions, 20-minute timer.
  * **Topics**: Natural, whole, integer, rational, irrational classifications, odd/even, primes, and divisibility shortcuts.
  * **Features**: Live progress bar, instant option highlight feedback, and final score summary.
* **50 Question HCF/LCM Quiz** ([`Prime_Factorisation_HCF_LCM_50_Question_Quiz.html`](Prime_Factorisation_HCF_LCM_50_Question_Quiz.html)):
  * **Format**: 50 questions, 20-minute timer.
  * **Topics**: Prime numbers, factor trees, prime factorisation, HCF, LCM, and real-world word problems (cycle coincidences, equal division).
  * **Features**: Shuffled questions & options, navigation between questions, comprehensive score card, detailed answer review with explanations, and print-ready results.

---

## 📁 Repository Structure

```text
test-paper/
├── index.html                                        # Main Portal Hub (Home page)
├── Number_System_Practice-2.html                     # 50-Question Number System Practice Test
├── Prime_Factorisation_HCF_LCM_50_Question_Quiz.html # 50-Question Timed HCF & LCM Quiz
├── factors-practice.html                             # Multi-tier generated factors practice
├── hcf_lcm_2_number_interactive.html                 # 2-Number HCF & LCM Interactive Explorer
├── hcf_lcm_3_number_interactive.html                 # 3-Number HCF & LCM Interactive Explorer
└── README.md                                         # Project Documentation
```

---

## 🛠️ How to Run

### Direct Browser Access (Simplest)
Double-click [`index.html`](index.html) or open it in any modern browser (Chrome, Firefox, Edge, Safari).

### Local HTTP Server (Optional)
If you prefer running a local server:
```bash
# Using Python 3:
python -m http.server 8000

# Using Node (npx):
npx serve .
```
Then visit `http://localhost:8000` in your web browser.

### GitHub Pages Deployment
1. Go to repository **Settings** &rarr; **Pages**.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Set the branch to `main` and root folder `/`.
4. Your portal will be immediately live on `<username>.github.io/<repo-name>/`.

---

## 📚 Syllabus & Curriculum Coverage

Designed for middle school mathematics (CBSE Grade 6–8, ICSE, Cambridge Lower Secondary, and Math Olympiad preparation):
1. **Numbers**: $\mathbb{N}, \mathbb{W}, \mathbb{Z}, \mathbb{Q}$, terminating vs non-terminating decimals, irrationality of $\sqrt{2}, \sqrt{3}, \pi$.
2. **Divisibility Tests**: Divisibility by $2, 3, 5, 9, 10$.
3. **Primes & Composites**: Sieve intuition, uniqueness of 2 as an even prime, why 1 is neither prime nor composite.
4. **Prime Factorisation**: Unique prime factorisation, factor trees, ladder division.
5. **HCF (GCF)**: Greatest common divisor by prime factor powers (minimum exponent rule).
6. **LCM**: Least common multiple by prime factor powers (maximum exponent rule).
7. **Word Problems**: Practical applications (bus schedules, bells ringing, equal distribution of goods).
