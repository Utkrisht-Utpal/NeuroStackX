# CODEXPATH AI

> Transforming real-world codebases into structured learning experiences.

---

## 📌 Overview

**CODEXPATH AI** is an AI-powered structured code intelligence and learning system that analyzes GitHub repositories using deterministic static analysis and generates clear architectural explanations and personalized learning roadmaps.

This system is **not a generic chatbot**.

It is a layered architecture that separates:

- ✅ Deterministic structural analysis (FACT)
- 🟡 AI-generated explanations and recommendations (INFERENCE)

The goal is to help developers truly understand how real-world projects work.

---

## 🚩 Problem Statement

When developers open a GitHub repository, they often:

- Don’t know where execution starts
- Don’t understand how files are connected
- Cannot identify core vs utility modules
- Feel overwhelmed by project structure
- Don’t know which concepts they must learn

Most tools summarize code.  
They do not analyze architecture.

**CODEXPATH AI solves this gap.**

---

## 🎯 Core Objective

Transform any codebase into a structured technical mentor that:

- Explains how the system works
- Explains why it is structured that way
- Extracts real learning concepts from implementation
- Generates a personalized learning roadmap

---

## 🧠 System Architecture Philosophy

The system strictly separates responsibilities:

### ✅ Deterministic Layer (FACT-Based)

- Repository ingestion
- Language & framework detection
- AST-based parsing
- Dependency graph construction
- Entry point detection
- Concept extraction (rule-based pattern matching)

### 🟡 LLM Layer (INFERENCE-Based)

- Concept explanations
- Architectural reasoning
- Learning roadmap recommendations

> The LLM never directly analyzes raw code.  
> All structural understanding is deterministic.

---

## ⚙️ System Workflow

### 1️⃣ Repository Ingestion
- Accept GitHub URL or project upload
- Clone repository
- Filter irrelevant directories (`node_modules`, `.git`, `dist`, etc.)
- Generate structured file tree

---

### 2️⃣ Language & Framework Detection
- Detect languages via file extensions
- Parse configuration files:
  - `package.json`
  - `requirements.txt`
  - `pyproject.toml`
- Classify project type (Frontend / Backend / Full-stack / Library)

---

### 3️⃣ AST-Based Structural Analysis
- JavaScript parsed using Babel / TypeScript compiler
- Python parsed using Python `ast` module
- Extract:
  - Functions
  - Classes
  - Imports/Exports
  - API routes
  - Database connections

---

### 4️⃣ Dependency Graph Construction
- Build directed graph of file relationships
- Detect circular dependencies
- Identify entry points
- Calculate dependency depth

---

### 5️⃣ Concept Extraction Engine
Pattern-based detection of learning concepts.

Examples:

| Code Pattern | Detected Concept |
|--------------|-----------------|
| Express routes | REST APIs |
| JWT usage | Authentication |
| ORM models | Database abstraction |
| React hooks | Lifecycle management |
| try/catch blocks | Error handling |

Each concept is tagged as **FACT** and linked to specific file locations.

---

### 6️⃣ LLM Explanation Layer
- Uses Amazon Bedrock
- Generates structured explanations
- References actual file locations
- Output tagged as **INFERENCE**
- Never modifies factual analysis

---

### 7️⃣ Personalized Learning Roadmap
User provides:
- Skill level
- Goal
- Available time

System generates:
- Ordered learning modules
- Concept dependency order
- File references
- Realistic study progression

---

## 🏗️ Cloud Architecture (AWS)

- **API Gateway** – REST interface  
- **AWS Lambda** – Serverless compute  
- **Amazon S3** – Temporary repository storage  
- **DynamoDB** – Structured analysis data  
- **Amazon Bedrock** – LLM explanation layer  
- **CloudWatch** – Monitoring  
- **IAM** – Least privilege security model  

---

## 🔐 Security Principles

- Temporary repository storage (TTL-based cleanup)
- Encryption at rest and in transit
- Strict FACT vs INFERENCE tagging
- No raw code sent directly to LLM
- Least privilege IAM roles
- No long-term storage of private repositories

---

## 🚀 MVP Scope

Version 1 supports:

- JavaScript
- Python
- Small to medium repositories
- Beginner to intermediate explanation depth

---

## 📈 Long-Term Vision

Future enhancements may include:

- Enterprise onboarding mode
- Large-scale monorepo analysis
- Code quality scoring
- Refactoring suggestions
- Interactive architecture visualization
- CI/CD integration
