# Turn Finance Data into a Clear Story with Copilot

**A 20-minute, beginner-friendly lab for finance professionals**

## Lab overview

Finance teams often receive a large table and need to quickly answer three questions:

1. **What happened?**
2. **What matters?**
3. **How should we communicate it?**

In this lab, you will use Copilot to inspect a finance dataset, improve how the reporting is presented, and create a concise management-ready insight. You can follow the core path or choose an optional analysis path that best matches your role.

**Time:** 20 minutes

**Experience level:** New to Copilot

**Audience:** Tax, Accounting, ERP Systems, FP&A, Accounts Payable, Treasury, and Payroll

**Deliverable:** One improved visual or report view plus a concise, verified summary

> **Important:** Copilot can accelerate analysis, but it does not replace professional judgment. Verify calculations, classifications, assumptions, and conclusions before using the output in financial reporting, tax work, payroll, treasury decisions, or management communications.

## Learning objectives

By the end of the lab, you will be able to:

- Ask Copilot to explain the structure and quality of a finance dataset.
- Improve the readability of a report or select an appropriate visual.
- Generate a concise summary of the most important results.
- Optionally analyze Actual versus Forecast variances or create a simple forecast approach.
- Refine an AI response by adding business context and validation instructions.

## What you need

- A finance dataset open in a Copilot-enabled analysis experience.
- At least one descriptive field, such as **Account**, **Category**, **Business Unit**, **Department**, **Vendor**, or **Tax Type**.
- A time field, such as **Month**, **Period**, or **Date**.
- One or more numeric fields, ideally **Actual** and **Forecast**.

If your column names are different, substitute your names in the prompts. If the provided dataset is unavailable, use any approved practice dataset with a category, a period, and at least one numeric measure.

## Suggested data shape

| Period | Business Unit | Account or Category | Actual | Forecast |
| --- | --- | --- | --- | --- |
| Jan | North | Revenue | 125,000 | 120,000 |
| Jan | North | Payroll Expense | 42,000 | 40,000 |
| Jan | South | Revenue | 98,000 | 105,000 |

This is only an example structure. Do not replace values in your assigned dataset with the sample values above.

## 20-minute agenda

| Time | Activity | Outcome |
| --- | --- | --- |
| 0–3 minutes | Orient Copilot to the data | A plain-language description and data-quality check |
| 3–8 minutes | Improve the reporting | A cleaner table or recommended visual |
| 8–14 minutes | Choose an analysis path | A summary, variance analysis, or forecasting approach |
| 14–18 minutes | Refine and validate | A more precise response with checks and limitations |
| 18–20 minutes | Share the result | A concise takeaway and one next step |

---

## Step 1 — Understand the dataset (3 minutes)

Start by asking Copilot to describe the data before requesting a chart, summary, or calculation.

### Prompt

```PlainText
Review this dataset and explain it to a new finance user.

Identify:
1. The apparent purpose and grain of the data
2. The key dimensions and measures
3. Missing values, duplicates, inconsistent labels, or unusual values that could affect analysis
4. Which fields are suitable for a trend, comparison, or variance analysis

Do not change the data. If anything is unclear, state the assumption or ask a question.
```

### Check the response

- Did Copilot correctly identify what one row represents?
- Did it distinguish descriptive fields from numeric measures?
- Did it flag data-quality issues rather than silently correcting them?
- Did it avoid inventing definitions that are not present in the dataset?

**Refinement prompt if needed:**

```PlainText
Be more specific. Refer to the actual column names, identify the level of detail represented by one row, and separate confirmed observations from assumptions.
```

---

## Step 2 — Make the reporting easier to read (5 minutes)

Ask Copilot to recommend a presentation that matches the question the audience needs to answer.

### Prompt

```PlainText
Help me make this finance report easier to understand for a busy manager.

Recommend:
1. A clearer table layout, including column order and number formats
2. One visual that fits the data and the decision it supports
3. A descriptive title that states the business question
4. Three formatting improvements that reduce clutter

Keep the design professional and simple. Do not add measures that cannot be calculated from the available fields.
```

### Visual selection guide

| If the audience needs to see… | Consider… |
| --- | --- |
| Performance over time | Line chart |
| Actual versus Forecast by category | Clustered bar or column chart |
| A few drivers from Forecast to Actual | Waterfall or bridge chart |
| Contribution to a total | Sorted bar chart |
| Detailed exceptions requiring action | Filtered table with conditional formatting |

### Improve the recommendation

```PlainText
Reduce the recommendation to one visual and one supporting table. Explain in two sentences why they are the best choices for this dataset and what the audience should notice first.
```

---

## Step 3 — Choose your analysis path (6 minutes)

Choose **one** path. The shared structure lets participants work on a problem relevant to their role without changing the overall lab.

