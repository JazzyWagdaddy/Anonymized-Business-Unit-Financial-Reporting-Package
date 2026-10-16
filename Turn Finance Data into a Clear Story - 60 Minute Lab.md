# Lab: From Spreadsheet to Story with Microsoft Copilot
### A 60-minute hands-on lab for Finance teams (Tax · Accounting · ERP Systems · FP&A · AP/Treasury · Payroll)

> Every month you build a report that's 95 rows tall and 24 columns wide… and your CFO reads three numbers. Today, Copilot is your new analyst — fast, eager, a little overconfident. Your job isn't to do the work. It's to *manage* the work.

---

## Lab at a glance

| | |
|---|---|
| **Duration** | 60 minutes |
| **Level** | New to Copilot. Comfortable in Excel. |
| **Tools** | Microsoft 365 Copilot in Excel (primary) · Microsoft 365 Copilot Chat (backup) |
| **Data** | [`data/Anonymized BU Sample Data - Original.xlsx`](data/) — one business unit's monthly reporting package |
| **Framework** | AI Fluency 4Ds: **Delegation · Description · Discernment · Diligence** |

### What you'll walk away able to do

1. **Pretty it up** — turn a dense report into something an exec can scan in 10 seconds.
2. **Summarize it** — get a concise, accurate narrative tailored to *your* audience.
3. **Explain the variance** — Actuals vs. Forecast and year-over-year, with the "why."
4. **Visualize & project** — build a chart and a simple forecast, then sanity-check it.
5. **Catch Copilot when it's wrong** — because it will be, and finance is where that hurts.

### Agenda

| Time | Segment | 4D focus |
|---|---|---|
| 0:00–0:05 | Kickoff & setup | Delegation |
| 0:05–0:12 | **Exercise 1** — Meet your data (and its traps) | Discernment |
| 0:12–0:22 | **Exercise 2** — Make it look nicer | Description |
| 0:22–0:32 | **Exercise 3** — Summarize it in 30 seconds | Description |
| 0:32–0:44 | **Exercise 4** — Variance analysis | Discernment |
| 0:44–0:52 | **Exercise 5** — Chart it & forecast it | Delegation + Discernment |
| 0:52–0:57 | **Exercise 6** — Your role track (pick one) | All 4 |
| 0:57–1:00 | Debrief | Diligence |

---

## Before you start (setup checklist)

- [ ] Download the workbook you received in email.
- [ ] Upload it to **OneDrive or SharePoint** and open it in Excel. Copilot in Excel needs the file saved in the cloud with **AutoSave on**.
- [ ] Click the **Copilot** button on the Home ribbon *or* in the lower right corner, depending on your configuration. If you don't see it, use **Microsoft 365 Copilot Chat** and attach the file instead — every prompt in this lab works there too.
- [ ] **Work on a copy.** Name it `BU Lab - <your initials>.xlsx`.
- [ ] If Copilot says it can't find your data, select the report range (**A4:X95**) before prompting, or mention the range in your prompt. Copilot works best on clean, table-shaped data, and this report has title and section-header rows.

> 🔒 **Diligence check:** This dataset is anonymized and randomized (±3%) for training. Before you try any of this on real data, confirm what your company allows in Copilot. Rule of thumb: use your *work* Copilot (signed in with your company account), never a personal AI account, for company financials.

### About the data (read this — it matters later)

- **One business unit**, 95 rows: Income Statement → Ratios/KPIs → Balance Sheet stats → Headcount.
- **Columns:** May–Aug 2026 Actuals · Sep 2026–Jan 2027 Forecast · Quarterly Actuals/Forecast · FY 2025 Actual · YTD Aug 2025 vs. YTD Aug 2026 · FY 2026 Outlook · FY 2027 Forecast.
- **Units:** The cells hold whole dollars but are *formatted to display in thousands*. Keep that in mind. 😉
- Totals and subtotals are live formulas.

---

## How to talk to Copilot: the 4-part prompt

New learners: you don't need to be a "prompt engineer." Just give it four things — like briefing a new hire.

| Part | Ask yourself | Example |
|---|---|---|
| **Role** | Who should it act like? | "Act as an FP&A analyst…" |
| **Task** | What exactly do I want? | "…summarize performance for Aug 2026 YTD…" |
| **Context** | What does it need to know? | "…values are in dollars, displayed in thousands…" |
| **Format** | What should it look like? | "…as 3 bullets, under 60 words, for a CFO." |

That's **Description** — the second D. Vague in, vague out.

