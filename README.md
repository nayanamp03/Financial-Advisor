# Ledgerlight – Personal Financial Advisor

A single-page web app that helps students, salaried employees, freelancers and business owners understand their finances, plan loan repayments and work toward savings goals. Amounts are in Indian rupees (₹).

**Live demo:** https://nayanamp03.github.io/Financial-Advisor/

## Features

- **Accounts:** create a local account with a name and PIN. The PIN is hashed with SHA-256 before it is stored.
- **Profile:** age, occupation, income, other income and savings, plus nine expense categories. Total expenses and monthly disposable income update as you type.
- **Debt management:** add unlimited loans (education, gold, personal, home, vehicle, credit card, other) with interest rate, EMI, tenure, due date, prepayment charge, priority and secured or unsecured status.
- **Goals:** set a target amount, amount saved and target date, and see the monthly saving needed to reach it.
- **Advisor:** a rule-based analysis engine that produces:
  - a 0–100 financial health score (Strong, Moderate or Needs attention)
  - debt-to-income ratio, emergency-fund cover and monthly cash flow
  - detected problems such as high-interest debt, heavy EMIs and negative cash flow
  - a debt payoff order that accounts for prepayment charges
  - a repayment simulator comparing EMIs only, avalanche and snowball, with an adjustable extra payment
  - a suggested split of the monthly surplus, a goal feasibility check and an action list

## How the analysis works

- Disposable income = total income − living expenses. Free cash = disposable income − total EMIs.
- Emergency-fund target is 3 months of outflow for students, 6 for salaried employees and 9 for self-employed people, freelancers, business owners and others.
- The repayment simulator runs month by month. Interest accrues, EMIs are paid, and freed-up EMIs roll into the next target debt.

## Tech

Plain HTML, CSS and JavaScript in one file, with no build step and no dependencies. Data is stored in the browser's `localStorage`, so nothing leaves your device. Clearing browser data removes your account.

## Run locally

Download `index.html` and open it in a browser.

## Disclaimer

The suggestions come from the numbers you enter and general rules of thumb. They are not regulated financial advice.
