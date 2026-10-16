# Turn Finance Data into a Clear Story with Copilot

**A 60-minute, beginner-friendly hands-on lab for finance professionals**

## Lab purpose

Finance professionals are often handed a table, report, or export and asked to explain what happened, why it matters, and what should happen next. Copilot can accelerate that work, but only when the user gives it a clear business question, enough context, a defined output, and explicit review rules.

In this lab, you will use Copilot as an **analysis partner**, not as an unquestioned answer engine. You will practice a repeatable workflow for understanding a finance dataset, asking a focused question, improving the presentation, drafting a concise narrative, challenging the response, and documenting what still requires human review.

The exercises are designed for a new Copilot user. Every activity includes a prompt to try, an explanation of why it works, an expected output, and a checkpoint before moving forward.

> **Professional judgment remains essential.** Verify calculations, classifications, assumptions, source data, confidentiality, and conclusions before using AI-assisted work in financial reporting, tax, payroll, treasury, forecasting, operational decisions, or management communications.

## Lab at a glance

| Item | Description |
| --- | --- |
| **Time** | 60 minutes |
| **Experience level** | New to Copilot |
| **Audience** | Tax, Accounting, ERP Systems, FP&A, Accounts Payable, Treasury, and Payroll |
| **Working format** | Individual work with brief pair or group discussion |
| **Primary deliverable** | One decision-ready finance analysis with a supporting table or visual recommendation |
| **Validation deliverable** | A documented list of checks, limitations, assumptions, and next actions |
| **Reusable takeaway** | A finance prompt that can be adapted to a recurring task |

## Learning objectives

By the end of the lab, you will be able to:

1. Explain the four building blocks of a strong finance prompt: **goal, context, output, and guardrails**.
2. Ask Copilot to describe a dataset's purpose, fields, period, and level of detail.
3. Identify data-quality issues that could make an analysis incomplete or misleading.
4. Turn a broad request into one focused business question.
5. Select a table or visual based on the audience's decision need.
6. Create a concise management summary, Actual-versus-Forecast analysis, or transparent baseline forecast approach.
7. Improve a weak response through follow-up prompts instead of starting over.
8. Separate confirmed observations, assumptions, possible causes, and recommendations.
9. Review AI-assisted work for calculation, classification, confidentiality, and interpretation risks.
10. Save a reusable prompt and explain where human judgment is still required.

## What you need

- A finance dataset open in a Copilot-enabled analysis experience.
- At least one descriptive field, such as **Account**, **Category**, **Business Unit**, **Department**, **Vendor**, **Jurisdiction**, or **Tax Type**.
- A time field, such as **Month**, **Period**, or **Date**.
- At least one numeric field. **Actual** and **Forecast** are helpful but not required.
- A place to copy prompts and record your final result.
- An approved environment appropriate for the sensitivity of the data.

If your assigned dataset is unavailable, use an approved practice dataset with a category, a period, and at least one numeric measure. If your column names differ from the examples, substitute the actual names from your dataset.

## Suggested practice data shape

| Period | Business Unit | Account or Category | Actual | Forecast |
| --- | --- | --- | ---: | ---: |
| Jan | North | Revenue | 125,000 | 120,000 |
| Jan | North | Payroll Expense | 42,000 | 40,000 |
| Jan | South | Revenue | 98,000 | 105,000 |

This small table illustrates a usable structure only. Do not replace values in an assigned dataset with these sample values.

## The beginner workflow

Use the same six-stage workflow whenever you ask Copilot to help with finance data:

1. **Frame** — State the business goal, audience, requested output, and review rules.
2. **Understand** — Confirm what the data represents and what one row means.
3. **Inspect** — Identify data-quality issues and missing definitions.
4. **Analyze** — Perform one focused comparison, trend, exception, or forecast task.
5. **Challenge** — Ask what may be wrong, unsupported, incomplete, or confidential.
6. **Communicate** — Put the verified result, limitation, and next action first.

## 60-minute agenda

