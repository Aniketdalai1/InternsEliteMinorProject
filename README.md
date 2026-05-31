# InternsEliteMinorProject
# 🧠 DSA Visualizer (C++)

> A terminal-based **Data Structures & Algorithms Visualizer** that walks you through sorting and searching algorithms **step by step**, printing each comparison, swap, and decision to the console in real time.

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Project Structure](#-project-structure)
- [Algorithms Covered](#-algorithms-covered)
  - [Bubble Sort](#-bubble-sort)
  - [Selection Sort](#-selection-sort)
  - [Binary Search](#-binary-search)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Compilation](#compilation)
  - [Run](#run)
- [Usage Guide](#-usage-guide)
- [Sample Output](#-sample-output)
- [Tech Stack](#-tech-stack)
- [Future Improvements](#-future-improvements)
- [Contributing](#-contributing)
- [License](#-license)

---

## 📖 Overview

DSA Visualizer is a lightweight C++ console application designed to help students and developers **understand how classic algorithms work internally**. Instead of just showing the final result, it displays every intermediate step — comparisons, swaps, pointer movements — so you can truly follow along.

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔵 **Bubble Sort Visualization** | Shows every comparison and swap pass-by-pass |
| 🟢 **Selection Sort Visualization** | Displays array state after each minimum selection |
| 🔴 **Binary Search Visualization** | Prints `low`, `mid`, `high` pointers at every step |
| 🔁 **Loop Menu** | Continuously run algorithms without restarting |
| ⚡ **Lightweight** | Pure C++, zero external dependencies |

---

## 📁 Project Structure

```
dsa-visualizer/
│
├── main.cpp          # Entry point — menu loop and user input handling
├── sorting.cpp       # Bubble Sort & Selection Sort implementations
├── searching.cpp     # Binary Search implementation
└── README.md         # Project documentation
```

---

## 🔍 Algorithms Covered

### 🔵 Bubble Sort

**Time Complexity:** O(n²) &nbsp;|&nbsp; **Space Complexity:** O(1) &nbsp;|&nbsp; **Stable:** ✅ Yes

Repeatedly compares adjacent elements and swaps them if out of order. The largest element "bubbles up" to the end with each pass.

**Visualization shows:**
- Current pass number
- Every pair being compared
- Whether a swap occurred
- The full array state after each comparison

---

### 🟢 Selection Sort

**Time Complexity:** O(n²) &nbsp;|&nbsp; **Space Complexity:** O(1) &nbsp;|&nbsp; **Stable:** ❌ No

Finds the minimum element in the unsorted portion and places it at the beginning. Repeats for the rest of the array.

**Visualization shows:**
- The array state after each minimum selection and placement

---

### 🔴 Binary Search

**Time Complexity:** O(log n) &nbsp;|&nbsp; **Space Complexity:** O(1) &nbsp;|&nbsp; **Prerequisite:** ⚠️ Array must be sorted

Repeatedly halves the search range by comparing the target to the middle element.

**Visualization shows:**
- Current `low`, `high`, `mid` indices and their values
- Direction of movement (`Move Left` / `Move Right`)
- Final result: found at index or not found

---

## 🚀 Getting Started

### Prerequisites

- A C++ compiler with **C++11 or later** support
  - Linux/macOS: `g++` (GCC) or `clang++`
  - Windows: MinGW, MSVC, or WSL with g++

Verify your compiler:
```bash
g++ --version
```

---

### Compilation

Compile all source files together using:

```bash
g++ main.cpp sorting.cpp searching.cpp -o app
```

**Optional flags for better debugging:**
```bash
g++ main.cpp sorting.cpp searching.cpp -o app -Wall -Wextra -std=c++17
```

---

### Run

```bash
./app
```

On Windows:
```bash
app.exe
```

---

## 📘 Usage Guide

Once the program starts, you'll see the main menu:

```
====== DSA VISUALIZER ======
1. Bubble Sort
2. Selection Sort
3. Binary Search
4. Exit
Enter choice:
```

**Steps:**
1. Enter the number corresponding to your desired algorithm.
2. Input the size of the array.
3. Enter the array elements one by one.
4. For **Binary Search**, make sure the array is sorted beforehand, then enter the target value.
5. Watch the step-by-step visualization in the console.
6. Return to the menu after each run — select `4` to exit.

> ⚠️ **Note for Binary Search:** The program assumes the input array is already sorted. Passing an unsorted array will produce incorrect results.

---

## 🖥️ Sample Output

**Bubble Sort** on `[5, 3, 1, 4, 2]`:
```
PASS 1
Comparing 5 and 3
Swapped: 3 5 1 4 2
Comparing 5 and 1
Swapped: 3 1 5 4 2
...
```

**Binary Search** for `7` in `[1, 3, 5, 7, 9, 11]`:
```
Low: 0  High: 5  Mid: 2  Value: 5
Move Right
Low: 3  High: 5  Mid: 4  Value: 9
Move Left
Low: 3  High: 3  Mid: 3  Value: 7
Found at index 3
```

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| Language | C++ (C++11/17) |
| Compiler | g++ / clang++ |
| Platform | Cross-platform (Linux, macOS, Windows) |
| Dependencies | None (Standard Library only) |

---

## 🔮 Future Improvements

- [ ] Add **Insertion Sort** and **Merge Sort** visualizations
- [ ] Add **Linear Search** alongside Binary Search
- [ ] Introduce **color-coded output** using ANSI escape codes
- [ ] Add **time measurement** to compare algorithm performance
- [ ] Implement a **file input** option for loading arrays from `.txt` files
- [ ] Add a **graphical mode** using a simple TUI library (e.g., ncurses)

---

## 🤝 Contributing

Contributions are welcome! To get started:

1. Fork this repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m "Add: your feature description"`
4. Push to your branch: `git push origin feature/your-feature-name`
5. Open a **Pull Request**

Please ensure your code follows consistent formatting and includes comments where necessary.

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

<div align="center">
  Made with ❤️ in C++ &nbsp;|&nbsp; Happy Learning! 🎓
</div>
