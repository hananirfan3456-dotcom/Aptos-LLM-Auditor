# AptosMove-Guard: Automated LLM Bug Hunting Framework

An advanced, open-source automated vulnerability detection and static analysis framework designed specifically for **Aptos Move Smart Contracts**. This project leverages localized, high-parameter reasoning LLMs to audit, identify, and benchmark security flaws without compromising data privacy.

---

## 🚀 Core Objective

Web3 auditing typically relies on centralized APIs, which poses a massive risk of zero-day vulnerability leaks. **AptosMove-Guard** runs entirely on local, decentralized infrastructure utilizing high-performance open-source models to analyze Aptos Move code structure, structural logic, and state management under complete data sovereignty.

## 🧠 Model Architecture & Infrastructure

To handle complex Move language semantics and complex logic structures, the framework orchestrates a dual-model pipeline distributed via Tensor Parallelism (`vLLM`):

1. **DeepSeek-R1 (Distill Qwen 70B):** Utilized for deep chain-of-thought reasoning, multi-step logic verification, and contextual bug synthesis.
2. **Qwen-2.5 (72B):** Utilized for structural syntax validation, abstract syntax tree (AST) code comprehension, and standard Move pattern matching.

### Hardware Requirement Target
* **Compute Cluster:** 2x NVIDIA A100 (80GB VRAM) running continuously on On-Demand/Reserved infrastructure to host full unquantized weights with optimal throughput and context windows.

---

## 🛠️ Project Roadmap & Milestones

### 📅 Phase 1: Environment Setup & Prompt Pipeline (Month 1)
* Deploy local inference endpoints using `vLLM` across a 2x A100 GPU cluster.
* Structure foundational prompt templates specifically optimized for the Move programming language rules (resource safety, linear types, and signers).

### 📅 Phase 2: Core Analysis Engine & Inference (Month 2)
* Build the automated pipeline to digest multi-file Aptos modules.
* Conduct continuous heavy inference loops to cross-examine security patterns against known Aptos/Move vulnerability vectors.

### 📅 Phase 3: Benchmarking & Open-Source Release (Month 3)
* Benchmark LLM detection accuracy against classic vulnerabilities (reentrancy-equivalents, integer overflows, and missing access controls).
* Open-source the fully functional benchmarking tool and inference scripts for the Web3 developer community.

---

## 🔒 Security & Privacy Notice
This project enforces a **Local-First** policy. No source code processed by AptosMove-Guard is ever sent to third-party endpoints or closed-source API vendors. 
