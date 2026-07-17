---
title: Regret Lottery Grading – Probabilistic Rewards for Consistent Engagement
slug: regret-lottery-grading
---

## Intent

Enable students to build consistent study and participation habits by turning routine effort into entries for probabilistic grade-related rewards, thereby increasing engagement without high-stakes exams.

## Problem

Many students delay engagement until high-stakes exams, leading to cramming, uneven practice, and large performance gaps. Traditional bonus points or extra credit often reward already high-achieving students who would engage anyway, and fixed rewards can quickly lose motivational power. There is also a need for mechanisms that incentivize participation without exacerbating anxiety or grade pressure.

## Solution

A regret lottery grading layer sits on top of regular assessments: low-stakes actions (e.g., weekly problem sets, formative quizzes, forum posts) yield virtual points, and each "wave" (e.g., every 2–3 weeks) ends with a lottery. Only students above a point threshold are eligible to receive prizes, but lottery draws are made across all students, and non-eligible drawn "winners" are told they missed a prize due to insufficient points, maximizing anticipated regret. Points, thresholds, and winners are displayed via a leaderboard or dashboard so students can monitor eligibility and relative activity. In a grading context, prizes can be structured as grade-relevant bonuses (e.g., small exam boosts, late-pass tokens) without changing core grade calculations.

## Applicability

Works well in large-enrollment introductory STEM courses where motivating ongoing practice is difficult. Effective in hybrid or online courses with robust LMS tracking of low-stakes activities like quizzes and check-ins, and in courses emphasizing behavior change or sustained practice (e.g., programming drills, problem sets, spaced retrieval).

Tradeoffs/limitations: Requires reliable tracking of points and eligibility and some technical setup (leaderboards or dashboards). Some students may perceive lotteries as unfair if grade-relevant rewards feel too random rather than effort-linked. Needs careful communication to prevent students overestimating the impact of lottery prizes on final grades.

Not a good fit when: Institutional policy prohibits probabilistic or lottery-like components in grading or incentives. Class sizes are extremely small, reducing the psychological impact of public eligibility and regret messaging. The course already relies heavily on high-stakes summative assessments with little room for additive incentive structures.

## How to Implement

1. Identify 3–5 recurring low-stakes activities per week (e.g., online quizzes, practice sets, participation in discussion boards) and assign simple virtual point values that the LMS can track automatically. Group weeks into "waves" (e.g., three 3-week waves) during the semester.
2. For each wave, set a cumulative point target required for eligibility in that wave's lottery; use decreasing thresholds across waves (e.g., 400, then 100, then 50 points) to keep eligibility attainable.
3. Use the LMS or a simple shared dashboard to show each student's current point total, whether they have reached the eligibility threshold, and relative ranking to others.
4. At the end of each wave, draw winners from the entire class; then award the defined prizes only to students above the threshold while notifying ineligible drawn "winners" that they missed out due to insufficient points, mirroring the regret structure.
5. Use small but meaningful grade-related rewards such as a 1–2 point exam boost or a free late pass as prizes.
6. Track completion rates of low-stakes activities across waves, and gather student perceptions about motivation and fairness to refine thresholds, prize sizes, and messaging.

## Examples

In the StepApp pilot, participants earned points for daily step counts, visualized on a leaderboard, and lotteries were run at the end of each "wave," with prizes randomly distributed among those above thresholds of 400, 100, and 50 points across successive waves.

Winners were drawn from all participants, but non-eligible "winners" were publicly told about forgone prizes, intentionally harnessing regret to increase future engagement.

The study reported that gamified lottery-based incentives increased engagement metrics relative to control conditions.

## See Also


## Source

Nuijten, R., Van Gorp, P., Hietbrink, J., Le Blanc, P., Kemperman, A., van den Berg, P., & Simons, M. (2022). Pilot evaluation of the impact of lottery-based incentives on engagement levels of male low SES vocational students with an mHealth app. *Frontiers in Digital Health*, 3, 748588. https://doi.org/10.3389/fdgth.2021.748588

## References


## Community Discussion

Community members are free to comment on, ask questions about, share
experiences, or otherwise contribute to knowledge about this play by
posting comments below.
See {% include chapter-link.html slug="join-discussions" %} for details.

* Insert a comment here.
