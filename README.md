# Your Tasks, Measured.

**How do you measure a task?** The question has plagued project managers,
software engineers, and product owners alike for decades. Do we measure in
urgency? Estimated time? Work produced? Or can tasks only be measured relative
to one another? None of these answers ever quite represent all the complexity
a single task contains.

This is where **Quantified Tasks** comes in. By considering five attributes of
any task -- attributes you probably already think about -- and placing them on
five point scales, you unlock significant, practical insight into your tasks,
your sprints, and the project as a whole. Best of all, this insight is easily
shared and understood by all stakeholders in the project: clients, project
managers, supervisors, and developers of all seniorities. Quantified Tasks
informs project goals, schedules, sprint planning, and allocation of work.

It all comes down to five little numbers.

## Measures at a Glance

Quantified Tasks has five core measures: Gravity, Priority, Distance,
Friction, and Relativity. Optionally, there are two additional measures
for bug reports: Origin and Detected.

All measures in Quantified Tasks use a scale of 1 to 5.

### The Planning Measures

In planning, Quantified Tasks distinguishes between the importance of a task,
which is typically fixed, and the urgency of the task, which is fluid.

**Gravity** is the importance of a task to the goals of the project.
g5 is considered absolutely essential, while g1 is a wishlist item.
Gravity is defined primarily by the product owner and stakeholders,
in collaboration with the project manager.

**Priority** is the urgency of the task, somewhat akin to a Kanban
perspective (Now/Next/Later). p4 is considered a "Now" task, while p1
is explicitly omitted from the schedule. p5 is a special value, indicating
an "Emergency" task. Priority is defined by the project manager and developers,
especially following Kanban or Scrum.

Read more about [The Planning Measures](/measures/planning.md).

### The Estimation Measures

Quantified Tasks empowers effective and honest (yes, really!) effort
estimation, making it useful for roadmaps, sprint planning, and more.

**Distance** is the estimated time frame for completion relative to a sprint,
_if you understood everything about the task_. d1 would be a single work
session, while d5 would exceed a sprint.

**Friction** is a measure of available documentation and precedent for
completing the task. f1 would be a task for which there is a complete
tutorial, while f5 would be pure invention.

**Relativity** is a measure of uncertainty, or the likelihood that the
task is a "black hole" with an undeterminable completion date. r1 would
be a task with no known uncertainty, while r5 has virtually no certainty.

The formula `(Distance + Friction) * Relativity` yields an **Energy Points**
value. This can be used in the same manner as Story Points or T-shirt sizes.
Possible Energy Point values follow a non-linear curve. Scores are higher
when confidence is lower (Relativity is higher), ensuring estimates leave
room for unknowns.

Read more about [The Estimation Measures](/measures/estimation.md)

### The Stability Measures

Bug reports optionally have two more measures in Quantified Tasks. These
measures reveal patterns about the stability of your project. The numbers
map to major phases of the Software Development Life Cycle.

**Origin** represents the stage at which a bug originated: Requirements (O1),
Design (o2), Coding (o3), SQA (o4), or Production (o5).

**Detected** represents the stage at which a bug is caught, from t1 to t5,
following the same stages as Origin.

The **Volatility** is calculated as `Detected - Origin`. Higher volatility means
the bug existed in the system for a longer period fo time.

Taking the mean Volatility across your project gives you a
**Project Volatility Score**. This is a predictor of the stability of your
project as a whole, because typically more bugs exist than are caught and
reported.

Read more about [The Stability Measures](/measures/stability.md)

## FAQ

> Is the Quantified Tasks technique compatible with Agile, Scrum, and/or Kanban?

**Yes!** Quantified Tasks is simple enough to fit in with your existing
workflows, especially Agile. In Scrum, you would use Energy Points in
place of Story Points. In Kanban, you'd associate Priority with your board
columns. Read [Agile and Quantified Tasks](/faq/agile.md).

> Is Quantified Tasks compatible with my issue tracker?

There are a few ways to use Quantified Tasks in your issue tracker,
depending on its features. Read [Issue Tracker Usage](/faq/issue_trackers.md).

> What about story points, T-shirt sizes, or Fibonacci numbers?

Energy Points can be used in place of Story Points. It serves many of the
same functions, but it has a few advantages. Read more about
[Story Points or Energy Points](/faq/story_points.md).

> Does Quantified Tasks really measure tasks?

Yes! Quantified Tasks is the first objective technique for measuring tasks, so much so
that it even allows you to [measure developer accomplishment](faq/accomplishment.md).

> Who developed Quantified Tasks?

Quantified Tasks was conceived and developed by Jason C. McDonald,
a principal software engineer with over a decade of experience leading
teams and projects.

The concept of Volatility was originally devised by Kashif Gul Kazi,
in his article [How I Measured The Software Testing Quality](https://dev.to/kashifkazi/how-i-measured-the-software-testing-quality-b60).
It was adapted by Jason C. McDonald.

> How is this related to Quantified Task Management?

The Quantified Task Management standard, originally published by MousePaw Media,
is the predecessor of Quantified Tasks. The name was simplified in this new
version, partly to avoid confusion with another QTM (Quantitative Trust Management),
and partly to move away from the bureaucratic sound of the word "management".
A few improvements to the standard were made besides.

## Feedback

If you have questions, comments, or suggestions, please email us at
feedback (at the quantified tasks domain name).
