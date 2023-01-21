# The Planning Measures

There are two Quantified Task measures related to planning work to be done on a project.
This work is typically done up front by the project manager and the product owner
Priority is adjusted as part of sprint planning, in conjunction with the
[Estimation Measures](/measures/estimation.html) instead.

## Gravity

Gravity is the importance of a task in relation to the **product release**.
It is useful for defining which features belong in each iteration of a product,
and should be revised with each release.

This one measure is reserved for the product owner and the project manager, and is
the only measure that the product owner is allowed to set or change. Developers should
never change Gravity themselves. That said, the product owner should be aware that
Gravity is intentionally distinct from Priority (defined below). Only the project
manager and developers are qualified to set Priority, although Gravity is a major
factor.

* **g5. Critical.** Project/release cannot ship without. Absolutely must be completed.
  This must only contain Minimum Viable Product/Release features.
* **g4. Significant.** Must be completed, only omit from release if desparate. These
  must be functional requirements, especially those that directly improve on g5 features.
* **g3: Major.** Non-essential, but should be completed if time permits. Includes
  "polishing"-type tasks and more important bells and whistles.
* **g2: Minor.** Not slated for current release, but may be g4 or g5 for later release.
* **g1: Trivial.** "Nice-to-have" tasks that take a back seat to all higher-gravity
  tasks. There must still be reasonable certainty these tasks will be included in a
  later release.

If a task hasn't been discussed yet, or you're not sure it should be included,
it should not be assigned a Gravity score. Depending on your issue tracker,
you may leave it blank or mark it as `gT: Triage`.

As a rule, if everything is critical, nothing is critical! We estimate that your
g5 and g4 tasks should account for only about 20% of your tasks (Pareto principle).
A good way to think about this is to imagine the minimum viable product (MVP),
which contains only g5 features. An MVP is often not going to be particularly fast,
easy to use, or aesthetically pleasing; it is only going to perform its essential
functions in the most Spartan manner possible.

If you're a project manager, it is your duty to ensure the g5 and g4 lists are streamlined!
Failure to do so will impair the developers in setting priorities and planning sprints.

For a detailed discussion of Gravity in practice (in an earlier iteration of Quantified
Tasks), please read the article [Three Ground Rules for Sane Project Planning](https://dev.to/codemouse92/three-ground-rules-for-sane-project-planning-37g9)

## Priority

Priority defines how soon the task needs to be completed, particularly related to **sprint planning**.

Priority is similar to Kanban columns, especially Jira's task statuses.

* **p1: Backlog/Eventual.** Tasks which are not currently planned for the current or next sprint.
* **p2: Later.** Tasks that may be included in next sprint. They may be pulled into the
  current sprint if time permits.
* **p3: Next.** Tasks that should be completed in the current sprint. Developers should
  select tasks to work on which have this Priority level. Similar to Jira's "Selected
  For Development".
* **p4: Now.** Tasks that are currently being worked on. Similar to Jira's "In Progress"
  and "In Review".
* **p5: Emergency.** Reserved for escalating a task above all other priorities;
  "drop everything and do this now!"

Priority should be adjusted on tasks during sprint planning, and tasks will increase
in priority as they are worked on. Priority must always represent the current plan
of the developers.

### About Emergencies

A product owner may *request* that a task be marked as `p5: Emergency`, but it is
ultimately up to the project manager to field and evaluate these requests.
Remember: if everything is an emergency, nothing is an emergency.

Project managers must be prepared to push back on such requests, especially if product
owners, clients, or stakeholders have an "emergency mentality". An effective way to do
this is to require a description of consequences if the task is not completed immediately.
Additionally, one can require the product owner to identify at least one pending g5
(or g4, if no g5 exists) that may be cut from the sprint to accommodate the emergency
request. With the latter technique, only allow the product owner responsible for
setting Gravity on tasks to make that call, lest you be caught in a proxy war between
stakeholders over conflicting priorities.

See also, [Rule of Emergencies](/rules.html)