| Time | Activity | Participant outcome |
| --- | --- | --- |
| **0–5 minutes** | Orient to the workflow and choose a question | A clear decision or audience need |
| **5–13 minutes** | Build a strong finance prompt | A complete four-part prompt |
| **13–23 minutes** | Map and inspect the dataset | A data map and list of open definitions |
| **23–33 minutes** | Scan quality and select an analysis question | A focused, answerable question |
| **33–45 minutes** | Complete an analysis and presentation path | A draft table, visual recommendation, and narrative |
| **45–54 minutes** | Challenge, correct, and validate | A revised result with documented limitations |
| **54–60 minutes** | Report out and save a reusable prompt | A 60-second explanation and reusable template |

---

# Part 1 — Orient and choose a useful question (0–5 minutes)

## Why this step matters

A table is not a business question. Before asking Copilot to analyze anything, identify who needs the answer and what decision, review, or conversation the answer should support.

## Activity 1A — Identify the audience and decision

Complete these statements:

```text
The primary audience is: ______________________________________

They need to decide, review, explain, or monitor: ______________

The time period or comparison that matters is: _________________

A useful answer would help them: _______________________________
```

Examples of focused needs include:

- Explain the largest Actual-versus-Forecast differences to a finance leader.
- Identify transactions or balances that require reconciliation.
- Find vendor, category, or business-unit exceptions that need review.
- Assess whether historical data supports a simple baseline forecast.
- Improve a dense report so the main message is easier to understand.

## Beginner checkpoint

Your question is ready when it names:

- **One audience**;
- **One primary business need**;
- **One time period or comparison basis**; and
- **One expected action**, such as review, investigate, explain, prioritize, or decide.

If the question contains several unrelated goals, choose the one that would be most useful in the next meeting or review.

## Facilitator cue

Ask two participants to share their questions. Point out the difference between a topic such as “expenses” and a decision-focused question such as “Which expense categories account for the largest unfavorable Forecast variance this quarter?”

---

# Part 2 — Build a strong finance prompt (5–13 minutes)

## The four-part prompt pattern

New users often begin with a short instruction such as “Analyze this data.” The response may sound reasonable, but Copilot does not automatically know the business purpose, audience, output format, or review rules.

| Prompt element | Question it answers | Finance example |
| --- | --- | --- |
| **Goal** | What are you trying to accomplish? | Identify the largest Actual-versus-Forecast differences |
| **Context** | What should Copilot understand? | Each row represents one account, business unit, and month |
| **Output** | What should the answer look like? | Return a ranked table and a five-bullet summary |
| **Guardrails** | What should Copilot verify or avoid? | Show formulas, use exact figures, and do not invent causes |

## Activity 2A — Compare weak and strong prompts

**Weak prompt**

```text
Analyze this data and tell me what is important.
```

**Stronger prompt**

```text
Goal: Identify the most decision-relevant results in this finance dataset.

Context: Treat each row according to the dataset's actual level of detail. Use the existing field names and values. The audience is a finance manager reviewing the period.

Output: Provide a five-bullet executive summary and a ranked table of the five largest movements.

Guardrails: Use exact figures, show how rankings were determined, separate confirmed observations from possible explanations, and state any data limitations.
```

### Discuss for one minute

What information did the stronger prompt add? Which addition is most likely to improve the response?

## Activity 2B — Write your first complete prompt

```text
Goal: I need to ________________________________________________.

Context:
- Audience: ____________________________________________________
- The data represents: _________________________________________
- One row appears to represent: ________________________________
- Period or comparison basis: __________________________________

Output:
- Return the result as: ________________________________________
- Limit or organize the response by: ___________________________

Guardrails:
- Verify: ______________________________________________________
- Flag: ________________________________________________________
- Do not: ______________________________________________________
```

## Activity 2C — Improve one ambiguous phrase

Look for words such as **important**, **significant**, **unusual**, **best**, **large**, or **bad**. Replace at least one with a measurable instruction.

| Ambiguous phrase | More testable instruction |
| --- | --- |
| Find large variances | Rank by absolute variance amount and show variance percentage |
| Show unusual items | Identify values outside the normal range and explain the rule used |
| Create a good chart | Recommend one chart that answers the selected business question |
| Summarize the data | State the period, comparison basis, top result, limitation, and next action |

## Expected output

A complete prompt that another person could understand without hearing your verbal explanation.

## Beginner checkpoint

