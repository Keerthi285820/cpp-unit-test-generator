# 🧪 C++ Unit Test Generator using AI (Ollama + YAML)

This project is part of the **Keploy API Fellowship Task 5**, where we build an **AI-powered unit test generator for C++ applications** using a local LLM (Ollama) and structured YAML prompts.

## 🚀 What It Does

- ✅ Accepts raw C++ code (e.g., `calculator.cpp`)
- 🧠 Sends it to a self-hosted LLM (LLaMA3 via Ollama)
- 📄 Uses YAML instruction files to generate accurate unit tests
- 🧪 Outputs Google Test-compatible `.cpp` test files
- 🔁 Refines based on feedback or build logs

## 📂 Project Structure

cpp-test-generator/
├── cpp_src/ # C++ source code (e.g., calculator.cpp)
├── tests/ # Generated test cases (e.g., test_calculator.cpp)
├── instructions/ # YAML prompts for LLM (e.g., initial_prompt.yaml)
├── scripts/ # Python script to generate unit tests
├── reports/ # Test coverage reports or notes
├── build_logs/ # Build output and error logs (if any)
└── README.md

## ⚙️ Technologies Used

- 🧠 [Ollama](https://ollama.com/) (local LLM runner)
- 💬 LLaMA 3 (used for generating unit tests)
- 🐍 Python (for automation)
- 📄 YAML (for structured prompts)
- 🧪 Google Test (for unit testing C++ code)

## 🛠️ How to Use

### 1️⃣ Place your C++ source file
Put your `.cpp` file (e.g., `calculator.cpp`) inside `cpp_src/`

### 2️⃣ Create a YAML instruction file
Define rules in `instructions/initial_prompt.yaml`

Example:
task: Generate Google Test cases
language: C++
constraints:
  - Use TEST macros
  - Avoid duplicate tests
  - Include necessary headers
3️⃣ Run the generator script

python scripts/generate_tests.py
This will:

Read the C++ file and YAML prompt

Call Ollama LLM with instructions

Save output in tests/test_<file>.cpp

✅ Sample Output
From: calculator.cpp
Generated: test_calculator.cpp

Includes tests like:

TEST(CalculatorTest, AddTwoPositiveNumbers) { ... }
TEST(CalculatorTest, DivideByZero) { ASSERT_THROW(...); }

📊 Test Coverage
Function	Test Cases
add()	✅ Covered
subtract()	✅ Covered
multiply()	✅ Covered
divide()	✅ Covered, with edge case

🙌 Acknowledgements
Thanks to Keploy for this amazing learning opportunity under the API Fellowship program!
Built with 💻 + 🧠 + ⚡

📬 Contact
Created by Keerthi Sri S
Feel free to connect on LinkedIn