---

## Exercise 1 — Meet your data (and its traps)
**⏱ 7 minutes · 4D: Discernment**

> **Story:** You wouldn't let a new analyst present on day one without asking "what is this file, anyway?" Same with Copilot.

**Step 1.** Paste this into Copilot:

```
Describe this worksheet in plain English. What sections does it contain,
what time periods do the columns cover, and what units are the numbers in?
Then list anything that looks unusual, inconsistent, or worth questioning
before I use this data in a report.
```

**Step 2.** Compare Copilot's answer to the "About the data" section above.

### 🤔 Discuss (don't peek at the answers yet)

1. Did Copilot say the numbers are in **dollars** or **thousands**? If it reads a cell showing `1,405`, is that $1,405 or $1.4 million?
2. Look at **column V** ("Variance Aug 2026 YTD vs Aug 2025 YTD") in the **Ratios** section. Does a G&A ratio *variance* of 1.4% or an EBITA-margin variance of 116% make sense? Why might a formula that works for dollars break for ratios?
3. Sep 2026 is labeled **Forecast** in the monthly columns, but **Q3 2026** is labeled **Actual**. Q3 includes September. What does that tell you?
4. Is there any month that has **both** an Actual and a Forecast? (Hint: what does that mean for "Actual vs. Forecast"?)

> **The aha:** Copilot reads the data *exactly as given*. If the file has quirks, Copilot will confidently repeat them. Your expertise is the filter.

---

## Exercise 2 — Make it look nicer
**⏱ 10 minutes · 4D: Description**

> **Story:** Your report is a buffet with no labels. Everything's there, but nobody knows where the dessert is. Let's add signs.

Pick **two or three** of these. Run them one at a time and watch what changes.

**2a. Highlight the problems**
```
Apply conditional formatting to the Net Income row (row 45) so negative
values show in red and values above $200,000 show in green.
```

**2b. Bold the totals**
```
Make all subtotal and total rows bold with a light gray fill:
Gross Revenue, Cost of Sales, Net Revenue, EBITABA, EBITA,
Non-Operating Expenses Total, and Net Income.
```

**2c. Separate Actuals from Forecast**
```
Visually separate the Actual columns from the Forecast columns.
Use a light blue header fill for Actual columns and a light orange
header fill for Forecast columns.
```

**2d. Make ratios readable**
```
Format the ratio rows that are percentages (for example, EBITA as a % of
Net Revenue and G&A Ratio) as percentages with one decimal place.
```

> 💡 **Tip:** If Copilot can't act on the sheet, ask it to "explain the steps to do this in Excel" instead. Not every request can be applied automatically — that's normal, not failure.

