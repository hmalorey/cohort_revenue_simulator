# Revenue Model — Bottom-Up Simulator

A cohort-based revenue simulator that models annual revenue from first principles. Built for product and growth teams who need to understand the relative impact of acquisition, conversion, retention and ARPU changes on projected revenue.

## The problem

Every subscription or transactional app faces the same planning challenge: leadership sets a revenue target, say 2x year-over-year, and the team has to figure out how to get there. The debate usually stalls on which lever to pull: more downloads? better conversion? fix retention? raise prices?

Without a model, these conversations run on intuition. Someone argues for acquisition, someone else says retention is the real problem, and there's no shared framework to compare the options. The result is either analysis paralysis or a bet based on whoever argues loudest.

This simulator makes the trade-offs visible. You plug in your actual numbers (funnel rates, retention curve, existing base, churn) and drag sliders to see exactly how much revenue each lever adds. "Increase conversion by 10% vs. improve M3 retention by 5 points" stops being an opinion and becomes a number you can compare.

## What it does

The simulator splits revenue into two streams and combines them:

**New users:** Each month's acquired users flow through a conversion funnel and decay along a retention curve. Cohorts stack over 12 months, producing compounding active users and revenue.

**Existing base:** The starting user base churns monthly at a configurable rate, producing a decaying revenue stream.

The dashboard lets you drag any lever in real time and see how projected annual revenue responds:

- Monthly downloads
- Conversion funnel rates (3-step)
- New user ARPU
- Retention curve (13-month, with uplift slider)
- Existing base size, churn rate, and ARPU

## Features

- **Interactive sliders:** adjust any parameter, see revenue update instantly
- **Cohort matrix:** view active users by acquisition month x calendar month
- **Stacked charts:** revenue and MAU broken down by existing vs. new users
- **Settings page:** configure your own baseline values (revenue targets, funnel, retention curve, existing base)
- **Export:** download the configured model as a standalone HTML file
- **Zero dependencies:** single HTML file, vanilla JS, no build step

## How to use

1. Open `revenue_model.html` in a browser
2. Click **Configure Defaults** to set your own baseline numbers, or **Open Dashboard** to use the defaults
3. Use the sliders to simulate scenarios
4. Switch between Overview, New Users, and Existing Base tabs for detailed breakdowns

## Built with

HTML, CSS, JavaScript. Single file, no frameworks, no external dependencies.

## Context

I built this at Relai to answer a recurring strategic question: "By how much do we need to increase conversion or retention to hit our revenue target this year?" The model made it possible to quantify the relative ROI of investing in acquisition vs. conversion vs. retention vs. ARPU, and communicate trade-offs clearly to leadership.

This is the anonymized, open-source version with generic default values.
