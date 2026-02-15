# 🧪 Week 3 – Prompt Experiments
## Testing Prompt Strategies & Model Behavior

This document records structured experiments conducted to analyze prompt performance and output quality.

---

#  Experiment 1 – Open-Ended Prompt

Prompt:
Explain embeddings.

Result:
- General explanation
- Broad response
- No structured format

Insight:
Unstructured prompts lead to generic outputs.

---

#  Experiment 2 – Structured Output Format

Prompt:
Explain embeddings.
Return the response in JSON with:
{
  "definition": "",
  "advantages": [],
  "applications": []
}

Result:
- Organized response
- Easy to parse
- Clear structure

Insight:
Specifying format improves clarity and usability.

---

#  Experiment 3 – Information Extraction

Input:
"Anita paid 1500 rupees for 3 tickets."

Prompt:
Extract structured information in JSON.

Output:
{
  "customer": "Anita",
  "quantity": 3,
  "amount": 1500
}

Insight:
LLMs are effective for converting text into structured data.

---

#  Experiment 4 – Sentiment Classification

Prompt:
Classify sentiment as Positive, Neutral, or Negative.

Text:
"This service is disappointing."

Result:
Negative

Insight:
LLMs perform well in text classification tasks.

---

#  Experiment 5 – Context-Grounded Response

Prompt:
Answer only using the provided document context.

Observation:
- Reduced hallucination
- More accurate references
- Higher reliability

Insight:
Context grounding improves trustworthiness.

---

#  Experiment 6 – Prompt Length Comparison

Compared:

- Detailed long prompt
- Short structured prompt

Observation:
Short structured prompt used fewer tokens and gave similar clarity.

Insight:
Concise prompts can be more cost-efficient.

---

#  Experiment 7 – Vision Model Evaluation

Prompt:
Describe the objects and actions in the image.

Observation:
- Object detection
- Context explanation
- Scene understanding

Insight:
Vision models enable multimodal AI applications.

---

#  Key Conclusions

From all experiments:

- Prompt structure affects output quality
- Format instructions increase reliability
- Context improves factual grounding
- Token efficiency reduces cost
- Evaluation is necessary for stable systems

Prompt engineering is both an art and a systematic process.

---

## 🎉 Prompt Experiment Log Completed 🎉
