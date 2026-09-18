# Quantitative Aptitude Learning & Assessment Portal 🎯📊

A high-performance, standalone, responsive web application suite tailored for **Quantitative Aptitude Training, Campus Placement Preparation (CRT), and Competitive Examinations** (CAT, GATE, GMAT, GRE, Banking PO/Clerk, SSC CGL, and UPSC CSAT).

Zero dependencies, zero build tools, and fully client-side. Simply open [`index.html`](index.html) in any modern web browser or deploy directly with GitHub Pages.

---

## 🎯 Target Examinations & Use Cases

* **Campus Placement Drives (CRT)**: TCS NQT, Infosys, Cognizant, Wipro, Accenture, Capgemini, and Core Engineering aptitude screenings.
* **Management & Graduate Entrances**: CAT, XAT, NMAT, SNAP, CMAT, GRE, GMAT.
* **Government & Banking Examinations**: IBPS PO/Clerk, SBI PO, RBI Grade B, SSC CGL/CHSL, Railways RRB, UPSC CSAT.
* **Technical Competitive Exams**: GATE General Aptitude section.

---

## 🚀 Portal Architecture (`index.html`)

The main dashboard organizes quantitative prep into three structured modules:

```
                       [ index.html ] (Portal Hub)
                             │
        ┌────────────────────┼────────────────────┐
        ▼                    ▼                    ▼
📚 Learning Materials    📝 Practice          🎯 Tests
  ├── Number System        └── HCF/LCM Tools    ├── Number System Mock (50 Qs)
  ├── Prime Factorisation       (2 & 3 Numbers) ├── HCF & LCM Mock (50 Qs)
  ├── HCF & LCM Shortcuts                       └── Factors Speed Drill (50 Qs)
  └── Factors Theory
```

---

### 1. 📚 Learning Materials (Aptitude Concept Guides & Cheat Sheets)
Modal-accessible reference guides loaded with speed-math shortcuts and exam formulas:
* **🔢 Number System**: Real number classifications ($\mathbb{N}, \mathbb{W}, \mathbb{Z}, \mathbb{Q}$, irrationals), pure vs mixed recurring decimal to fraction shortcuts ($0.\bar{a} = a/9$), unit digit cyclicity, and fast divisibility tests ($2, 3, 4, 5, 8, 9, 10, 11$).
* **🔢 Prime Factorisation**: Canonical prime power representation $N = p_1^{a_1} p_2^{a_2} \dots p_k^{a_k}$, properties of coprime pairs ($\text{HCF}=1$), counting trailing zeroes via $\min(\text{powers of } 2, \text{powers of } 5)$, and prime form $6k \pm 1$.
* **➗ HCF & LCM**: Fast prime power rules (lowest powers for HCF, highest powers for LCM), the two-number product identity $A \times B = \text{HCF} \times \text{LCM}$, HCF/LCM of fractions, and classic aptitude problem models (circular track meetings, simultaneous bell ringings, rectangular tile optimization).
* **🧮 Factors & Multiples**: The total number of factors formula $T(N) = (a+1)(b+1)(c+1)$, even vs odd factor splits, factor pairs, and the perfect square odd-factors theorem.

---

### 2. 📝 Practice (Interactive Visual Explorers)
* **2-Number HCF & LCM Explorer** ([`hcf_lcm_2_number_interactive.html`](hcf_lcm_2_number_interactive.html)): Interactive prime-factor visualizer for two numbers. Sliders ($1–200$) illustrate shared vs unique prime factor allocations, Venn clusters, and live step-by-step arithmetic.
* **3-Number HCF & LCM Explorer** ([`hcf_lcm_3_number_interactive.html`](hcf_lcm_3_number_interactive.html)): Visualizer for three numbers ($A, B, C$) demonstrating pairwise overlaps, 3-way shared factors, and greatest common divisor / least common multiple calculations.

---

