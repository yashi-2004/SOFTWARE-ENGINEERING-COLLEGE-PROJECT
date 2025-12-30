# SOFTWARE-ENGINEERING-COLLEGE-PROJECT
AI-assisted symbolic execution framework for C/C++ programs using KLEE and Z3. Automatically explores execution paths, detects bugs, generates test cases, computes coverage, and applies LLM-based repair with validation. Designed using core software engineering principles.

# AI-Assisted Symbolic Execution Framework for Bug Detection and Repair

## 📌 Overview

This project implements an **AI-assisted symbolic execution system for automated bug detection, test generation, and program repair in C/C++ programs**. It combines **formal methods (symbolic execution using KLEE and Z3)** with **large language models (LLMs)** to systematically analyse programs and improve software reliability.

Unlike traditional testing, which relies on manually chosen inputs, this system explores **all feasible execution paths symbolically**, ensuring that bugs reachable through any input are detected.

---

## 🎯 Key Features

* Accepts **C/C++ source code**
* Compiles code into **LLVM bitcode**
* Performs **symbolic execution using KLEE**
* Detects bugs such as:

  * Division by zero
  * Null pointer dereferences
  * Buffer overflows
  * Assertion and memory errors
* Generates **concrete test cases (.ktest)**
* Computes **code coverage**
* Classifies bugs by severity
* Uses **AI (LLMs)** to propose and validate code repairs
* Produces structured reports and visualisations

---

## 🧠 What is Symbolic Execution?

Symbolic execution executes a program using **symbolic inputs instead of concrete values**.
At each conditional branch, execution forks into multiple paths, collecting constraints that describe when each path is feasible. These constraints are solved using an SMT solver (Z3) to generate concrete test inputs that trigger bugs.

This approach enables **systematic and near-complete path coverage**, uncovering bugs that traditional testing often misses.

---

## ⚙️ Technologies Used

* **Programming Languages:** C, C++, Python
* **Symbolic Execution:** KLEE
* **Constraint Solver:** Z3
* **Intermediate Representation:** LLVM Bitcode
* **AI Repair:** Large Language Models (GPT/Claude)
* **Backend:** Python
* **Testing:** pytest, pytest-cov
* **Version Control:** Git, GitHub

---

## 🏗 Development Methodology

The project follows the **Spiral Model**, allowing iterative development with continuous risk analysis, prototyping, testing, and refinement. This was particularly suitable due to uncertainties related to symbolic execution scalability and AI-based repairs.

---

## 🧪 Testing Strategy

The system was tested at three levels:

1. **Unit Testing:** Individual modules tested independently using pytest
2. **Integration Testing:** Contract-based testing between modules using predefined JSON schemas
3. **System Testing:** End-to-end testing using real C programs

**Results:**

* ~85–90% code coverage
* ~85–90% bug detection accuracy
* Successful validation of all major functional and non-functional requirements

---

## ⏱ Performance

* Small programs (<200 lines): under **5 minutes**
* Medium programs (200–500 lines): under **15 minutes**
* Secure sandboxed execution
* New users productive within ~30 minutes

---

## ⚠️ Limitations

* Path explosion for highly complex programs
* Constraint solver timeouts for complex arithmetic
* Partial support for advanced C features
* AI-generated repairs may not always be semantically perfect

The system performs best on **focused modules under ~500 lines**, which is typical for symbolic execution tools.

---

## 📄 Conclusion

This project demonstrates the practical integration of **formal program analysis techniques** with **modern AI-based repair mechanisms**, showcasing a complete software engineering workflow from requirement analysis to implementation, testing, and validation.