Before submitting the prompt, confirm that it:

- [ ] Asks one primary business question.
- [ ] Identifies the intended audience.
- [ ] States the period or comparison basis.
- [ ] Defines the requested format and level of detail.
- [ ] Includes at least one calculation, review, or “do not” instruction.
- [ ] Does not ask Copilot to invent explanations that are absent from the data.

---

# Part 3 — Understand and inspect the dataset (13–23 minutes)

## Why this step matters

An analysis can be mathematically correct and still be misleading if the user misunderstands what one row represents, mixes monthly and cumulative values, overlooks missing periods, or treats a label as a confirmed business definition.

## Activity 3A — Create a data map

Submit this prompt:

```text
Review this dataset and explain it to a new finance user.

Create a data map that identifies:
1. The apparent purpose of the dataset
2. What one row appears to represent
3. Each important descriptive field and numeric measure
4. The time period and level of detail
5. Which fields can support trends, comparisons, exceptions, or variance analysis
6. Any field whose meaning cannot be confirmed from the data alone

Use the actual column names. Separate confirmed observations from assumptions. Do not change the data.
```

## Activity 3B — Test the dataset grain

“Grain” means the level of detail represented by one row. Examples include one row per invoice, account-period, employee-pay-period, entity-month, or vendor-category combination.

Use this follow-up:

```text
Recheck the level of detail.

Identify the combination of fields that appears to make a row unique. Show any duplicate-looking combinations. If uniqueness cannot be confirmed, explain what definition or identifier is missing.
```

## Review the response

Ask yourself:

- Did Copilot correctly identify what one row represents?
- Did it distinguish descriptive dimensions from numeric measures?
- Did it accurately describe the period covered?
- Did it confuse a transaction amount, period balance, and cumulative balance?
- Did it make an assumption about an unfamiliar field?
- Could two rows represent the same transaction, balance, or category-period?

## Activity 3C — Create a field-definition log

Record unresolved fields before analysis:

| Field or term | What Copilot inferred | What must be confirmed | Owner or evidence needed |
| --- | --- | --- | --- |
| Example: Forecast | Approved plan | Whether this is plan or current outlook | FP&A owner or report definition |
|  |  |  |  |
|  |  |  |  |

## Expected output

- A short description of the dataset;
- A proposed definition of one row;
- A list of measures and dimensions;
- A list of definitions that still require confirmation.

## Beginner checkpoint

Do not continue until you can explain, in one sentence, what one row represents. If you cannot, carry that uncertainty into the final limitations section.

---

# Part 4 — Scan quality and select an analysis question (23–33 minutes)

## Activity 4A — Run a data-quality scan

```text
Inspect the dataset for issues that could affect analysis.

Check for:
- Blank or missing values
- Duplicate-looking records
- Inconsistent category, account, vendor, or business-unit labels
- Unexpected signs or number formats
- Missing or partial periods
- Zero, blank, or negative comparison values
- Unusually large or small values
- Totals mixed with detail rows
- Values that may contain confidential or employee-level information

Return a table with:
1. Issue
2. Affected field or record
3. Why it matters
4. Recommended review step
5. Whether analysis can continue before the issue is resolved

Do not silently correct, remove, or replace any data.
```

## Activity 4B — Classify the issues

Place each issue into one of three categories:

| Classification | Meaning | Example response |
| --- | --- | --- |
| **Stop** | The issue may invalidate the requested analysis | Confirm whether values are monthly or cumulative before totaling them |
| **Proceed with caution** | Analysis can continue if the limitation is disclosed | One business unit is missing the latest period |
| **Document only** | The issue does not change the current calculation but should be noted | Two category labels use different capitalization |

## Activity 4C — Generate answerable business questions

```text
Based only on fields available in this dataset, propose five finance questions that the data can answer.

For each question, identify:
- The relevant fields
- The calculation or comparison required
- The best output format
- One definition or limitation that should be confirmed
- The likely audience or decision supported

Do not propose a question that requires data not present in the dataset.
```

## Select one question

Score each proposed question from 1 to 3:

