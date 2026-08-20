# Generative AI Response Evaluation Project

**Evaluator:** Benjamin Dickinson  
**Date:** August 16, 2026  
**Model evaluated:** OpenAI GPT-5.6-sol through OpenClaw  
**Sample size:** 10 responses

## Project objective

Evaluate generative-AI responses using a consistent four-part rubric: accuracy, instruction-following, clarity, and completeness. Identify unsupported claims, contradictions, calculation mistakes, formatting failures, and loss of source meaning; then recommend corrected responses.

## Method

Each response was scored from 1 (poor) to 5 (excellent) on four criteria:

- **Accuracy:** Factual and logical correctness
- **Instruction-following:** Compliance with explicit constraints
- **Clarity:** Readability and organization
- **Completeness:** Inclusion of necessary information

The evaluator reviewed each response before receiving reviewer feedback. Scores were supported with a written rationale and an improved response.

## Evaluation summary

| # | Test type | Accuracy | Instruction | Clarity | Completeness | Primary finding |
|---|---|---:|---:|---:|---:|---|
| 1 | Constraint following | 4 | 3 | 5 | 4 | All bullets exceeded the 10-word limit; one solution was omitted |
| 2 | Information extraction | 5 | 5 | 5 | 4 | “Broken” overstated the customer’s report that a switch did not work |
| 3 | Unsupported claims | 2 | 3 | 5 | 4 | Invented waterproofing, padded straps, comfort, and intended uses |
| 4 | Numerical reasoning | 3 | 5 | 5 | 5 | Tax was two cents low, producing an incorrect final total |
| 5 | Meaning preservation | 4 | 3 | 5 | 5 | Invented a refund and future expedited shipping request |
| 6 | Sentiment classification | 3 | 5 | 5 | 5 | Classified a predominantly negative message as neutral |
| 7 | Policy summarization | 2 | 2 | 5 | 5 | Invented a trial and contradicted cancellation and refund terms |
| 8 | Structured JSON output | 5 | 5 | 5 | 5 | Initial review missed invalid single quotes and trailing comma |
| 9 | Schedule consistency | 3 | 3 | 5 | 4 | Confused the event time with the required early-arrival time |
| 10 | Version-status reasoning | 2 | 2 | 5 | 5 | Mistook the newest beta for the latest stable release |

*The table preserves the evaluator’s initial scores. Reviewer notes in the full evaluation record document suggested score adjustments where relevant.*

## Key findings

Across the sample, the most common AI failure patterns were:

1. **Unsupported specificity:** The model converted uncertain or general source language into stronger claims, such as describing a nonworking switch as broken.
2. **Invented details:** The model added product features, refund terms, shipping benefits, or remedies absent from the source.
3. **Constraint failures:** Responses appeared polished while violating measurable requirements such as word limits or valid JSON syntax.
4. **Meaning changes:** Professional rewrites and summaries sometimes altered the requester’s intent.
5. **Reasoning errors:** The model carried a calculation mistake into the final total and confused “latest” with “latest stable.”
6. **Timeline confusion:** The model merged an event time with an early-arrival instruction.

## Evaluator strengths demonstrated

- Detected subtle overstatements and unsupported inferences
- Distinguished omissions from factual errors
- Checked calculations step by step rather than accepting plausible totals
- Compared outputs directly against source requirements
- Recognized when sentiment depended on severity and specificity, not simple keyword counting
- Revised judgments after learning exact technical requirements for JSON
- Explained errors clearly and proposed practical corrections

## Development area

The structured-output test showed that technical validation requires exact knowledge of the requested format. Future evaluations should include a short format-specific checklist—for example, verifying quotation marks, commas, schema, and whether extra Markdown is prohibited—before marking machine-readable output as valid.

## Conclusion

This project demonstrates entry-level capability in AI response evaluation, quality assurance, source-grounded fact checking, instruction compliance, and error documentation. The evaluator consistently identified material defects in fluent-looking responses and explained how to correct them without overstating his current technical experience.
