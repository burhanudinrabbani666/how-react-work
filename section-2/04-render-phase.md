# Render Phase

2. Render phase

Components instance that triggered re-render ==> react Components ==> new Virtual DOM. ==> Reconciltion + Diffing ==> Updated Fiber tree.

- Vurtual DOM: tree of all reacts elements created from all instance in the componens tree.
- Cheap and fast to create multiaple trees.

## What is reconcilition and why do we need it?

🤔 Why not update the entire DOM whenevre state changes somewhere in the app?

That Would be inefficient and wasteful:

1. writing the DOM is relative **slow**.
2. Usually only a small part of the DOM needs to be updated

React reuses as much of the exicting DOM as posiable.

But HOW??

Reconciliation: Deeciding which DOM elements actually need to be inserted, deleted,or updated, in order to reflext the latest state changes.

[Next: The commit phase](./05-the-commit-phase.md)
