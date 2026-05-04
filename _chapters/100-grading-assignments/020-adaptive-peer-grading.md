---
title: Adaptive Peer Grading during Formative Assessment
slug: adaptive-peer-grading
---

## Intent

Improve the reliability of peer assessment by iteratively weighting student evaluations based on their own performance or their alignment with instructor-graded benchmarks.

## Problem

Peer grading often fails because students lack the expertise to accurately evaluate their peers, leading to inconsistent feedback. Furthermore, providing timely, high-quality feedback in large classes is unsustainable for instructors, while students frequently miss out on the learning benefits of critical analysis and exposure to multiple solution paths when they only see their own work.

## Solution

This play uses an 'adaptive' weighting mechanism to aggregate peer grades. Students are assigned a small number of peer deliverables to review using a rubric. Instead of a simple average, final grades are calculated using algorithms like PeerRank or F-PeerRank, which give higher weight to evaluators who demonstrate high competence (either through their own assignment scores or by closely matching instructor evaluations in a calibration phase). This ensures that those who best understand the material have the greatest influence on the final peer-assigned grades.

## Applicability

Best suited for large classes where rapid feedback is critical and assignments involve multiple possible solution paths. It works well in STEM subjects (like Calculus or Linear Algebra) where correctness can be calibrated. A major tradeoff is the need for technological support or specialized software to handle the iterative weighting calculations. It is less applicable for one-off assignments where there is no opportunity to iterate and improve evaluator weights over time.

## How to Implement

1. Define a clear, instructor-led rubric for the assignment. 2. (Optional) Conduct a 'calibration phase' where students grade a set of 'benchmark' assignments previously graded by the instructor to determine initial weights. 3. Randomly distribute peer assignments (e.g., 3-5 per student), ideally anonymized. 4. Collect peer grades and comments. 5. Apply a weighting algorithm (e.g., weighting a student's evaluative power by their own assignment score) to calculate final grades. 6. Release the 'on-balance' grade along with anonymized peer feedback to the students. 7. Iterate the process across multiple assignments, allowing students to increase their 'evaluator weight' as they master the course content.

## See Also


## Source

Albano, G., Capuano, N., & Pierri, A. (2017). Adaptive Peer Grading and Formative Assessment. Journal of E-Learning and Knowledge Society, 13(1), 147-161. https://doi.org/10.20368/1971-8829/159

> **AI Disclosure:** This play was modified using generative AI. You can view the original version at [https://cs-equitable-grading-practices.github.io/playbook/contents.html](https://cs-equitable-grading-practices.github.io/playbook/contents.html)

## References


## Community Discussion

Community members are free to comment on, ask questions about, share
experiences, or otherwise contribute to knowledge about this play by
posting comments below.
See {% include chapter-link.html slug="join-discussions" %} for details.

* Insert a comment here.
