# Project Submission Flow: Problem and Fix

## The problem
When a student clicked Submit Project, the project went straight into the student's portfolio with no company review. That meant unreviewed work looked like verified work to anyone viewing the portfolio, which undermines the point of a portfolio-based hiring platform.

## How I found it
I traced the submission path from the student side, then checked what the company could see and do. I found there was no review step between submission and the portfolio.

## The fix I proposed
1. Student submits the project. Status becomes **Under Review**.
2. The company reviews it using the existing Mark participation as completed screen.
3. If the company ticks Mark project as officially Completed, the project is added to the student's portfolio.
4. If the company leaves feedback without ticking that box, the status becomes **Changes Requested** and the student can resubmit.

## Why this design
It reuses a screen that already exists, so it could ship quickly, and it keeps the portfolio trustworthy. A fuller milestone-based verification at 25, 50, 75 and 100 percent was deliberately deferred to a later phase until there is enough project volume to justify it.
