
# human-alignment-pl-en-codeswitch

**Human-in-the-Loop Alignment for Polish-English Code-Switching Dialogues.**  
Training data and annotation guidelines for teaching AI to understand sarcasm, frustration, and humor — the way real humans actually speak.


##  Human-in-the-Loop Alignment

> “A programmer never asks why it works — it works, that’s enough.  
> Why it doesn’t? That’s the user’s question.”

This project explores how conversational AI handles **mixed-language dialogues (Polish-English)**, **sarcasm**, and **emotional tone** — the kind of natural communication real users produce when technology stops behaving as expected.

The goal is to simulate realistic **AI Training Data** for *human-in-the-loop alignment* — where people help AI models understand not just what is said, but what is meant.

---

## Objectives

- Model and annotate **code-switching** (PL/EN mix) in natural dialogues.  
- Capture **sarcastic, ironic, and emotional** user tones.  
- Evaluate how AI responses can remain empathetic, concise, and technically correct.  
- Provide **annotated examples** for prompt-tuning and RLHF evaluation.  



## Why It Matters

AI systems often misunderstand “imperfect” human speech — especially when languages mix or emotions rise.  
But that’s exactly when we need them to understand us the most.

This dataset trains conversational models to handle:
- frustration (“update again? really?”)  
- sarcasm (“oh great, now it works worse than before”)  
- humor and idioms  
- emotional context without losing technical accuracy  



## Data Format

All examples are stored in **JSONL (JSON Lines)** format — each line contains one dialogue sample and its evaluation fields.

**Example:**
```json
{"id":"cs-0001","user_utterance":"No i super, zrobili update i teraz upload nie działa. Great job, guys.","model_B":"That’s a known issue with voice mode. Turn off the mic, then tap ‘+’ → ‘Upload file’.","eval_pair_preference":"B","tone_user":["sarcastic","frustrated"],"intent":"report_bug"}
```


## Files Included

File	Description

README.md	Project overview and documentation
guidelines.md	Annotation and evaluation instructions
data/sample.jsonl	Sample dataset (Polish-English dialogues)
results/report.md	Evaluation summary and insights




 Data Card (Pilot)

Languages: Polish-English (code-switch)

Domain: UX frustration & conversational repair

Samples: 8 (pilot) — plan: 50 (v0.2), 100 + (v1.0)

Fields: user_utterance, intent, tone_user, model_A/B, eval_pair_preference, rationale, edit_best

Safety: de-identified, no personal data

License: MIT License




Example Use Cases

Evaluating AI model empathy in multilingual frustration contexts.

Improving RLHF datasets for mixed-language users.

Testing AI consistency when dealing with sarcasm or irony.



License

This project is released under the MIT License © 2025 M.E. Benderyszyn.


Project by M.E. Benderyszyn
Independent AI Writer & Researcher
