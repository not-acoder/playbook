---
title: Outcome Evaluation Clobbering
slug: outcome-evaluation-clobbering
---

## Intent

Implement an "outcome evaluation clobbering" system where grades from subsequent assessments automatically override lower marks from earlier attempts at the same learning outcomes, rewarding final mastery and growth without the logistical burden of manual resubmissions.

## Problem

Traditional assessment models often fix a student's grade at a single point in time, even if the student later demonstrates significant improvement in that same skill. While allowing manual resubmissions is one solution, it often imposes a prohibitive grading burden on instructors and TAs, especially in large courses. Without a mechanism to "repair" early mistakes, students may become demotivated by a low initial mark that they feel no longer reflects their current understanding, leading to disengagement or even withdrawal from the course.

## Solution

Design the course so that learning outcomes are revisited across multiple assignments or exams. When a student demonstrates a higher level of proficiency on a specific skill in a later assessment, that score should automatically "clobber" or replace the lower score from the earlier assessment. This ensures that the final grade is a more accurate representation of the student's end-of-course mastery. To prevent students from simply skipping early assessments, a "participation threshold" (e.g., a minimum score of 20% or evidence of a legitimate attempt) should be required on the initial attempt before it becomes eligible for clobbering by later work.

## Applicability

This play is highly effective in introductory programming (CS1) and other skill-based disciplines where concepts are naturally cumulative. It works best in environments with automated grading tools that can handle the logic of score overrides without manual intervention. A primary tradeoff is the potential for increased student workload, as learners may spend more time on subsequent assignments to repair earlier grades. Instructors must also carefully align learning outcomes across different assessment formats (e.g., ensuring a final exam question truly tests the same skill as an early lab) to maintain the integrity of the evaluation.

## How to Implement

Start by mapping each assessment to specific, granular learning outcomes (e.g., "Variables," "Control Flow," "Data Structures"). Ensure that later assignments are "inclusive," meaning they incorporate and re-evaluate outcomes from previous units. Set up your gradebook logic to compare scores across these mapped outcomes: if grade_n > grade_{n-1}, update the earlier record. To encourage consistent effort, establish a rule that only "serious attempts" (e.g., those meeting a 20% proficiency threshold) are eligible for clobbering. Clearly communicate this policy in the syllabus, emphasizing that the final grade will reflect their best and most recent demonstrations of mastery, thereby reducing the high-stakes pressure of any single initial evaluation.

## See Also


## Source

João Paulo Barros. 2010. Assessment and grading for CS1: towards a complete toolbox of criteria and techniques. In Proceedings of the 10th Koli Calling International Conference on Computing Education Research (Koli Calling '10). Association for Computing Machinery, New York, NY, USA, 106–111. https://doi.org/10.1145/1930464.1930483

> **AI Disclosure:** This play was modified using generative AI. You can view the original version at [https://cs-equitable-grading-practices.github.io/playbook/contents.html](https://cs-equitable-grading-practices.github.io/playbook/contents.html)

## References


## Community Discussion

Community members are free to comment on, ask questions about, share
experiences, or otherwise contribute to knowledge about this play by
posting comments below.
See {% include chapter-link.html slug="join-discussions" %} for details.

* Insert a comment here.
