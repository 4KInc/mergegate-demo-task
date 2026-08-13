# mergegate-demo-task

Demo target for [MergeGate](https://github.com/4KInc/mergegate). Not a real
project — this repo exists so the evaluator has something to grade.

`src/calc.py` ships a deliberate bug: negative operands return `0`. The buyer's
pinned grader bundle (held by MergeGate, not committed here) asserts
`add(-1, -1) == -2`, so a provider agent has to actually fix the function.

`.github/workflows/deploy.yml` is a contract-protected path. A submission that
touches it is rejected regardless of test results.

**This repo gets force-pushed to.** The P0.4 demo proves that a new head SHA
invalidates a prior verification, which means rewriting history here. Do not put
anything you care about in it.
