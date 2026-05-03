# LLM Comparative Study — Prompt Engineering for Academic Use

**By:** Kunal Chauhan | NMIMS Mukesh Patel School of Technology and Management, Mumbai  
**Period:** 2025 – 2026  
**Models Tested:** GPT-4 (ChatGPT), Google Gemini, Anthropic Claude

---

## Overview

This repository documents my hands-on comparative study of three major large language models (LLMs) — ChatGPT, Gemini, and Claude — evaluated across real academic use cases. The goal was to understand how different prompt strategies and model behaviours affect output quality, and to identify which models perform best for specific tasks.

All comparisons were made using the same or similar prompts across models.

---

## Use Cases Tested

1. Study notes generation and concept explanation
2. Exam study plan creation (with date constraints)
3. Diagram and visual explanation requests
4. Document and presentation (PPT) generation
5. Summary quality across varying response lengths

---

## Findings

### 1. Concept Explanation & Study Notes

**Task prompt used:**  
*"Explain [topic] to me in simple language. Teach me each concept step by step as if I'm a student learning it for the first time. Keep the language simple and vary the answer length based on complexity."*

| Model | Quality | Notes |
|-------|---------|-------|
| ChatGPT (GPT-4) | `●●●○○` 3/5 | Explanations are basic. Often requires 2–3 follow-up correction prompts to reach the desired depth. High iteration cost per session. |
| Gemini | `●●●○○` 3/5 | Performs reasonably but responses tend to be too short. Lacks depth for complex academic topics without explicit prompting. |
| Claude | `●●●●●` 5/5 | Best results on first or second prompt. Responses are well-structured, appropriately detailed, and easier to read as study material. |

**Key insight:** Claude required the least prompt iteration to produce usable study notes. GPT-4 required the most re-prompting, increasing time cost significantly.

---

### 2. Exam Study Plan Generation

**Task prompt used:**  
*"My exams are on [date]. Create a day-by-day study plan covering [subjects/topics]. Prioritise based on difficulty and time available."*

| Model | Quality | Notes |
|-------|---------|-------|
| ChatGPT (GPT-4) | `●●●○○` 3/5 | Generates a plan but it is generic. Does not adapt well to specific date constraints without additional prompting. |
| Gemini | `●●●○○` 3/5 | Similar to GPT — functional but not personalised. |
| Claude | `●●●●●` 5/5 | Produces structured, realistic plans that account for the actual days available. Output is directly usable. |

---

### 3. Diagram & Visual Explanation Requests

**Task prompt used:**  
*"Show me a diagram explaining [concept]."*

This was one of the most significant differentiators across models.

| Model | Quality | Notes |
|-------|---------|-------|
| ChatGPT (GPT-4) | `●●○○○` 2/5 | Cannot render diagrams inline. A completely separate prompt and tool (e.g. DALL-E) is required. Breaks the study workflow. |
| Gemini | `●●●○○` 3/5 | Attempts diagrams but output is heavily AI-generated in appearance and harder to interpret for academic understanding. |
| Claude | `●●●●○` 4/5 | Renders inline diagrams (SVG/visual) within the same chat. Quality is higher and more readable. Occasionally requires a second prompt, but the result is usable. |

**Key insight:** Workflow continuity matters. Models that require switching to a separate tool for diagrams introduce friction that reduces study efficiency.

---

### 4. Document & Presentation Generation

**Task prompt used:**  
*"Create a Word document / PowerPoint presentation on [topic] with proper structure, headings, and content."*

| Model | Quality | Notes |
|-------|---------|-------|
| ChatGPT (GPT-4) | `●●○○○` 2/5 | Document and PPT output is poor — basic formatting, minimal structure, not submission-ready. |
| Gemini | `●●○○○` 2/5 | Similar issues — documents lack proper formatting. Not reliable for academic submission. |
| Claude | `●●●●●` 5/5 | Produces well-structured, formatted documents and presentations. Output is closest to submission-ready with minimal editing. |

---

### 5. Summary Quality

**Task prompt used:**  
*"Summarise [topic/text] clearly. Vary the detail level — give a brief overview first, then a detailed breakdown."*

| Model | Quality | Notes |
|-------|---------|-------|
| ChatGPT (GPT-4) | `●●●○○` 3/5 | Summaries are functional but sometimes factually imprecise. Requires verification. |
| Gemini | `●●●○○` 3/5 | Summaries tend to be too short even when length is specified. |
| Claude | `●●●●●` 5/5 | Best summary quality. Handles the two-part structure (overview + detail) well without additional prompting. |

---

## Prompt Strategies That Worked Best

Through repeated experimentation, the following prompt patterns consistently improved output quality across all models:

1. **Role assignment** — *"Act as a teacher explaining this to a first-year student"* improved clarity significantly
2. **Explicit length guidance** — Specifying *"vary the length based on complexity"* produced better-calibrated responses than asking for "short" or "long"
3. **Constraint inclusion** — Adding real constraints like exam dates, subject names, and difficulty levels improved personalisation
4. **Staged prompting** — Breaking a complex request (e.g. full study plan + notes + diagrams) into sequential prompts improved accuracy over a single large prompt
5. **Correction prompting** — Explicitly stating what was wrong with the previous response (*"that was too basic, go deeper on X"*) was more effective than rephrasing the original prompt from scratch

---

## Limitations Observed

| Model | Key Limitation |
|-------|---------------|
| ChatGPT | High prompt iteration needed; no inline diagrams; occasional factual errors |
| Gemini | Responses too short by default; diagram quality poor; weaker document generation |
| Claude | Slower response time; fewer free-tier conversations per day compared to competitors |

---

## Conclusion

For academic use cases requiring study notes, exam planning, document generation, and visual explanations, **Claude consistently outperformed** the other models tested — requiring fewer corrective prompts and producing higher-quality first-pass output.

However, **rate limits and response speed** are real constraints for daily student use. A practical workflow might combine models: Claude for complex explanation and document tasks, others for quick lookups.

---

## What I Learned About Prompt Engineering

- Prompt quality directly determines output quality — the same question phrased differently can produce vastly different results
- Models respond differently to the same prompt; understanding each model's strengths is itself a skill
- Iteration cost (how many prompts it takes to get a usable result) is a real metric for evaluating LLM effectiveness
- Constraints and context in prompts (dates, roles, difficulty levels) dramatically improve output relevance

---

*This study is ongoing. New use cases and models will be added as tested.*