### 3. 🎯 Tests (Timed Sectional Mocks & Drills)
* **Number System Sectional Test** ([`Number_System_Practice-2.html`](Number_System_Practice-2.html)):
  * **Duration**: 20 Minutes • **Questions**: 50 MCQs.
  * **Syllabus**: Number categories, divisibility rules, even/odd parity, prime properties, and fraction forms.
  * **Features**: Live timer, real-time feedback, and automated performance categorization (Correct / Wrong / Unreached).
* **Prime Factorisation, HCF & LCM Quiz** ([`Prime_Factorisation_HCF_LCM_50_Question_Quiz.html`](Prime_Factorisation_HCF_LCM_50_Question_Quiz.html)):
  * **Duration**: 20 Minutes • **Questions**: 50 MCQs.
  * **Syllabus**: Prime identification, factor tree end-nodes, prime factorization, HCF/LCM calculations, and real-world aptitude word problems.
  * **Features**: Randomized questions and answer options, question navigation, comprehensive scorecard with explanation review, and print-ready results.
* **Quant Sprint Mock** ([`quant_quiz.html`](quant_quiz.html)):
  * **Duration**: 20 Minutes • **Questions**: 50 MCQs.
  * **Syllabus**: Time & Work (rates, efficiency), Time, Speed & Distance (relative speed, trains), and Percentages.
  * **Features**: Live timer, immediate explanation on incorrect choices, and topic-wise performance breakdown.
* **Aptitude Foundations Challenge** ([`aptitude_50_questions_20min.html`](aptitude_50_questions_20min.html)):
  * **Duration**: 20 Minutes • **Questions**: 50 MCQs.
  * **Syllabus**: Foundational arithmetic (worker-days, pipes & cisterns, speeds, percentages).
  * **Features**: Prev/Next question navigation, instant worked solutions, and final review list.
* **Factors Speed Practice** ([`factors-practice.html`](factors-practice.html)):
  * **Duration**: Self-paced / timed drill • **Questions**: 50 dynamic questions.
  * **Syllabus**: Prime factorisation, LCM, and HCF across 5 progressive difficulty tiers.
  * **Features**: Immediate answer validation, step-by-step solutions, and detailed error review log.

---

## 📁 Repository Structure

```text
test-paper/
├── index.html                                        # Aptitude Portal Dashboard (Homepage)
├── Number_System_Practice-2.html                     # 50-Question Number System Sectional Mock
├── Prime_Factorisation_HCF_LCM_50_Question_Quiz.html # 50-Question HCF & LCM Sectional Mock
├── quant_quiz.html                                   # 50-Question Quant Sprint (Work, Speed, %)
├── aptitude_50_questions_20min.html                  # 50-Question Aptitude Foundations Challenge
├── factors-practice.html                             # 5-Tier Generated Factors & Primes Speed Drill
├── hcf_lcm_2_number_interactive.html                 # 2-Number Prime Factor & LCM Interactive Tool
├── hcf_lcm_3_number_interactive.html                 # 3-Number Prime Factor & LCM Interactive Tool
└── README.md                                         # Project Documentation
```

---

## 🛠️ How to Run & Deploy

### 1. Direct Browser Access (Simplest)
Double-click [`index.html`](index.html) or open it in any modern browser (Chrome, Firefox, Edge, Safari). No installation or network connection required.

### 2. Local HTTP Server (Optional)
```bash
# Python 3:
python -m http.server 8000

# Node.js:
npx serve .
```
Access via `http://localhost:8000`.

### 3. GitHub Pages Deployment
1. Navigate to **Settings** &rarr; **Pages** in the repository.
2. Select **Deploy from a branch** under *Build and deployment*.
3. Choose branch `main` and root folder `/`.
4. The aptitude portal will deploy to `https://<username>.github.io/<repo-name>/`.

---

## 🏷️ Tags & Topic Keywords

`#quantitative-aptitude` `#campus-placements` `#cat-quant` `#gate-aptitude` `#banking-po` `#ssc-cgl` `#number-systems` `#prime-factorisation` `#hcf-lcm` `#speed-math` `#timed-mocks`
