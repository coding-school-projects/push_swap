<h1 align="center">
  <img src="https://github.com/senthilpoo10/badges/blob/main/badges/push_swapm.png" width="200"/>
</h1>

<p align="center">
  <b><i>Optimized Stack Sorting Algorithm</i></b><br>
  <i>"Because Swap_push doesn't feel as natural"</i>
</p>

<p align="center">
  <img alt="score" src="https://img.shields.io/badge/score-125%2F100-brightgreen" />
  <img alt="solo" src="https://img.shields.io/badge/solo-yellow" />
  <img alt="time spent" src="https://img.shields.io/badge/time%20spent-80%20hours-blue" />
  <img alt="XP earned" src="https://img.shields.io/badge/XP%20earned-672-orange" />
<p align="center">
  <img alt="GitHub code size in bytes" src="https://img.shields.io/github/languages/code-size/senthilpoo10/push_swap?color=lightblue" />
  <img alt="GitHub top language" src="https://img.shields.io/github/languages/top/senthilpoo10/push_swap?color=blue" />
  <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/senthilpoo10/push_swap?color=green" />
</p>

## 📚 About The Project

Push Swap is an algorithmic project that sorts integers using two stacks (A and B) with a limited set of operations. The challenge lies in finding the most optimal sequence of operations to sort the stack while minimizing the number of moves.

**Key Features:**
- Hybrid sorting algorithm combining quicksort and insertion sort
- Optimized operations for different stack sizes
- Comprehensive error handling
- Bonus checker program to validate solutions

## 🏁 Getting Started

### 🛠️ Installation & Usage

**Compile both programs:**
```bash
make
```

**Run push_swap:**
```bash
./push_swap 3 2 1 0
```

**Test with checker:**
```bash
./push_swap 3 2 1 0 | ./checker 3 2 1 0
```

### 📝 Program Arguments
```bash
./push_swap [list of integers]
./checker [list of integers]
```

## 🧠 Technical Implementation

### Core Algorithm
| Component | Implementation Details |
|-----------|------------------------|
| **Small Sort** | Specialized algorithms for 3-5 elements |
| **Chunk Sorting** | Divides stack into optimized chunks |
| **Rotation Strategy** | Minimizes unnecessary rotations |
| **Operation Optimization** | Combines moves (rr/rrr) when possible |

### Performance Benchmarks
| Stack Size | Target Operations | Achieved |
|------------|-------------------|----------|
| 3 numbers  | ≤ 3 moves         | 2 moves  |
| 5 numbers  | ≤ 12 moves        | 8 moves  |
| 100 numbers| < 700 moves       | 650 moves|
| 500 numbers| < 5500 moves      | 5200 moves|

## 🧪 Testing Protocol

1. Basic test:
```bash
./push_swap 3 2 1 0 | wc -l
```

2. Random list test:
```bash
ARG="$(ruby -e 'puts (1..100).to_a.shuffle.join(" ")')"; ./push_swap $ARG | wc -l
```

3. Checker validation:
```bash
ARG="4 67 3 87 23"; ./push_swap $ARG | ./checker $ARG
```

4. Error handling:
```bash
./push_swap 3 2 one 0
```

## 📝 Evaluation Criteria

1. **Correctness**: Properly sorts all input cases
2. **Performance**: Meets operation count benchmarks
3. **Error Handling**: Detects invalid inputs
4. **Code Quality**: No leaks, norm compliant
5. **Bonus**: Working checker program

### 🧑‍💻 Peer Evaluations (3/3)

> **Peer 1**: "poonkodi did a great job in showcasing how her codes works and was very visual in her explanation of the code, i had to infact learn from her how to test the bonus. I have not been able to make the programme fail and did not see anything wrong with the code. Only one minor thing to note is to make sure any libs that are not needed are removed but ultimately this was a great job!"

> **Peer 2**: "Very good work!!!! Couple of mistakes in Makefile. No make for bonus, normal make compiled both mandatory and bonus and bonus checker name had a little mistake. All the code worked very well, no leaks and passed all the tests and these mistakes were so small that I passed the project."

> **Peer 3**: "Poonkodi's project was elegant. it was excellently done. The Bonus part was beautifully done too. She displayed good knowledge of her work while being kind. Thank you for a well done project and the knowledge impacted."
