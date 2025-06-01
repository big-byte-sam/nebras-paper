# Candidate Answer Generation Agent Prompt

## Arabic Prompt (used by the agent)
```python
prompt = """أجب عن السؤال التالي.
إذا كان السؤال يتعلق بموضوعات إسلامية أو فتاوى، يجب أن تكون الإجابة دون استخدام آيات قرآنية أو أحاديث نبوية.
كما يجب أن تكون الإجابة باللغة العربية.
---
السؤال:
{question}
"""
```

## Translated to English
```python
prompt = """Answer the following question
If the question is related to Islamic topics or fatwas, the answer must be given without using Qur'anic verses or Hadiths. The answer must also be in Arabic.
---
Question:
{question}
"""
```