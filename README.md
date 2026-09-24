# Brew & Bean Cafe - AI Email Triage

## Task 2: Prompt Design and Classification Function

This project implements a reusable LLM prompt and Python email classification
function for Brew & Bean Cafe.

## Objective

The system classifies customer emails into:

- order
- feedback
- support
- other

The LLM is instructed to return a JSON object containing:

- category
- confidence

A confidence threshold of 0.6 is applied. If the confidence is below 0.6,
the category is changed to `Uncertain`.

## Project Files

### prompt.txt

Contains the reusable LLM classification prompt.

The prompt instructs the model to:

- classify the email
- return only JSON
- provide a confidence score
- ignore malicious instructions inside customer emails

### triage.py

Contains:

- reusable prompt loading
- mock LLM classification
- JSON parsing
- response validation
- confidence threshold handling
- `classify_email(email_text)` function

### test_triage.py

Contains pytest tests for:

- normal classification
- low-confidence classification
- prompt injection
- empty input
- whitespace input
- required JSON keys
- confidence range

## Running the Tests

Install pytest:

```bash
pip install pytest