| Criterion | 1 | 2 | 3 |
| --- | --- | --- | --- |
| **Answerable** | Key data is missing | Some assumptions are needed | Available fields directly support it |
| **Useful** | Interesting but not actionable | Supports discussion | Supports a clear review or decision |
| **Verifiable** | Logic is difficult to reproduce | Some calculations can be checked | Calculations and source rows can be traced |

Choose the question with the strongest combined score. Do not use the score as a substitute for professional judgment.

## Expected output

One focused question that the available data can answer, plus a short list of data issues and definitions that must accompany the result.

---

# Part 5 — Analyze and improve the presentation (33–45 minutes)

Choose **one** path. The goal is not to complete every prompt; it is to practice the full cycle of requesting, reviewing, and improving one useful result.

## Path A — Create a concise management summary

Choose this path when the immediate need is to communicate the main message.

### Initial prompt

```text
Summarize this dataset for a finance leader in no more than five bullets.

Include:
- The most important verified result
- The largest positive and negative movements
- A notable trend, exception, or concentration
- One data-quality or interpretation limitation
- One recommended follow-up

Use exact figures from the dataset. State the period and comparison basis. Do not speculate about causes that are not supported by the data.
```

### Review the first draft

Mark any sentence that:

- Uses “significant,” “large,” or “material” without a number or threshold;
- Describes a result without its comparison basis;
- Presents an assumed cause as a fact;
- Includes detail that does not change a decision;
- Omits the period, unit, or relevant category;
- Combines several messages in one bullet.

### Improvement prompt

```text
Revise the summary for clarity and precision.

Quantify vague statements, identify the comparison basis, remove repetition, and label unsupported explanations as questions for investigation. Put the most decision-relevant finding first. End with a specific next action and the evidence needed.
```

### Success test

A reader can understand the result, limitation, and next action in under one minute.

---

## Path B — Analyze Actual versus Forecast

Choose this path when the dataset contains comparable **Actual** and **Forecast** values.

### Initial prompt

```text
Analyze Actual versus Forecast using this dataset.

For each relevant category, calculate:
- Variance amount = Actual minus Forecast
- Variance percentage = (Actual minus Forecast) divided by Forecast
- Absolute variance amount for ranking

Then:
1. Rank the largest absolute variances
2. Identify the three items that deserve investigation
3. Label a variance as favorable or unfavorable only when the business meaning is clear
4. Write a concise narrative that separates observed results from possible causes

Show the formulas used. Flag zero, blank, or negative Forecast values that require special handling. Preserve the source signs.
```

### Add a review threshold

Use an approved threshold supplied by the facilitator or organization. If none is available, practice the prompt structure without presenting the example as policy.

```text
For this exercise, highlight an item when it exceeds either [dollar threshold] or [percentage threshold].

Return a table containing category, Actual, Forecast, variance amount, variance percentage, threshold result, and a short review note. Recalculate percentages from the underlying values rather than adding percentage rows.
```

### Improve the narrative

```text
Rewrite the top three variance explanations using this structure:

[Category]: [amount and percentage] versus Forecast for [period].
Observed result: [what the data confirms].
Possible driver to investigate: [question or hypothesis, not a stated fact].
Next step: [specific owner, evidence, or analysis needed].

Do not use “timing,” “one-time,” “mix,” or “volume” unless the dataset or added context supports that explanation.
```

### Important interpretation note

A positive variance is not automatically favorable. Higher revenue may be favorable and higher expense may be unfavorable, while balance-sheet, tax, treasury, payroll, and operational measures require additional business context.

---

## Path C — Explore a transparent baseline forecast

Choose this path when the dataset contains several comparable historical periods.

### Assess suitability first

```text
Assess whether this dataset is suitable for a simple baseline forecast.

Identify:
- The available time range and number of periods
- Missing or partial periods
- Unusual values that could distort a forecast
- Visible trend or seasonality
- Changes in categories or business structure
- Important factors not captured in the dataset

Conclude whether a baseline forecast is reasonable, conditionally reasonable, or not supported. Explain why. Do not generate forecast values yet.
```

### Compare simple methods

```text
Compare up to three transparent baseline forecasting methods that fit this dataset, such as:
- Recent-period average
- Growth-rate trend
- Seasonal pattern

For each method, explain the calculation, required history, strengths, weaknesses, and when it could mislead. Recommend one method, but do not produce forecast values until the assumptions are stated.
```

