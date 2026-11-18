# Payroll Check: A Claude Skill

A working example of a Claude Skill I built and use every payroll at a nine-location restaurant group. It checks each biweekly payroll before it is submitted, explains in plain language why the numbers changed, and flags problems for a person to review.

> **This is a public example version.** Company names, account numbers, employee names and internal policy details have been removed. The structure and rules are the same as the version I use at work. All numbers in the sample output are made up.

📄 **[Read the skill →](SKILL.md)** · 📊 **[See a sample report →](sample-output.md)**

---

## What is a Claude Skill?

A Skill is a saved set of instructions that Claude follows the same way every time. Instead of explaining the job from scratch each payroll, I wrote down exactly how I check a payroll, once, in plain English. Now I hand Claude the payroll reports and it runs the same thorough check every cycle.

## The problem

Payroll runs every two weeks for about 350 people across nine locations and two companies. Before approving it, I need to know two things: is the math right, and if the total went up, why? That used to mean comparing reports side by side by hand every cycle, and the "why" was often a guess.

## How I built it

1. **Wrote down the process I already followed.** Every check I do by hand became a step: validate the math, compare to the last payroll, explain the change by type of pay, flag pay under minimum wage, and flag employees who have stopped working.
2. **Captured the exceptions.** The hard part was not the math. It was the details only someone who does the job knows: overtime for a person with two pay rates is paid at a blended rate, early wage access is not extra cost, time off taken in December but paid in January belongs to the earlier year, and the provider rejects a termination date before a rehire date.
3. **Kept a person in charge.** The skill never changes anything in the payroll system. It checks, explains and prepares files. I review everything and decide what gets submitted. Before it builds a termination file, it gives me a review list first.
4. **Improved it over time.** When a payroll turned up something new (a rejected reason code, a rehire that wasn't a real break in service), I added a rule so it is handled correctly from then on.

## What it does each payroll

- Confirms the payroll report math ties out for both companies
- Compares this payroll to the last one and explains the change: more hours, overtime, raises, retro pay, time off
- Flags anyone paid under minimum wage, usually rehires on an old pay rate
- Lists active employees who haven't been paid in two payrolls, so they can be terminated and stop adding monthly per-employee fees
- Checks manager requests (raises, deductions, time off) against what was actually paid
- Updates the time-off trackers

## Results

- **Every payroll gets the same check,** with a plain-language explanation of what changed that I can share with the owner.
- **144 inactive employee records cleared,** lowering per-employee fees from the payroll provider, and the count stays accurate because the check runs every cycle.
- **Problems are caught before checks go out,** not after.

## What I learned

The AI was the easy part. The real work was knowing the process well enough to write down every rule and exception, and deciding where a person has to stay in charge. Anything that touches people's pay gets a human check.

---

Part of my [portfolio](https://sarahmartin897.github.io/portfolio) · [LinkedIn](https://www.linkedin.com/in/sarahmartin897)
