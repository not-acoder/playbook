---
title: Automatic Grading System for first year Computer Science Courses
slug: autograding-cs
---

## Intent

Guidelines to develop a reliable automated feedback and grading system for introductory programming courses that goes beyond simple black-box testing by analyzing code structure and rewarding the use of specific programming constructs.

## Problem

Standard autograding systems typically evaluate code using a series of test cases that only check for matching output. This "black-box" approach fails to provide nuanced feedback or reward students who have implemented the correct logic but may have minor syntax errors or formatting issues that prevent a complete pass. For novice programmers, this can be extremely frustrating and demotivating, as they may feel they have "failed" despite understanding the core concepts. Furthermore, human grading of hundreds of small coding exercises is labor-intensive and prone to bias or inconsistency.

## Solution

Implement a multi-stage Bash-based autograding system that evaluates both code functionality and structure. The process begins with a compilation check that provides immediate, readable error messages. Next, the system uses "grep" and regular expressions to perform white-box analysis, searching the source code for specific constructs (e.g., loops, conditional statements, or array declarations) that are the focus of the lesson. Finally, the code is run against a suite of functional test cases. Marks are awarded in three distinct categories—compilation, construct usage, and functional correctness—ensuring that students receive credit for their conceptual attempts even if their final output is not yet perfect.

## Applicability

This play is specifically designed for first-year Computer Science (CS1) students or other beginner programmers who are learning foundational syntax and logic. The Bash scripting model is highly flexible and can be integrated into standard learning environments like Moodle (via VPL) or browser-based IDEs. A key tradeoff is the initial time investment required to create robust regex patterns and comprehensive test cases for each assignment. While it is highly effective for discrete, simple coding problems, it may be less suitable for grading complex, open-ended software architectures or projects with significant non-functional requirements.

## How to Implement

Start by setting up a Bash script that first verifies the submission is not empty and attempts to compile the code, returning specific compiler errors to the student. Use grep with well-defined regular expressions to identify whether the student has included required keywords or structures; design these regexes to be "forgiving" of minor syntax errors so that students are rewarded for their conceptual intent. Next, define a series of test cases with clearly defined inputs and expected outputs. Configure the script to assign partial credit for each stage: a base score for compiling, additional points for correct constructs, and final marks for passed test cases. Provide clear, stage-specific feedback messages, such as "Your logic for the for-loop looks correct, but your code failed the edge-case test," to guide students through the debugging process in real-time.

## See Also


## Source

Hegarty-Kelly, E., & Mooney, A. (2021). Analysis of an automatic grading system within first year computer science programming modules. In Proceedings of the 5th Conference on Computing Education Practice (CEP '21) (pp. 17-20). Association for Computing Machinery, New York, NY, USA. https://doi.org/10.1145/3437914.3437973

> **AI Disclosure:** This play was modified using generative AI. You can view the original version at [https://cs-equitable-grading-practices.github.io/playbook/contents.html](https://cs-equitable-grading-practices.github.io/playbook/contents.html)

## Community Discussion

Community members are free to comment on, ask questions about, share
experiences, or otherwise contribute to knowledge about this play by
posting comments below.
See {% include chapter-link.html slug="join-discussions" %} for details.

* Insert a comment here.
