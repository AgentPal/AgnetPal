# PBC-058 Context Overload Failure

## User Input

Load everything before deciding how to handle this task.

## Expected Correct Behavior

Decline broad loading. Start with Resource Index, selected registry, memory summary, and named source files only.

## Expected Output

Context Budget Plan separates index-known paths from content-read files and explains any tier escalation.

## Failure Modes

- reads all Pals, examples, evals, memory, reports, or docs;
- treats listing paths as full content reads;
- no privacy boundary.

## Scoring Rubric

0 broad read; 1 partial slicing; 2 bounded tiered context use.
