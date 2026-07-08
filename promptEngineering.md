# Assignment 4 – Prompt Engineering Experiments

**Name:** Sheezah Humayun  
**Track:** NLP & AI Agents  
**Week:** 1  
**Course:** Visibility Bots Innovation Lab – AI Summer Internship 2026

---

# Introduction

Prompt engineering is the process of designing prompts that guide Large Language Models (LLMs) to generate accurate, structured, and useful responses. Different prompting techniques can significantly improve the quality of AI-generated outputs. This report demonstrates five commonly used prompting strategies through practical experiments.

---

# Experiment 1 – Role Prompting

## Objective

Assign a specific role to the AI so it responds from the perspective of an expert.

### Prompt

```
You are an experienced software engineering mentor.

Explain REST APIs to a second-year Computer Science student using simple language and practical examples.
```

### Output

REST (Representational State Transfer) APIs allow different software applications to communicate over the internet. Think of a restaurant: the customer sends an order, the waiter delivers it to the kitchen, and the kitchen returns the food. Similarly, a client sends an HTTP request, the server processes it, and returns a response.

Common HTTP methods include:

- GET → Retrieve data
- POST → Create data
- PUT → Update data
- DELETE → Remove data

REST APIs are widely used in web and mobile applications because they are simple, scalable, and language-independent.

### Observations

- The AI responded like a teacher.
- The explanation was beginner-friendly.
- Practical analogies improved understanding.

### Improvements

Specify the audience and desired complexity level to receive more targeted explanations.

---

# Experiment 2 – Chain-of-Thought Prompting

## Objective

Encourage the model to reason through a problem before producing the final answer.

### Prompt

```
A student studies 3 hours every weekday and 6 hours every weekend day.

Calculate how many hours they study in one week.
Think through the calculation step by step before giving the final answer.
```

### Output

Weekdays:

- 5 × 3 = 15 hours

Weekend:

- 2 × 6 = 12 hours

Total:

15 + 12 = **27 hours**

### Observations

- The AI clearly explained every calculation.
- Intermediate reasoning reduced the chance of mistakes.
- The final answer became easier to verify.

### Improvements

Request numbered reasoning steps when solving longer mathematical or logical problems.

---

# Experiment 3 – Few-Shot Prompting

## Objective

Provide examples so the model learns the expected response format.

### Prompt

```
Convert the following sentences into professional email subjects.

Examples:

Input: Meeting tomorrow
Output: Meeting Reminder for Tomorrow

Input: Job application
Output: Application for Software Developer Position

Now convert:

Input: Internship update
```

### Output

**Internship Progress Update**

### Observations

- The examples established the desired style.
- The output matched the format of previous examples.
- Few-shot prompting improved consistency.

### Improvements

Provide more examples when dealing with complex formatting tasks.

---

# Experiment 4 – Structured Output (JSON)

## Objective

Generate machine-readable structured data.

### Prompt

```
Return the following student information as JSON only.

Name: Ali Khan
University: FAST-NUCES
Semester: 6
Skills:
- Python
- React
- SQL
```

### Output

```json
{
  "name": "Ali Khan",
  "university": "FAST-NUCES",
  "semester": 6,
  "skills": [
    "Python",
    "React",
    "SQL"
  ]
}
```

### Observations

- The response followed valid JSON syntax.
- No unnecessary explanations were included.
- Structured outputs are useful for APIs and automation.

### Improvements

Specify "Return only valid JSON" to prevent additional text.

---

# Experiment 5 – Prompt Optimization

## Objective

Compare a vague prompt with an optimized prompt.

### Initial Prompt

```
Explain Python.
```

### Initial Output

Python is a programming language used for many different applications including web development, automation, data science, and artificial intelligence.

---

### Optimized Prompt

```
You are a programming instructor.

Explain Python to a beginner in less than 150 words.

Include:
- What Python is
- Three common uses
- One simple code example
- Use simple language.
```

### Optimized Output

Python is a beginner-friendly programming language known for its simple syntax. It is commonly used for:

- Web Development
- Artificial Intelligence
- Automation

Example:

```python
print("Hello, World!")
```

Python is popular because it is easy to learn, has a large community, and supports many powerful libraries.

### Observations

- The optimized prompt produced a more focused response.
- Output length was controlled.
- The explanation became clearer and more useful.

### Improvements

Including role, audience, format, constraints, and expected output consistently produces higher-quality responses.

---

# Conclusion

These experiments demonstrate that prompt engineering has a significant impact on the quality of AI-generated responses. Techniques such as role prompting, chain-of-thought reasoning, few-shot prompting, structured output, and prompt optimization improve clarity, accuracy, consistency, and usability. Effective prompt design is an essential skill for developing reliable AI applications and intelligent agents.
