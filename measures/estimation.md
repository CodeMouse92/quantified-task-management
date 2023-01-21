# The Estimation Measures

There are three Quantified Task measures involved in estimating effort on a task:
**Distance**, **Friction**, and **Relativity**. Each is useful by itself, and you
can combine them to get **Energy Points**, which can be used like Agile story points.

## What To Estimate On

Estimation Measures are meant to be used with User Stories, or else with single,
actionable tasks.

**Do not use estimation measures on Epics or umbrella tasks.** Instead, for these
you should refer to the averages from all the child tasks.

## How To Estimate

You can create an initial estimate for most tasks in under a minute. Remember, this is
only an estimate! You should update these measures later as you learn more about the task.

If you estimate as a team, I recommend using the "planning poker" technique, but
with each team member voting on each of the three measures at once, like this:

```
d3 f2 r3
```

In practice, it doesn't take longer to settle all three of these than it would one number.
The same conversations take place -- effort, precedent, and uncertainty -- but these insights
are captured in the numbers.

## Distance

Distance is the estimated time it would take to complete the task, assuming total
proficiency and knowledge about every aspect. This assumption is crucial in controlling
for different levels of experience, as we only want to measure the task, not the skill
of the developers. It is also important not to let elements of uncertainty in the task
affect this estimate, as that is covered by the other two measures.

Despite the association with time, you are actually measuring implementation effort.

Distance is measured relative to your sprint duration. If you don't use an Agile methodology,
you can still measure relative to a two-week period, the duration of a traditional sprint.

* **d1**: Within day.
* **d2**: Within quarter sprint.
* **d3**: Within half sprint.
* **d4**: Within sprint.
* **d5**: Exceeds sprint. Typically indicates task should be broken down into subtasks.

To help you visualize this, here are the distances relative to particular sprint durations.

|        | 1 week    | **2 weeks**   | 3 weeks   | 4 weeks    |
|--------|-----------|---------------|-----------|------------|
| **d1** | < 1 day   | **< 1 day**   | <= 1 day  | <= 1 day   |
| **d2** | 1-2 days  | **1-2½ days** | 2-4 days  | 2-5 days   |
| **d3** | 2½-3 days | **3-5 days**  | 5-7½ days | 6-10 days  |
| **d4** | 4-5 days  | **6-10 days** | 8-15 days | 11-20 days |
| **d5** | > 7 days  | **> 10 days** | > 15 days | > 20 days  |

Again, if you don't use Sprints, use the **2 week** schedule.

If your project has a high average Distance, this indicates high complexity. Look for
opportunities to break down tasks into subtasks.

## Friction

Friction is a measure of available resources to help complete the task. Importantly,
this is _not_ a direct measurement of difficulty, as that would be relative to
the skill of the developer.

Resources to consider include:

* Reference materials like documentation, articles, tutorials, and lectures. Consider the recency
  of such materials.

* Precedent in code, either internal or open source. The overall health of this code -- good
  practice, patterns, clean coding -- should be taken into account. Also consider the language,
  langauge version, and relevant dependency versions. If your task is in Python, code in Rust is
  likely less relevant than code in Javascript.

* Direct availability of subject matter experts to advise.

* Also consider the health of the source code for the task. Raise your Friction score if
  the code is objectively difficult to work in, relative to good practice in the language.

Remember to measure Friction objectively and empirically. It must _never_ take a developer's
actual skill or experience as a factor.

* **f1: Highway.** Low-skill tasks, tutorial-guided work, low-hanging fruit, housekeeping.
* **f2: Street.** Good reference materials, close precedent. Work occurs in relatively
  healthy source code. Some innovation may be required.
* **f3: Off-Road.** Some reference materials, reasonable precedent. Significant innovation may
  be required, or work may occur in somewhat unhealthy source code.
* **f4: Trail.** Sparse reference materials, distant precedent. Mostly innovation, or work
  occurs in particularly unhealthy source code.
* **f5: Jungle.** Uncharted territory. This issue ticket will self-destruct in fifteen seconds.
  Good luck, Mr. Hunt.

If you're uncertain about the Friction of a task you're estimating, it is usually possible to
establish an initial estimate with a cursory web search. If you cannot, increase the Relativity
or schedule a spike.

When selecting tasks to work on, a developer can pair Friction with their own assessment of
their experience in the code and technical stack to find work appropriate to their skill level.

A high average Friction on a project indicates that you need senior developers or subject
matter experts on the team.

## Relativity

Relativity is a measure of uncertainty, which we call "flux". It indicates the likelihood that
the task is a "black hole" -- its completion date is indefinite, and the more you work on it,
the further you seem to be from completion.

This is part of what makes Quantified Tasks so useful. Instead of effectively lying about our
estimates, as virtually all other project planning techniques do, we literally measure and
report that uncertainty. The higher the Relativity score, the more likely the task is going
to take longer than projected.

A useful analogy is to think of your project as a route on a geographic map. Each uncertainty in
your project is represented a "flux-bridge", or a bridge of indeterminate length. It could be inches, feet, or miles long! We don't know how long these flux-bridges are, but we can typically
count how many lie along a route. This is what Relativity is about.

* **r1: Trivial Flux.** Virtually no unknown factors.
* **r2: Low Flux.** A few identifiable unknown factors.
* **r3: Moderate Flux.** Several unknown factors, but still believed to be completable.
* **r4: Significant Flux.** Extensive unknown factors. Completion unlikely without eliminating
  some flux from the task.
* **r5: Total Flux.** Black hole, completion believed impossible. Task must be abandoned or
  refactored.

Notice, there is always _some_ flux in any task. Nothing is certain but death, taxes, and bugs.

For a detailed discussion of Relativity in practice (in an earlier iteration of Quantified Tasks),
including more information about the concept of flux in project planning, please read the article
[Gallifreyan Software Project Management](https://dev.to/codemouse92/gallifreyan-software-project-management-29a1)

A high average Relativity across a project may indicate significant uncertainty in the design.

## Energy Points

Energy Points are a composite unit of estimated effort required to complete a task. This is
calculated with the formula `(Distance + Friction) * Relativity`. This value is reliable as
an estimation tool because it accounts for implementation (Distance) and research (Friction)
effort separately, and then scales the estimate according to the degree of uncertainty in the
task (Relativity). The idea of multiplying by Relativity comes from the idea of multiplying
software estimates by three to account for delays from unknown factors.

When recording Energy Points on a task, you should ensure that you record Distance, Friction,
and Relativity separately. If you do not have the option to store these in separate fields,
you would store the Energy Point score in the "story point" field, and then write the full
Energy Point equation in the task description, like this:

```
(d2+f3)*r2 = 10
```

(See also, [Issue Tracker Usage](/faq/issue_trackers.html).)

As you get used to working with Energy Points, you will come to understand how much work
you can take on in a given sprint. This is useful for allocating work and determining if your team will need additional developers. Since Distance is relative to a sprint, the average energy points you can complete in a sprint will often remain consistent even with sprints of different length.
As a result, however, Energy Points are "heavier" in longer sprints; you'll be able to clear
less points in a session when the sprints are longer.

Energy Points are used in place of Story Points or T-Shirt Sizes in Agile workflows.
(See also, [Story Points or Energy Points](/faq/story_points.html).)

