# Practical Software Developer Assessments

This repository contains practical assessments and interviewer guides for Software Developer Engineers (SDE1/SDE2, SDE3, and SDE Lead). The goal is to evaluate how candidates build and reason about real systems—not how quickly they can solve contrived puzzle questions under pressure.

## Why This Exists

After 25+ years as a .NET developer, I went through a layoff and had to re-learn the modern interview process. The experience highlighted several issues with common practices:

- **Algorithm trivia doesn't reflect real work.** Solving palindromes on a whiteboard under stress doesn't show whether someone can design, build, and maintain production systems.
- **Stress distorts signal.** People lock up when watched; that measures nerves, not engineering capability.
- **Real skills are broader.** Architecture, testing, observability, security, and communication matter far more day to day than remembering CS trivia.

These assessments aim to reduce unnecessary stress and focus on what actually matters: can the candidate build and reason about software similar to what they'll own on the job?

## What This Is

- **Three practical coding assessments:**
  - `SDE1_Assessment.md` — Entry-level build with guidance on time and expectations; exercises core engineering skills (APIs, async, Blazor, JWT, EF, tests).
  - `SDE2_Assessment.md` — Mid-level build with less hand-holding; same technical scope, but candidates manage their own time and scope.
  - `SDE3-Lead_Assessment.md` — Senior-level build emphasizing systems thinking, resilience, observability, and leadership.
- **Three interviewer guides:**
  - `SDE1_Interviewer_Guide.md`
  - `SDE2_Interviewer_Guide.md`
  - `SDE3-SDEL_Interviewer_Guide.md`

Each guide includes question frameworks, what to listen for, rubrics, and red flags—so interviewers can run consistent, fair conversations centered on real-world capability.

## How to Use

1. **Share the appropriate assessment** with the candidate (SDE1/2 or SDE3/Lead) and give them up to a week to complete it.
2. **Have them walk through their solution** in the interview. Let them explain their design, trade-offs, and testing approach.
3. **Use the matching interviewer guide** to keep the discussion structured and consistent.
4. **Assess on real engineering signals:** clarity of design, correctness, resilience, security thinking, test strategy, and communication—not on how well they perform under whiteboard pressure.

## Philosophy

- **Realistic work over puzzles:** Evaluate the skills engineers actually use.
- **Thought process over perfection:** How they reason about trade-offs and failure modes matters more than flawless code.
- **Lower stress, higher signal:** Give time to produce thoughtful work; use discussion to understand judgment and communication.
- **Fairness and clarity:** Clear expectations, documented rubrics, and repeatable questions yield more consistent decisions.

## Adapting to Your Stack

These assessments are written with .NET and Blazor in mind, but the principles apply broadly. If your team uses a different stack:

- **Swap the tech requirements** (e.g., React instead of Blazor, Spring Boot instead of ASP.NET) while keeping the core challenges (multi-API integration, auth, testing, observability).
- **Adjust the interviewer guides** to reflect your stack's idioms and best practices.
- **Keep the philosophy intact:** realistic work, clear expectations, consistent evaluation.

The goal is evaluating engineering judgment, not framework familiarity—unless framework expertise is specifically what you're hiring for.

## Repository Contents

- `SE1_Assessment.md` — Practical assessment for SDE1 (includes time guidance and rubric tiers).
- `SE2_Assessment.md` — Practical assessment for SDE2 (lighter guidance; scope management is part of the evaluation).
- `SE3-Lead_Assessment.md` — Practical assessment for SDE3/Lead.
- `SDE1_Interviewer_Guide.md` — Interviewer guide for the SDE1 assessment.
- `SDE2_Interviewer_Guide.md` — Interviewer guide for the SDE2 assessment.
- `SDE3-SDEL_Interviewer_Guide.md` — Interviewer guide for the SDE3/Lead assessment.

## Contributing / Adapting

Feel free to adapt these assessments and guides to your team's tech stack or constraints. If you improve clarity or find gaps, update the docs and keep interviewer expectations explicit—consistency is key to fairness.
