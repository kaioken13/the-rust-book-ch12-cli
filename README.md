# 🛠️ Rust System Toolchain: High-Performance CLI Suite
### *Advanced implementation of system utilities based on The Rust Book (Ch. 12)*

---

## 🚀 Overview
This repository contains a suite of Command Line Interface (CLI) tools developed to explore Rust's core strengths: memory safety, zero-cost abstractions, and performance. What started as a foundational exercise has been refactored into a modular infrastructure toolchain designed for efficient file processing and data stream manipulation.

## 🏗️ Engineering Highlights (Beyond the Book)
Moving past the basic tutorial, this project incorporates "Elite-level" software engineering patterns:

* **Iterator Patterns (Zero-Cost Abstractions):** Replaced manual `for` loops with functional iterator chains (`filter`, `collect`), enhancing both readability and execution speed.
* **Multi-Binary Architecture:** Utilizes the `src/bin/` directory to manage multiple independent executables (`grep`, `ls`) sharing a centralized core logic (`lib.rs`).
* **Zero-Copy Config Parsing:** Optimized `Config::build` using an iterator-based approach to minimize `.clone()` calls and reduce memory overhead.
* **Modular System Design:** Clear separation of concerns between the user interface (binaries) and the core business logic (library modules).

---

## 🛠️ Included Tools

### 1. `minigrep`
A robust text search engine.
* **Features:** Case-sensitive and case-insensitive search (via environment variables), idiomatic error handling, and optimized search logic.
* **Usage:**
    ```bash
    cargo run --bin grep -- "search_term" "file.txt"
    ```

### 2. `minils`
A lightweight directory listing utility.
* **Features:** Direct interaction with the `std::fs` module for high-speed file system metadata retrieval.
* **Usage:**
    ```bash
    cargo run --bin ls
    ```

---

## 🧪 Core Rust Concepts Applied
* **Lifetimes & Ownership:** Efficient management of string references during intensive search operations.
* **Error Propagation:** Leveraging `Box<dyn Error>` and the `Result` type for resilient application flow.
* **TDD (Test-Driven Development):** Integrated unit test suite validating search logic and case-sensitivity edge cases.

---

## 📈 Engineering Roadmap (MLOps Focus)
This toolchain serves as the backbone for a high-performance genomic data pipeline:
- [ ] **Parallel Processing:** Implementing multi-threaded search using the `rayon` crate.
- [ ] **Data Engine Integration:** Integrating the **Polars** engine for large-scale Matrix/Parquet manipulation.
- [ ] **Pattern Matching:** Adding Regex support for DNA sequence identification.

---

## 👨‍💻 Author
**Thiago Aragão da Silva**
*Data Science Student @ USP - ICMC | Powerbuilder | BJJ Practitioner*

---
*Built with the precision and performance that only Rust provides.*