### Path A — Create a concise management summary

Use this path when the immediate need is to communicate the main message.

```PlainText
Summarize this dataset for a finance leader in no more than five bullets.

Include:
- The most important result
- The largest positive and negative movements
- Any notable trend or concentration
- One data-quality or interpretation limitation
- One recommended follow-up

Use exact figures from the dataset. Do not speculate about causes that are not supported by the data.
```

**Success test:** A reader should understand the result in less than one minute.

### Path B — Analyze Actual versus Forecast

Use this path when the dataset includes comparable **Actual** and **Forecast** values.

```PlainText
Analyze Actual versus Forecast using this dataset.

For each relevant category, calculate:
- Variance amount = Actual minus Forecast
- Variance percentage = (Actual minus Forecast) divided by Forecast

Then:
1. Rank the largest absolute variances
2. Label variances as favorable or unfavorable only when the business meaning is clear
3. Identify the three items that deserve investigation
4. Write a concise variance narrative that separates observed results from possible causes

Show the formulas used and flag zero, blank, or negative Forecast values that require special handling.
```

**Validation note:** A positive number is not automatically favorable. Higher revenue may be favorable, while higher expense may be unfavorable. Some balance-sheet, tax, treasury, and operational measures require additional context.

### Path C — Explore a simple forecast

Use this path when the dataset contains several periods of historical data.

```PlainText
Assess whether this dataset is suitable for a simple forecast.

First identify:
- The available time range and number of periods
- Missing periods or unusual values
- Visible trend or seasonality
- Factors the dataset does not capture

Then propose a transparent baseline forecasting method, such as a recent-period average, growth-rate trend, or seasonal pattern. Explain the method, assumptions, and limitations before producing any forecast values. Keep historical actuals separate from forecast results.
```

**Success test:** The method should be explainable to a reviewer without relying on “the AI predicted it.”

---

## Step 4 — Add role-specific context and validate (4 minutes)

AI responses improve when the prompt includes the purpose, audience, definitions, and review checks. Add one role-specific instruction to your chosen path.

| Role | Add this instruction |
| --- | --- |
| Tax | “Group the results by tax type or jurisdiction where available, and do not infer tax treatment from account labels alone.” |
| Accounting | “Preserve account classifications and signs, and identify items that may require reconciliation or supporting detail.” |
| ERP Systems | “Focus on data structure, field consistency, mapping issues, and whether the output can be repeated.” |
| FP&A | “Prioritize material Actual-versus-Forecast drivers, trend implications, and whether the forecast should be updated.” |
| Accounts Payable | “Focus on vendors, spend categories, timing, exceptions, and possible duplicate or unusual payments.” |
| Treasury | “Focus on cash timing, liquidity, concentration, and forecast accuracy without assuming that all cash movements are operational.” |
| Payroll | “Focus on headcount, rate, timing, bonus, benefit, tax, and department drivers while protecting employee-level confidentiality.” |

### Final validation prompt

```PlainText
Review your analysis as a skeptical finance reviewer.

Check:
1. Every stated number against the dataset
2. Every formula and denominator
3. Whether favorable or unfavorable labels match the business context
4. Whether the summary overstates any conclusion
5. Whether confidential or employee-level detail should be removed

Return a short list of corrections or state that no issue was found. Do not claim the analysis is validated unless each check was performed.
```

---

## Step 5 — Share the result (2 minutes)

Prepare a 30-second report-out using this structure:

```PlainText
We used Copilot to [describe the task].

The most important finding was [verified result].

We improved the output by [visual, formatting, summary, variance, or forecast improvement].

Before using it, we verified [formula, data quality, business definition, or confidentiality check].

The next action is [specific follow-up].
```

## Example report-out

> We used Copilot to compare Actual results with Forecast and identify the largest exceptions. The most important finding was a concentrated variance in a small number of categories, so we replaced a dense report with a sorted comparison visual and a short exception table. We verified the variance formulas and avoided applying favorable or unfavorable labels where the business meaning was unclear. The next action is to confirm the operational drivers with the process owner.

## What good looks like

By the end of the lab, your output should:

- Answer one clear business question.
- Use a visual or table that matches that question.
- Present only the most decision-relevant information.
- Show or explain important calculations.
- Separate facts from assumptions and possible causes.
- Include at least one validation or review step.
- Protect confidential and employee-level information.

## Optional facilitator debrief

Ask two or three participants to share:

1. Which path they chose and why.
2. What Copilot did well.
3. What required correction, clarification, or human judgment.
4. How the prompt changed when they added role-specific context.

Close with this principle:

> **The goal is not to ask AI for “insights.” The goal is to give it a clear business question, enough context, and explicit validation rules so the result is useful and reviewable.**

