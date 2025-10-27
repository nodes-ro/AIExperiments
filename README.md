# AI Experiments

Most large language models  **GPT-5**) are **not deterministic** by default.  
They include controlled randomness (often called *temperature*) in how responses are generated.  
This means even when you provide the **same prompt** under the **same conditions**, the model may produce **slightly different outputs**.

---

## Experiment 1 — Consistency Check

**Question:**  
> *Which number is larger: **27,483** or **27,482**?*

This seems trivial — but that's the point.  
If a model is consistent, it should always respond the same way.

The experiment tracks whether the model:
- Answers correctly  
- Uses consistent phrasing  
- Shows variation over time

| Variable | Value |
|--------|-------|
| Model | GPT-5 |
| Prompt | *"What is the largest number: 27483 or 27482?"* |
| Schedule | Automated once per day |
| Output Storage | Google Sheets |
| Display Method | Static webpage reading CSV feed |

---

## Method

We:
1. **Ask GPT-5 the exact same question daily, through an automated n8n workflow**
2. **Store each response** in a Google Sheet
3. **Automatically publish the results** to a lightweight webpage


---


## Live Results

See the webpage that loads the daily log directly from the experiment sheet.  
