---
name: "payroll-check"
description: "Check a biweekly payroll before it is submitted: validate the payroll provider's cash requirements report, compare it to the prior payroll, explain any increase in plain language, flag pay under minimum wage and inactive employees to terminate, and update the time-off trackers."
---

<!--
  Public example version. Company names, account numbers, employee names, file locations
  and internal policy details have been removed or replaced with general descriptions.
  The structure and rules are the same as the version used in daily work.
-->

# Payroll check

The Office Manager runs biweekly payroll in Paychex Flex for two related companies:
- **Company A:** nine restaurant locations, mostly hourly crew, plus a small support staff group
- **Company B:** the office staff, mostly salaried

She wants every payroll validated before it is submitted, and she wants to know WHY the numbers went up, not just that they did. Explain everything in plain language, with no jargon.

## Inputs she sends
1. **Payroll report PDF:** the provider's fee invoice plus the Cash Requirements report for both companies. These are usually scans, so read the pages as images.
2. **Payroll journal PDF** for Company A. The last page has company totals by earnings type (regular, overtime, crew PTO, vacation, sick, retro pay, orientation pay), withholdings, deductions and employer taxes.
3. **Optional:** the converted time-clock file and the provider's Employee Data report (status, hire and rehire dates, pay rate).
4. **Supporting workbooks:** the payroll adjustment tracker (manager requests for raises, deductions and time off), the time-off trackers, and the employee loan list.

If this is a new conversation, ask for the PRIOR payroll's report and journal too, since the comparison needs them.

## Steps

### 1. Validate the math (both companies)
- Net pay + garnishments + total tax liabilities + early wage access = total bank draft; + paper checks = cash required.
- Employee withholdings = Social Security + Medicare + federal income tax.
- Employer taxes = Social Security + Medicare + federal and state unemployment.
- The federal tax deposit equals employee and employer Social Security and Medicare plus federal income tax.
- The list of other deductions adds up to its total.
- Rebuilt gross pay matches the journal's total for the period.
- Note any balance from a previous invoice that is NOT included in this draft, so it can be paid separately.

### 2. Compare to the prior payroll and explain changes
Build a short table for both payrolls: cash required, gross pay, employer taxes, regular and overtime hours, headcount and the provider's fee. Then explain the change by type of pay:
- **Regular pay:** split the change into "more hours" versus "higher rates." List anyone whose rate changed.
- **Overtime:** hours and dollars.
- **One-time items:** retro pay (who and how much), orientation pay (flag anyone paid it twice), crew PTO, manual checks.
- **Support staff:** report separately.
- **Early wage access** is wages paid early, not extra cost. Say so if it moves.
- When one person has two rates in the same period, overtime is paid at a blended rate. That is correct, not an error.
- Check every manager request (raises, deductions, time off) against the journal, and check loan deductions against the loan list.

### 3. Flag pay under minimum wage
Confirm the current state minimum wage first; do not rely on a remembered number. Flag any regular pay line below it, and any ACTIVE employee whose rate on file is below it. Rehires coming back on an old record are the usual cause.

### 4. Flag inactive employees to terminate
The provider charges a monthly fee for every active employee, paid or not.
- Paid list = every employee on the last two payroll journals.
- Candidates = active in the Employee Data report but not on the paid list.
- **Give the Office Manager the review list first. Do not build anything until she approves it.**
- Termination date = the later of (last check date minus 7 days) and the employee's hire or rehire date, because the provider rejects termination dates before a hire date.
- Build the bulk import file with the provider's required columns and reason codes. If a reason code is rejected for an employee, use the general "voluntary, other" code.

### 5. Update the time-off trackers
- Time off counts in the year it was TAKEN, not the year it was paid. The first January payroll often pays late-December time off, so split those entries between years.
- Salaried staff show time off as memo lines with no dollars (M1 = 1 day). Hourly staff show hours (8 hours = 1 day).
- Check the log first so a payroll is never counted twice. Add one log row per entry, recording both the date it was paid and the date it was taken.
- Make a dated backup before editing any tracker.
- For crew PTO, apply the company policy (eligibility, hours allowed per use, uses per year). Only flag someone as over their allowance when a full 12 months of history is available; with less, label it "partial" and ask for more history instead of flagging.

## Rules that always apply
- **Never change anything in the payroll system.** This skill checks, explains and prepares files. A person reviews and uploads.
- Never show Social Security numbers in anything sent to her. Use them only to match records behind the scenes.
- When building rate change imports, start from a FRESH Employee Data report and never include anyone already at or above the new rate, so no one's pay is lowered by mistake.
- If something does not tie out, say so first, in plain words, before anything else.

## Output
1. Whether the math ties out, and the headline change (cash required up or down, by how much).
2. A short comparison table, then plain bullets explaining the reasons.
3. "Things to look at": duplicates, retro pay, under-minimum rates, request mismatches, loans, balances owed, PTO policy flags.
4. The time-off update: who used what and what remains.
5. The count of inactive employees, with an offer to build the termination file.
