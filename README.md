# Intern Assessment – Judge Extraction Task

## Overview

You are required to build a **deterministic extraction system** to identify:

1. **bench** – All judges listed as part of the bench (coram/present/before).
2. **judge_final** – Judge(s) who authored/delivered the final judgment (may be one or more).

You must extract this information from the case reports provided.

---

## Input

- All input case reports will be placed inside the `data/` folder.
- There will be **4 case reports**.

Your program must automatically process all files inside the `data/` folder.

---

## Required Output

Your program must generate structured output in JSON format.

For each input file, produce:

{
  "source_file": "case1.pdf",
  "bench": ["Judge Name 1", "Judge Name 2"],
  "author_judge": ["Judge Name 1"],
  "evidence": {
    "bench": "Original extracted text snippet",
    "author_judge": "Original extracted text snippet"
  }
}

Output files may be:
- One JSONL file per input file, or
- A single combined JSONL file.

The output must be reproducible by running your script.

---

## Rules (Very Important)

1. ❌ No LLMs or Generative AI models.
   - No OpenAI, Anthropic, OpenRouter, Gemini, etc.
   - No AI-based extraction tools.
2. ❌ No manual editing of results.
3. ✅ Extraction must be done using deterministic methods such as:
   - Python
   - Regex
   - Rule-based parsing
   - Standard NLP libraries (non-generative)
4. ✅ All work must be included in a Git repository.
5. ✅ The project must include clear execution instructions in `README.md`.

---

## What We Are Evaluating

We will evaluate:

- Correctness of `bench` extraction
- Correctness of `author_judge` extraction
- Robust handling of formatting variations
- Code structure and clarity
- Reproducibility of results

---

## Environment Setup

This project uses **uv** for dependency management and execution.

Install uv if you do not already have it:

curl -Ls https://astral.sh/uv/install.sh | sh


or follow the official installation instructions:
https://docs.astral.sh/uv/

---

## Running the Extraction

Your repository must clearly include the commands required to run the extraction.

Example execution:

uv run main.py

or

uv run main.py --input_dir data --output output.json

All dependencies should be declared so that `uv` can automatically install them when running the project.

---

## Scaling Question (Conceptual)

In addition to implementation, answer the following question in your `README.md`:

> If this system needed to process 20,000+ case reports, some exceeding 300+ pages, how would you modify or optimize your approach to ensure scalability and performance?

This answer should be brief but technically sound.

---

## Submission Instructions

Send the following to:

admin@paralegal.lk

Include:

- Git repository link
- Your CV
- A cover letter
- Clear execution instructions in your repository

---

## Notes

- Your solution must run without manual intervention.
- Code quality and clarity matter.
- Make reasonable assumptions, but document them in your README.