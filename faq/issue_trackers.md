# Issue Tracker Usage

Quantified Tasks is a fairly new process, and is not officially supported by any task trackers
that we are aware of. However, it is easy enough to integrate. Here's a few strategies to consider.

## Priority <-> Status

**Priority** maps to Kanban columns or the status field in most trackers. If you can edit
the names of the statuses, we recommend using something like the following:

* Backlog (Triage Priority)
* p1: Eventual
* p2: Later
* p3: Next, Selected for Development
* p4: Now/In Progress & In Review
* p5: Emergency
* Done

If that's too many columns, you may be able to set Wishlist and Emergency as tags instead.

## Gravity <-> Urgency/Priority

The "urgency" or "priority" field on most trackers maps to the concept of Gravity. (Yes,
this is confusing until you're used to it.) If you can edit the names of the urgency or
priority options, we recommend the following:

* g5: Highest/Critical
* g4: High
* g3: Medium
* g2: Low
* g1: Lowest/Trivial
* g0: Wishlist (or No Value)
* gT: (No Value)

If you're using Jira, you already have five possible values under their "Priority" field
that you can equate to Gravity scores g1-g5.

## Energy Points <-> Story Points

The Energy Points score belongs in the Story Points field, which most trackers have.
For example, Jira and Phorge have Story Points, while GitLab Premium has Weight.

## Distance, Friction, and Relativity

At a bare minimum, you should include the full formula for your Energy Points at the top
of your description. For example, `(d3 + f2) * r2 = 10` might appear in your description,
while just `10` goes in the Story Points field.

If you have tags, labels, or custom fields, we recommend adding the five values for each of
these three measures as well.

* Jira, Trello, and Phorge/Phabricator (among others) have custom fields on tasks, so add fields
  for Distance, Friction, and Relativity.

* GitHub and GitLab (among others) support arbitrary labels. These should look like
  `d3: Half Sprint` or `f4: Trail` for easy reading and quick adding.

## Stability Measures

Origin, Detected, and Volatility are best specified with custom fields. Barring this,
include them in the description instead.

## Share Your Usage Patterns!

If you have any patterns you'd like to share, email us at feedback (at the quantified tasks domain name).

Additionally, if you are a designer or developer on an issue tracker, and you add support
for Quantified Tasks, let us know! We want to spread the word.
