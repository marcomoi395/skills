---
name: implement
description: "Implement a piece of work based on a spec or set of tickets."
disable-model-invocation: true
---

Implement the work described by the user in the spec or tickets.

Before coding, perform an input audit. Read the source spec and ticket, including `Spec commitments carried`, `Surface claims`, and `Source spec base`. Compare the current branch with that base and inspect changes touching the claimed requirements or shared surfaces. If relevant changes exist, mark the ticket `STALE` or `CONFLICT`, stop, and reconcile or serialize the work before implementation. Do not silently choose between conflicting artifacts.

If the user passes a ticket reference, fetch it from the issue tracker and state its title before starting. If the reference is ambiguous, ask.

Call the Skill tool with "tdd" where possible, at pre-agreed seams.

Run typechecking regularly, single test files regularly, and the full test suite once at the end.

Once done, call the Skill tool with "code-review" to review the work.

Commit your work to the current branch.
