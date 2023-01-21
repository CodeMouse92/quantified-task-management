# Story Points or Energy Points?

Advocates of Story Points bring up several purported benefits. Some of these
are real, but others are just accepted flaws which were re-branded as features.

## Shared Benefits

The real benefits of Story Points are also shared by Energy Points:

* Relative: Task A is larger (requires more effort) than task B.

* Objective: Developers can discuss and agree on points based on observable attributes
  of the task, regardless of their individual skill.

* Unitless: The point system is not mapped to existing units of time or money, thus resisting
  (but not utterly preventing) efforts to interpret points as budgets or commitments.

* Measuring velocity: Both systems of points can be used for measuring and predicting
  team velocity and generating things like burndown charts.

* Persistent: Tasks don't have to be re-estimated frequently (unlike time-based estimates).
  Under either system of points, it may still be necessary to adjust if additional complexity
  is discovered.

* Collaborative: Scoring is done as a team. Either point system can be used in Planning Poker
  (see [The Estimation Measures](/measures/estimation.html).

## What About Fibonacci?

Fans of Fibonacci-based Story Points insist that having a non-linear increase of subsequent
point values is essential.

The main reason cited is that, with increased complexity comes increased uncertainty.
This is represented by having larger gaps between each subsequent level of complexity.
Energy Points does not need this compensation, however, as uncertainty is baked in via
the Relativity measure. The higher the Relativity, the larger the gaps become as complexity
grows.

In fact, Energy Points covers almost the same range of values as Fibonacci-based Story Points.
When you only consider Relativity scores 1-4 (since 5 is typically a warning sign), Energy Points
spans values 1-40, while Fibonacci Story Points spans 1-55, or 0-40 if you're using the common
modified form. Additionally, less than half the values in either system are less than 11, while
only approximately 11% of values are greater than 30.

One other reason Fibonacci is brought up is that it's a "natural" progression of numbers.
While this is a factual statement, it is something of a "sacred geometry" misconception
when it comes to estimation. The very fact many teams modify the sequence to make it work
better for estimation proves the point. After all, what's stopping us from using the
exponents of the Mersenne primes instead (2, 3, 5, 7, 13, 17, 19, 31...)?

However, if you really, _really_ cannot bear to part ways with Fibonacci point scores,
you can just use the closest value to the Energy Score. Since the distributions are similar,
as long as you record your Distance, Friction, and Relativity, which are also useful by
themselves, you don't lose the advantages of Energy Points.

## Unique Advantages of Energy Points

There are a couple of flaws with Story Points that Energy Points overcomes:

Story Points are inconsistent between teams, and point values can even change meaning
as the composition of the team changes. This invalidates the usefulness of points on
tasks estimated by other teams, or even earlier iterations of the current team.

In contrast, Energy Points are calculated from three standardized measures, so relative
"sizes" of tasks are consistent even across teams, and individuals can understand their
own personal capabilities in relation to Energy Points.

The second problem with Story Points is that they discard relevant information, particularly
related to what factors are contributing to a task's size. In Story Points, two tasks may
both be sized as "8", but one is merely a long, repetitive task, while the other involves
developing a new algorithm. While this information should be captured in the task description,
in practice, most teams don't excel at writing descriptions that succinctly express all
relevant information.

With Energy Points, two tasks may still have a score of "8", but the three contributing
measures serve as a "TL;DR" of the essential properties of the task. The long, repetitive
task is `(d3+f1)*r2=8`, while the one involving developing a new algorithm is `(d1+f3)*r2=8`.
This aids in allocating work, and guides further conversation and description.
