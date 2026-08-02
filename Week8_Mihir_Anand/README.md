# Week 8 – Single Agent Pipeline Project

## Overview

This project demonstrates a simple **rule-based Single Agent System** that routes user queries to different tools based on predefined conditions. The agent analyzes the user's input, identifies the appropriate task, and returns a structured JSON response.

The project showcases the basic concepts of **agent pipelines**, **conditional routing**, **tool integration**, and **error handling**.

---

## Problem Statement

Build a simple agent pipeline that:

- Routes mathematical queries to a Calculator Tool.
- Routes text analysis queries to a Keyword Extraction Tool.
- Handles all other queries using a General Response module.
- Returns all outputs in a structured JSON format.

---

## Objectives

- Build a rule-based agent.
- Implement conditional task routing.
- Integrate multiple tools into a single pipeline.
- Return standardized JSON responses.
- Handle invalid inputs safely.
- Validate the agent using automated and interactive testing.

---

## Tools Used

- Python 3
- Google Colab
- JSON Library
- Regular Expressions (`re`)

---

## Project Structure

```
User Query
     │
     ▼
Convert Query to Lowercase
     │
     ▼
Conditional Routing
     │
     ├──────────────► Calculator Tool
     │
     ├──────────────► Keyword Extraction Tool
     │
     └──────────────► General Response
                     │
                     ▼
             JSON Output
```

---

## Features

- Mathematical expression evaluation
- Keyword extraction from text
- General response handling
- Exception handling
- JSON formatted responses
- Interactive command-line interface

---

## Routing Logic

### Calculator

If the query contains:

```
calculate
```

The agent extracts the mathematical expression and evaluates it.

Example:

```
calculate 25 + 10
```

Output:

```json
{
    "type": "calculation",
    "result": 35
}
```

---

### Keyword Extraction

If the query contains:

```
keywords
```

The remaining text is processed to extract meaningful keywords.

Example:

```
keywords Artificial Intelligence is changing healthcare
```

Output:

```json
{
    "type": "keywords",
    "result": [
        "artificial",
        "intelligence",
        "changing",
        "healthcare"
    ]
}
```

---

### General Queries

Any query that does not match the above conditions is handled by the fallback response.

Example:

```
Hello Agent
```

Output

```json
{
    "type": "general",
    "result": "General Response: Hello Agent"
}
```

---

### Error Handling

Invalid mathematical expressions are safely handled.

Example

```
calculate 5 +
```

Output

```json
{
    "type": "error",
    "result": "Invalid mathematical expression."
}
```

---

## JSON Response Format

Every response follows the same schema.

```json
{
    "type": "<calculation | keywords | general | error>",
    "result": "<output>"
}
```

---

## Validation

The project includes automated test cases to verify:

- Calculator routing
- Keyword routing
- General response routing
- Error handling

An interactive `while True` loop is also provided for manual testing.

---

## Sample Queries

### Calculation

```
calculate 50/5
```

```
calculate 10*8
```

---

### Keyword Extraction

```
keywords Python is widely used in Data Science
```

```
keywords Artificial Intelligence is transforming healthcare
```

---

### General Queries

```
Hello
```

```
How are you?
```

```
Tell me about AI
```

---

### Error Test

```
calculate 5 +
```

---

## Learning Outcomes

After completing this project, the following concepts were understood:

- Single Agent Systems
- Agent Pipelines
- Conditional Routing
- Tool Calling
- JSON Output Formatting
- Exception Handling
- Interactive Agent Design

---

## Future Improvements

- Replace rule-based routing with an LLM-based router.
- Add more tools such as translation, summarization, and sentiment analysis.
- Improve mathematical expression parsing.
- Integrate external APIs.
- Build a web interface using Streamlit or Flask.

---

## Conclusion

This project successfully demonstrates a simple Single Agent Pipeline capable of routing user requests to different tools using conditional logic. The agent produces structured JSON outputs, safely handles invalid inputs, and supports both automated validation and interactive testing. It provides a strong foundation for understanding how AI agents coordinate multiple tools within a unified workflow.