### Create and challenge the baseline

```text
Using the selected method, produce a clearly labeled baseline forecast.

Keep historical Actuals separate from forecast periods. Show the calculation, assumptions, and limitations. Then identify two business scenarios that could make the result higher or lower without inventing specific impacts.
```

### Success test

A reviewer can understand and reproduce the method without relying on “the AI predicted it.”

---

## Presentation activity — Choose one visual and one supporting table

After completing your selected analysis path, submit:

```text
Using the selected business question and analysis, recommend one visual and one supporting table.

For the visual, specify:
- Chart type
- Category and value fields
- Sort order
- Recommended title
- What the audience should notice first
- One reason this chart could be misleading if used incorrectly

For the table, specify:
- Required columns
- Column order
- Number formats
- Useful filter or conditional-formatting rule
- Which rows should be traceable to source detail

Keep the design professional and simple. Do not add measures that cannot be calculated from the available fields.
```

### Visual selection guide

| If the audience needs to see… | Consider… | Avoid when… |
| --- | --- | --- |
| Performance over time | Line chart | Periods are missing or not comparable |
| Actual versus Forecast by category | Clustered bar or column chart | There are too many categories to read |
| Drivers from Forecast to Actual | Waterfall or bridge chart | The drivers do not reconcile to the total |
| Contribution or concentration | Sorted bar chart | Categories overlap or do not form comparable groups |
| Exceptions requiring action | Filtered table with conditional formatting | The goal is a high-level trend |

## Beginner checkpoint

Before moving on, you should have:

- [ ] One answer to the selected business question;
- [ ] One supporting calculation or comparison;
- [ ] One visual recommendation;
- [ ] One supporting table recommendation;
- [ ] One clearly stated limitation;
- [ ] At least one source row, total, or formula you can independently check.

---

# Part 6 — Challenge, correct, and validate (45–54 minutes)

## Activity 6A — Add role-specific context

Add the instruction that best matches your role:

| Role | Add this instruction |
| --- | --- |
| **Tax** | Group results by tax type or jurisdiction where available, and do not infer tax treatment from account labels alone. |
| **Accounting** | Preserve account classifications and signs, and identify items that may require reconciliation or supporting detail. |
| **ERP Systems** | Focus on data structure, field consistency, mapping issues, lineage, and whether the analysis can be repeated. |
| **FP&A** | Prioritize material Actual-versus-Forecast drivers, trend implications, and whether assumptions or the forecast should be updated. |
| **Accounts Payable** | Focus on vendors, spend categories, timing, exceptions, and possible duplicate or unusual payments. |
| **Treasury** | Focus on cash timing, liquidity, concentration, and forecast accuracy without assuming all cash movements are operational. |
| **Payroll** | Focus on headcount, rate, timing, bonus, benefit, tax, and department drivers while protecting employee-level confidentiality. |

Also add at least one definition known to you:

- Whether the period is complete;
- Whether values are monthly, quarter-to-date, year-to-date, or cumulative;
- Whether Forecast means approved plan, current outlook, or another comparison;
- What “favorable” means for the selected measure;
- Whether a category contains confidential information;
- Whether totals include eliminations, allocations, or adjustments.

## Activity 6B — Ask Copilot to challenge the work

```text
Act as a skeptical finance reviewer.

Identify:
1. Any conclusion not directly supported by the dataset or provided context
2. Any calculation, sign, total, or denominator that needs to be checked
3. Any favorable or unfavorable label that depends on business interpretation
4. Any category definition, period, unit, or comparison basis that remains unclear
5. Any confidential or employee-level detail that should be removed or aggregated
6. Any important alternative interpretation
7. Any evidence needed before someone acts on the result

Do not defend the existing answer. Focus on what could be wrong, incomplete, overstated, or misleading.
```

## Activity 6C — Independently check one result

Choose one important number and document the check:

```text
Result checked: ________________________________________________
Source rows or values used: ____________________________________
Formula or reconciliation: _____________________________________
My independently calculated result: _____________________________
Copilot result: ________________________________________________
Difference, if any: _____________________________________________
Action taken: __________________________________________________
```

