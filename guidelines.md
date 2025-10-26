## 2. `guidelines.md`
```markdown
# Annotation Guidelines

## Purpose
These guidelines describe how to annotate and evaluate dialogues between users and AI models in the *Human-in-the-Loop Alignment* dataset.  



## Annotation Fields
Each record in `sample.jsonl` includes:

| Field | Description |
|--------|-------------|
| `id` | Unique sample ID |
| `user_utterance` | User input text |
| `intent` | Purpose of message (e.g., report_bug, ask_info, vent_emotion) |
| `tone_user` | Emotional tone (e.g., sarcastic, frustrated, humorous) |
| `model_A` / `model_B` | Two alternative AI responses |
| `eval_pair_preference` | Which response is better (A, B, or tie) |
| `eval_pair_rationale` | Short justification |
| `edit_best` | Final, improved response (gold standard) |



## Evaluation Criteria
1. **Understanding** – Did the AI grasp what the user actually meant?  
2. **Helpfulness** – Did it answer or solve the problem?  
3. **Empathy & Tone Matching** – Did it respond in a tone fitting the user’s emotion?  
4. **Accuracy & Brevity** – Was the response technically correct and concise?  
5. **Safety** – No personal data, bias, or unsafe advice.  



## Tone Tags
Use these tags to capture user emotion:
- `neutral`
- `frustrated`
- `sarcastic`
- `humorous`
- `disappointed`
- `playful`
- `urgent`



## Intent Tags
Possible user intents:
- `report_bug`
- `ask_info`
- `vent_emotion`
- `seek_workaround`
- `meta_comment`
- `smalltalk`



## Style Rules
- Always keep short, human-like sentences.  
- Acknowledge user emotion before giving steps.  
- Humor is acceptable if the user uses it first.  
- Never apologize mechanically (“I’m sorry you feel that way”) — rephrase naturally.  



Example rationale:
> *Model B wins: it recognized sarcasm, acknowledged frustration, and offered a clear workaround in three steps.*
