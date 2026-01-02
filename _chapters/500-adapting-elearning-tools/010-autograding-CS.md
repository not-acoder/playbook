---
title: Automatic Grading System for first year Computer Science Courses
slug: autograding-cs
---
## Intent
Provide automated grading for coding assignments that evaluates both code structure and functionality, rewarding partial progress.

## Problem
Automated grading systems that rely solely on test cases (checking if student output matches expected output) provide limited pedagogical value. When a student's code fails test cases, they receive no credit even if they correctly implemented specific programming concepts required for the assignment. A student who writes a for loop with incorrect syntax might demonstrate understanding of loop structure but receive zero points because their code doesn't compile. Similarly, a student whose code compiles but produces incorrect output gets no recognition for using required data structures or control flow patterns. This all-or-nothing approach fails to provide formative feedback about what students did correctly.

## Solution
This automated grading system evaluates programming assignments through three complementary mechanisms:

**Compilation Checking:** The system first attempts to compile student code. Compilation errors are returned to students with standard error messages.

**Pattern Matching for Programming Constructs:** Using regular expressions, the system searches student code for specific programming patterns that correspond to concepts being taught (e.g., for loops, arrays, if-else statements). Patterns are designed to be flexible enough to accommodate different coding styles while ensuring syntactic correctness.

**Test Case Evaluation:** The system runs student code against predetermined test cases with specific inputs and expected outputs. Students see which test cases passed or failed, along with expected output for failed cases.

Marks are distributed across all three mechanisms, allowing students to earn partial credit for compiling code and using correct programming constructs even if their logic doesn't produce correct outputs.

## Applicability
This approach works well when:
- Teaching introductory programming courses (CS1/CS2) with large enrollments (50-400+ students)
- Assignments focus on specific, identifiable programming concepts
- You have access to frameworks supporting custom grading scripts (VPL for Moodle, browser-based IDEs)
- Demonstrators/TAs are available during labs and would benefit from freed-up time

This approach may not work when:
- Assignments involve complex, open-ended problems with many valid solution approaches
- Programming concepts are too abstract to capture with pattern matching
- Evaluating code quality, efficiency, or style beyond basic construct usage
- Setup time outweighs benefits (very small classes)

**Tradeoffs:** Requires significant upfront investment to create regex patterns and test suites. Regex patterns must be carefully crafted to avoid false positives and negatives. However, scripts are reusable and easily adapted. Works best for well-defined problems rather than creative assignments.

## How to Implement

**Design Assignments Around Teachable Concepts**
Create questions based on specific concepts students are learning. Identify core programming constructs students must use (e.g., "must use a for loop," "must declare an array"). These become targets for pattern matching.

**Develop Regex Patterns for Required Constructs**
For each required construct, develop regex patterns that match syntactically correct implementations while allowing flexibility in coding style. Test patterns against sample correct and incorrect implementations. Start strict and relax based on valid student approaches you observe.

**Create Comprehensive Test Cases**
Develop test cases covering normal cases, edge cases, and error cases. For each, define input values, expected output, and comparison method (exact match, pattern match, numerical tolerance).

**Implement Grading Script**
Create a script (Bash or your preferred language) that:
1. Checks for empty submissions
2. Attempts compilation and awards points if successful
3. Uses grep/regex to search for required constructs and awards points
4. Runs test cases, compares outputs, and awards points
5. Calculates total grade and generates feedback

**Integrate with Learning Management System**
Deploy your script within your chosen framework (VPL, MULE, etc.). Configure to run automatically on submission or on-demand. Set appropriate submission limits.

**Establish Grading Rubric**
Distribute marks across components. For novice programmers, consider:
- 10-20% for successful compilation
- 20-30% for using required programming constructs
- 50-70% for passing test cases

**Iterate Based on Student Submissions**
Review unexpected grades and refine regex patterns and test cases based on what you learn from actual student code.

## Examples

**Example 1: Three-Part Grading**
Assignment: Write Java code using a for loop to sum array elements.
- Compilation (20 points): Code must compile
- Pattern Matching (30 points): For loop present (15 pts), Array declaration (15 pts)
- Test Cases (50 points): 5 test cases × 10 points each

Student with syntax error in for loop but correct array: receives 20 + 0 + 15 + 0 = 35/100 with feedback identifying the for loop syntax issue.

**Example 2: Demonstrator Time Savings**
CS1 class of 400 students, 8 demonstrators, 2-hour lab:
- Without automated grading: ~150 minutes grading per demonstrator, 10 minutes helping students
- With automated grading: 0 minutes grading, 120 minutes helping students

**Example 3: Immediate Feedback Loop**
Student submits code during lab → receives feedback in <10 seconds → sees "Outer loop found ✓, Inner loop not found ✗" → revises and resubmits → demonstrator provides targeted help on nested loops rather than grading submissions.

**Example 4: Regex Pattern Evolution**
Initial pattern for Java for loop: `for.*\(.*\)` → matches invalid syntax
Improved: `for\s*\([^;]+;[^;]+;[^)]+\)` → requires two semicolons
Further refined based on observing student code variations while maintaining syntactic correctness.

## See Also
- Test Case Design for Programming Assignments
- Formative Feedback in Programming Education

## Source
Hegarty-Kelly, E., & Mooney, A. (2021). Analysis of an automatic grading system within first year Computer Science programming modules. In *Computing Education Practice 2021 (CEP '21)*. https://doi.org/10.1145/3437914.3437973

## References
Hegarty-Kelly, E., & Mooney, A. (2021). Analysis of an automatic grading system within first year Computer Science programming modules. In *Computing Education Practice 2021 (CEP '21)*. https://doi.org/10.1145/3437914.3437973