### 🤔 Discuss
- Which prompt worked on the first try? Which needed a second attempt? **What did you add the second time?** (That's Description getting sharper.)
- Is "prettier" the same as "clearer"? What would *your* manager want highlighted?

---

## Exercise 3 — Summarize it in 30 seconds
**⏱ 10 minutes · 4D: Description**

> **Story:** The elevator test. Your CFO steps in, hits the button for floor 12, and says "How's the business doing?" You have 30 seconds.

**Step 1 — The vague prompt (do this on purpose):**
```
Summarize this data.
```

**Step 2 — The 4-part prompt:**
```
Act as an FP&A analyst writing for the CFO. Summarize this business unit's
performance for Aug 2026 year-to-date compared to Aug 2025 year-to-date.
Cover revenue, EBITA, and net income. The numbers are in whole dollars.
Write exactly 3 bullet points, under 60 words total, and end with one
question the CFO should ask.
```

**Step 3 — Change the audience.** Re-run Step 2, but swap "for the CFO" with *your* audience:

| If you're in… | Try "writing for…" |
|---|---|
| Tax | "the Tax Director, focusing on taxes, FX, and non-operating items" |
| Accounting | "the Controller, focusing on unusual accruals or reversals" |
| AP/Treasury | "the Treasurer, focusing on cash, receivables, and deferred revenue" |
| Payroll | "the Payroll Manager, focusing on headcount and bonus accruals" |
| ERP Systems | "the ERP team lead, focusing on data quality and account mapping issues" |

### 🤔 Discuss
- Put the vague and the 4-part summaries side by side. Which would you actually send?
- **Spot check:** Pick *one* number from the summary and find it in the sheet. Did it match? Was it in the right units?
- Did your summary mention that net income went **up** while EBITA went **down**? If not, ask Copilot about it. How is that possible? (Look at rows 38–44.)

---

## Exercise 4 — Variance analysis: Actuals vs. Forecast
**⏱ 12 minutes · 4D: Discernment**

> **Story:** A forecast is a weather report. A variance analysis is asking "why did it rain when you said sunny?" The *number* is easy. The *why* is the job.

**4a. Year-over-year (true Actual vs. Actual)**
```
Create a variance table comparing Aug 2026 YTD Actual to Aug 2025 YTD Actual
for these rows: Gross Revenue, Net Revenue, Cost of Sales, EBITABA, EBITA,
Non-Operating Expenses Total, and Net Income. Show dollar variance, percent
variance, and flag anything with more than a 5% change. Add a one-line
explanation for each flagged item based on the detail rows.
```

**4b. Actual run-rate vs. Forecast run-rate**

> There's no month with both an Actual and a Forecast. So we compare the *average actual month* to the *average forecast month* — a common FP&A move.

```
Compare the average monthly value of the Actual months (May–Aug 2026) to the
average monthly value of the Forecast months (Sep–Dec 2026) for Net Revenue,
Sales & Marketing, EBITA, and Net Income. Show the averages, the dollar
difference, and the percent difference. Which line items is the forecast
most optimistic or pessimistic about?
```

**4c. Hunt for the outliers**
```
Look across the monthly columns (May 2026 – Jan 2027). Identify the three
biggest one-month spikes or drops in any expense line, and suggest a
plausible business reason for each. Label your reasons as hypotheses.
```

### 🤔 Discuss
- Copilot gave you *reasons*. Are those **facts** from the data or **guesses**? How can you tell?
- Look at **Cloud COGS** and **Maintenance COGS** around Sep 2026. Did costs really change — or did they just move rows? Why does this matter for a variance explanation?
- What would you need to *verify* before putting 4c in front of leadership?

> **The aha:** Copilot is great at *finding* the variance and terrible at *knowing* the reason. It's never sat in your month-end close meeting. You have.

---

## Exercise 5 — Chart it & forecast it
**⏱ 8 minutes · 4D: Delegation + Discernment**

> **Story:** A table is a recipe. A chart is the photo of the finished dish. People decide whether to eat from the photo.

**5a. Build a visual**
```
Create a line chart showing Net Revenue and EBITA by month from May 2026
through Jan 2027. Make the Actual months visually distinct from the
Forecast months, and add a clear title.
```

> If Copilot can't create the chart directly, try: *"Tell me step by step how to build this chart in Excel."*

**5b. Simple forecast**
```
Using the monthly Net Revenue values for May–Aug 2026 Actual and
Sep 2026–Jan 2027 Forecast, project Net Revenue for Feb–Apr 2027 using a
simple trend. Explain your method in one sentence and list the
assumptions and limitations.
```

### 🤔 Discuss
- Would you trust a forecast built on **9 data points**, where 5 are already forecasts? What's the risk of "forecasting a forecast"?
- Compare Copilot's trend to the **FY 2027 Forecast** column (col X). Does it point in the same direction?
- Which part of forecasting would you **delegate** to Copilot, and which part must stay with a human?

---

## Exercise 6 — Pick your role track
**⏱ 5 minutes · All 4Ds**

Choose the track that matches your job. Run the prompt, then do the **Verify** step.

<details>
<summary><b>🧾 Tax</b></summary>

```
Focus on the Taxes, Foreign Exchange Loss (Gain), Interest, and Other
Non-Operating rows. Summarize the month-by-month pattern for May–Aug 2026,
flag any month with an unusual amount, and list three questions I should
ask the accounting team before quarter-end.
```
**Verify:** Taxes appear in only one month. Is that a payment, an accrual true-up, or a reclass? Copilot can't know — who would?
</details>

<details>
<summary><b>📒 Accounting</b></summary>

```
Review the Profit Sharing Bonus rows (rows 34 and 85). Identify any negative
months or large swings, explain what an accrual reversal looks like in
monthly data, and draft a short note I could attach to the close file.
```
**Verify:** There are *two* Profit Sharing Bonus rows. Compare their monthly values, then their YTD columns (U and T). Should they tie? What would you check?
</details>

<details>
<summary><b>⚙️ ERP Systems</b></summary>

```
Using the Account and Ref Code columns, list every Ref Code that is used by
more than one row, and any rows where all monthly values are zero. Explain
what data-quality or mapping issues these might indicate in the source
system.
```
**Verify:** Several rows share the code `EmpTot` or `OpExpBBD`. Is that a mapping error or a rollup design choice?
</details>

<details>
<summary><b>📈 FP&A</b></summary>

```
Sales & Marketing is forecast at roughly $225K in Oct 2026 versus about
$100K–$130K in other months. Build a short variance explanation template
I can send to the budget owner, including the questions I need answered.
```
**Verify:** Confirm the Oct figure yourself in row 24. Did Copilot invent a reason, or ask for one?
</details>

<details>
<summary><b>🏦 AP / Treasury</b></summary>

```
Using the Balance Sheet Stats section for May–Aug 2026, summarize the trend
in Cash, Gross A/R, the A/R aging buckets, and Deferred Revenue. Calculate
the percent of Gross A/R that is over 90 days for each month and flag
any concerns.
```
**Verify:** The "Average Days in A/R" row shows 2–4 days. Does that sound realistic for B2B receivables? What might be wrong with the formula?
</details>

<details>
<summary><b>👥 Payroll</b></summary>

```
Using the HR Stats section, summarize headcount by department from May 2026
through Jan 2027. Which departments grow or shrink in the forecast? Show it
as a small table and add two bullets on what this could mean for payroll.
```
**Verify:** Headcount values have decimals (e.g., 114.99). Why? (Remember: this data was randomized.) Would Copilot catch that real headcount should be whole numbers or FTEs?
</details>

---

## Debrief
**⏱ 3 minutes · 4D: Diligence**

Ask the room — don't answer for them:

1. **Delegation:** What's one task from today you'd hand to Copilot *tomorrow*? What's one you never would?
2. **Description:** What single word or phrase made your prompts noticeably better?
3. **Discernment:** Where did Copilot sound confident and turn out wrong?
4. **Diligence:** If you send a Copilot summary to your boss and a number is wrong, whose name is on it?

> **Closing line:** "Copilot is the fastest junior analyst you'll ever have. It never sleeps, never complains… and never sat in your close meeting. Keep your hand on the wheel."

---

## Take-home prompt card

| Goal | Starter prompt |
|---|---|
| Understand a file | `Describe this sheet in plain English and flag anything unusual.` |
| Make it readable | `Bold the total rows and highlight negatives in red.` |
| Summarize | `Act as [role] writing for [audience]. Summarize [period] in 3 bullets under 60 words.` |
| Variance | `Compare [period A] to [period B] for [rows]. Show $ and %, flag changes over 5%.` |
| Explain | `Suggest possible reasons for [variance]. Label them as hypotheses.` |
| Visualize | `Create a [chart type] of [rows] over [columns] with a clear title.` |
| Forecast | `Project [metric] for [periods] using a simple trend. State assumptions and limits.` |
| Check yourself | `What in your answer am I most likely to need to double-check?` |

### Same prompts, other tools
These prompts also work in **ChatGPT** and **Claude** (upload the workbook). The difference: Copilot in Excel can *change* your sheet in place; ChatGPT and Claude typically analyze the file and hand you back results or a new file. Same skills, different hands.

---

## 🧑‍🏫 Facilitator answer key

<details>
<summary><b>Click to expand (instructors only)</b></summary>

All figures computed from the workbook. "$" = whole dollars as stored in the cells.

### Exercise 1 — The planted traps

| Trap | What's going on | Why it matters |
|---|---|---|
| **Units** | Cells store whole dollars; number format `#,##0,` *displays* them in thousands. Row 2's note says "thousands." | Copilot may report May Gross Revenue as "$1,405" or "$1.4M" depending on what it reads. The correct value is ~$1.41M. |
| **Column V ratios** | Column V applies ratio formulas to *variance dollars* (e.g., EBITA % shows 116.5%). | Ratio "variances" in col V are meaningless. Real EBITA margin: 22.2% (YTD 2025) → 21.0% (YTD 2026). |
| **Sep labeling** | Sep 2026 monthly = Forecast; Q3 2026 = Actual. | Labels are inconsistent; ask which is current before reporting. |
| **No overlapping A vs F** | No month has both an Actual and a Forecast. | True "Actual vs. Forecast" isn't possible from this file — hence the run-rate approach in Ex. 4b. |
| **Days in A/R** | Shows 2–4 days for May–Aug 2026. | Likely a formula/annualization error. Gross A/R ≈ $0.7–1.2M vs. ~$1.3M monthly net revenue implies ~15–30 days. |

### Exercise 3 — Key YTD facts (Aug 2026 YTD vs. Aug 2025 YTD)

| Line | 2025 YTD | 2026 YTD | $ Var | % Var |
|---|---:|---:|---:|---:|
| Gross Revenue | 11,489,590 | 11,249,203 | (240,387) | -2.1% |
| Net Revenue | 10,649,334 | 10,359,395 | (289,939) | -2.7% |
| Cost of Sales | 840,256 | 889,808 | 49,552 | +5.9% |
| EBITABA | 3,775,831 | 3,521,699 | (254,131) | -6.7% |
| EBITA | 2,359,248 | 2,171,947 | (187,302) | -7.9% |
| Non-Op Expenses Total | 1,403,429 | 642,524 | (760,904) | -54.2% |
| **Net Income** | **955,820** | **1,529,422** | **573,603** | **+60.0%** |

**The "how is NI up while EBITA is down?" answer:** Non-operating expenses fell ~$761K, mostly from Amortization (−$355K) and Other Non-Operating (−$522K, a 2025 item that didn't recur). Operating performance actually *declined*. A summary that leads with "Net income up 60%!" is technically true and misleading — a great Discernment moment.

### Exercise 4 — Variance highlights

**4b — Monthly averages, Actual (May–Aug) vs. Forecast (Sep–Dec 2026):**

| Line | Avg Actual | Avg Forecast | % Diff |
|---|---:|---:|---:|
| Net Revenue | 1,274,260 | 1,264,923 | -0.7% |
| Sales & Marketing | 100,281 | 148,161 | +47.7% |
| EBITA | 258,944 | 195,004 | -24.7% |
| Net Income | 174,839 | 150,231 | -14.1% |

**Story:** Revenue forecast is flat; profit forecast drops ~25% because S&M spend ramps — driven largely by Oct 2026 (~$225K vs. ~$122K average in the other forecast months).

**4c — Outliers learners should find:**
- **Cloud COGS → $0 from Sep 2026** while **Maintenance COGS (excl. Cloud) roughly doubles** (~$50K → ~$113K). Very likely a **reclassification**, not a real cost change.
- **Oct 2026 S&M spike** (~$225K).
- **Jun 2026 Profit Sharing Bonus is negative** (−$62K) followed by a big Jul (+$158K) — looks like an accrual reversal/true-up.
- **Jun 2026 FX loss** (~$120K) then a **Jul FX gain** (~$69K).
- **Jan 2027 Amortization jumps** to ~$137K (vs. ~$41K) → Jan 2027 **Net Income turns negative** (−$7.8K).
- **Jul 2026 CapEx is negative** (−$112K) — likely a disposal, credit, or reclass.

### Exercise 5 — Forecast context
- FY 2026 Outlook Net Revenue: $15.98M (−1.5% vs. FY 2025).
- FY 2027 Forecast Net Revenue: $14.05M (**−12.1%**); FY 2027 Net Income: $132K (−95%), driven by Amortization of ~$1.69M.
- A simple linear trend on the monthly Net Revenue points downward — directionally consistent with the FY 2027 forecast. Key teaching point: 5 of the 9 inputs are themselves forecasts.

### Exercise 6 — Track notes
- **Tax:** Taxes appear only in Jun 2026 (~$66.5K).
- **Accounting:** Rows 34 (P&L expense) and 85 (balance-sheet accrual) track closely month to month (small gaps come from the ±3% randomization), but their **YTD columns don't tie at all**: Aug 2026 YTD is $418,861 in row 34 vs. $42,265 in row 85 (and $649,869 vs. $77,239 for 2025 YTD). That's the real find — a YTD column built differently for a balance-sheet row. Great recon discussion.
- **ERP:** `OpExpBBD` is shared by rows 21–26, `EmpTot` by rows 88–93, and `6230_10` by rows 34 and 85 — rollup design, but ambiguous for lookups. 13 rows are all zeros across the monthly columns.
- **FP&A:** Oct 2026 S&M ≈ $225K.
- **AP/Treasury:** A/R >90 days as % of Gross A/R: May ~12.2%, Jun ~5.9%, Jul ~11.4%, Aug ~16.2%. Rising aged A/R in Aug is a real flag.
- **Payroll:** Decimal headcount is a side effect of the ±3% randomization. Total headcount ~113–120; S&M grows from 9 to ~12–13 in the forecast.

</details>

---

*Data is anonymized and randomized for training purposes only. Copilot features vary by license, tenant settings, and release channel; if a prompt doesn't run as written, ask Copilot to explain the steps instead.*