## Activity 6D — Correct and document the result

```text
Revise the analysis using the review findings and the independently checked result.

At the end, add a section titled “Validation and limitations” containing:
- Calculations checked
- Business definitions confirmed
- Assumptions still open
- Data-quality limitations
- Confidentiality considerations
- Recommended human review

Do not state that the analysis is validated if any listed check was not performed.
```

## Human review checklist

- [ ] The dataset, period, unit, and comparison basis are correctly identified.
- [ ] One row's level of detail is understood or disclosed as uncertain.
- [ ] All stated figures can be traced to the dataset.
- [ ] At least one important figure was independently recalculated.
- [ ] Formulas, signs, and denominators are correct.
- [ ] Totals and percentages are calculated appropriately.
- [ ] Zero, blank, and negative comparison values received appropriate treatment.
- [ ] Favorable or unfavorable labels match the business meaning.
- [ ] Observations are separated from hypotheses and recommendations.
- [ ] Confidential details have been removed or appropriately aggregated.
- [ ] The output states material limitations and open assumptions.
- [ ] A qualified owner will review the analysis before use.

## Expected output

A corrected analysis that explicitly states what is confirmed, what remains uncertain, and what a human reviewer must do next.

---

# Part 7 — Report out and capture a reusable prompt (54–60 minutes)

## Activity 7A — Prepare a 60-second report-out

```text
We used Copilot to [describe the business question].

The most important verified finding was [result and comparison basis].

We improved the reporting by [visual, table, summary, variance, or forecast improvement].

Copilot initially [describe one weakness, unsupported assumption, or unclear answer].

We corrected it by [adding context, using a follow-up prompt, checking a formula, or defining a business term].

Before using the result, the next human review is [specific follow-up].
```

## Activity 7B — Pair discussion

Discuss these questions with another participant:

1. Did you use the same data to answer different business questions?
2. Which prompt instruction produced the biggest improvement?
3. What did Copilot misunderstand, assume, or leave ambiguous?
4. Which independent check was most important?
5. What part required finance expertise rather than AI assistance?

## Activity 7C — Save your reusable prompt

```text
Goal: [Specific finance question]

Context:
- Audience: [Role or decision-maker]
- Dataset grain: [What one row represents]
- Period and comparison: [Period, Actual, Forecast, prior period, or other basis]
- Business definitions: [Relevant classification, threshold, or meaning]
- Known limitations: [Missing periods, incomplete definitions, or other constraints]

Output:
- [Requested table, visual, narrative, or calculation]
- [Length, ranking, grouping, or formatting requirement]
- [Decision or action the response should support]

Guardrails:
- Use exact figures and actual column names
- Show formulas and comparison bases
- Preserve source signs and classifications
- Separate observations, assumptions, hypotheses, and recommendations
- Flag missing, zero, negative, duplicate-looking, or unusual values
- Do not invent business explanations
- Protect confidential information
- State validation steps, open questions, and limitations
```

## Example report-out

> We used Copilot to compare Actual results with Forecast and identify the largest exceptions. The most important verified finding was concentrated in a small number of categories, so we replaced a dense report with a sorted comparison visual and an exception table. Copilot initially treated every positive variance as favorable, but we corrected the response by adding account context and explicitly defining favorable treatment. Before using the result, the process owner needs to confirm the operational drivers and supporting evidence.

---

# What good looks like

By the end of the lab, the work should:

- Answer one clear business question for a named audience.
- Identify the dataset, period, comparison basis, units, and level of detail.
- Use a visual or table that matches the question.
- Present the most decision-relevant information first.
- Show or explain important calculations.
- Make vague descriptions measurable.
- Distinguish facts, assumptions, hypotheses, and recommendations.
- Include a documented challenge-and-revision cycle.
- Include at least one independently checked result.
- State validation steps, open assumptions, and material limitations.
- Protect confidential and employee-level information.
- Be reviewable and reproducible by another finance professional.

# Common beginner mistakes and recovery prompts

