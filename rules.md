# Rules

Here are a few ground rules for implementing Quantified Tasks, to help you get the most out of it.

## Rule of Estimation

**Every Task, Story, and Bug with a Priority must also have Distance, Friction, and Relativity.**
If you aren't going to work on the task, you can wait on estimating. Epics also do not have estimates
of their own.

## Rule of Subtasks

**When scoring a subtask, rescore the parent to exclude factors from that subtask.** This ensures you do not
count various factors twice.

Typically, Epics are not estimated (see Rule of Estimation), although you may choose to calculate the sum
and average of their Distance, Friction, and Relativity.

## Rule of Fives

A "5" on any metric should be considered a warning:

* g5: The task must be done in this release.
* p5: The task is an emergency, and must be done _now_.
* d5: The task should be broken down into subtasks.
* f5: The task requires a Spike.
* r5: The task must be refactored to eliminate some unknowns.

## Rule of Emergencies

A priority of "p5" indicates an emergency. A justification for the emergency rating, a timeframe,
and a description of the project consequences if the emergency is unaddressed should be included. 

## Rule of Ones

A "1" on any metric indicates that the task was actually assessed. If the value has not been determined, it should
be left blank or (if a value is required), set to "Triage".

* g1: We plan to include it in a release eventually.
* p1: We plan to work on it eventually.
* d1: The task requires a small amount of work.
* f1: A large body of reference materials exist to assist.
* r1: We have identified virtually no unknowns in the task.

## Rule of Averages

The average of each metric on a task reveals helpful project management insight:

* High Gravity: Probable feature creep.
* High Priority: Sprints are overambitious, or tickets for future work aren't being created.
* High Distance: There's a lot of actual work. If team is falling behind, may need more help.
* High Friction: There's a lot of senior-level work.
* High Relativity: There's a lot of unknowns. Project will need to be refactored to be completed.