| Beginner mistake | Why it matters | Recovery prompt |
| --- | --- | --- |
| Asking “What insights do you see?” | The goal and decision are undefined | “List the questions this dataset can answer, then help me select one for [audience].” |
| Accepting a polished response without checking the grain | Totals or comparisons may be invalid | “Explain what one row represents and identify fields that appear to make it unique.” |
| Treating all positive variances as favorable | Business meaning differs by measure | “Remove favorable labels unless the account or measure context supports them.” |
| Asking for too many charts | The main message becomes unclear | “Recommend one visual that best answers the selected question and explain why.” |
| Letting Copilot invent causes | A plausible explanation may not be supported | “Rewrite causes as questions or hypotheses and list the evidence needed.” |
| Ignoring zero or negative denominators | Percentage variances may be meaningless | “Flag cases where percentage variance should not be calculated or needs special interpretation.” |
| Starting over after a weak answer | The user loses useful context | “Critique the prior response against these requirements, then revise only the weak areas.” |
| Sharing detailed sensitive data | Confidential information may be exposed | “Aggregate or remove employee-level and confidential fields before presenting the result.” |

# Optional stretch activities

Use these only if a participant finishes early. They are not required for the 60-minute core lab.

## Stretch 1 — Compare two audiences

Ask Copilot to rewrite the same verified result for:

- A finance leader who needs the decision and risk; and
- An analyst who needs calculations, definitions, and source detail.

Compare what should change and what must remain consistent.

## Stretch 2 — Build a prompt chain

Split one large request into four prompts:

1. Understand the data;
2. Perform the calculation;
3. Draft the communication;
4. Challenge and validate the result.

Discuss whether the staged approach makes errors easier to identify.

## Stretch 3 — Create a repeatable review standard

Ask Copilot to convert the human review checklist into a reusable review template for a recurring monthly process. Confirm that the template does not imply a check was completed when it was not.

---

# Facilitator guide

## Before the session

- Confirm participants can access the practice dataset and Copilot experience.
- Decide whether everyone will use one dataset or role-specific datasets.
- Provide approved variance thresholds, business definitions, or comparison rules if available.
- Identify fields that participants should not share or display.
- Test the core prompts using the selected dataset.
- Prepare a fallback screenshot or small approved table in case access is interrupted.
- Remind participants that the goal is to practice a workflow, not to produce an authoritative business conclusion during the class.

## Suggested facilitation rhythm

### 0–5 minutes — Frame the problem

Demonstrate the difference between a topic and a decision-focused question. Ask participants to name the audience and action before opening Copilot.

### 5–13 minutes — Build the prompt

Show the weak prompt first. Add goal, context, output, and guardrails one at a time so participants can see how each instruction reduces ambiguity.

### 13–23 minutes — Understand the data

Pause after the grain prompt. Compare two responses and ask what evidence supports the proposed row definition.

### 23–33 minutes — Inspect and choose

Emphasize that Copilot should identify issues without silently changing the data. Help participants choose one question that is answerable, useful, and verifiable.

### 33–45 minutes — Analyze and present

Have participants select one analysis path. Encourage follow-up prompts rather than restarting. Limit the presentation recommendation to one visual and one supporting table.

### 45–54 minutes — Challenge and validate

Ask participants to find at least one weakness in their first answer. Require one independent calculation or trace-back before the result is described as checked.

### 54–60 minutes — Share and transfer

Invite two or three 60-second report-outs. Close by asking each participant where the reusable prompt could fit into a real recurring process.

## Instructor observation checklist

Watch for whether participants:

- State an audience and decision before requesting analysis;
- Confirm the dataset grain;
- Notice unresolved field definitions;
- Use actual column names;
- Request formulas or comparison logic;
- Challenge unsupported explanations;
- Independently verify an important result;
- Protect confidential information;
- End with a specific human review step.

## Debrief questions

1. What changed when you provided a clear audience and output format?
2. Where did Copilot make an assumption?
3. Which follow-up prompt most improved the answer?
4. What was the difference between an observation and a possible cause?
5. Which calculation or business definition required human judgment?
6. What would prevent this workflow from being repeatable next month?
7. Where could this workflow save time without reducing review quality?

## Closing principle

> **The objective is not to ask AI for “insights.” The objective is to give it a clear business question, usable context, an explicit output, and review rules that make the result understandable, traceable, and testable.**
