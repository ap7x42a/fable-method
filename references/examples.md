# Illustrative scenarios and coverage limits

These compact scenarios explain the plays. They are not reproducible evidence that the whole method works in every environment.

## Debugging

A job emitted empty output. Reverting the newest logging commit did not change the symptom. Stage counts showed eight rows entering a threshold filter and none leaving it; focused config history found an earlier threshold change from 10 to 1000. The newest commit changed reporting, not behavior.

## Refactor

A plausible report cleanup changed ordering and column width. Golden comparison failed. A contract-preserving version was byte-identical while deleting five functions with zero call sites, net −24 lines.

## Extraction

A four-document harness included a non-invoice and a malformed amount. A best-guess extractor scored 1/4 and fabricated values; the anchored, typed, validated extractor scored 4/4.

## Automation

A naive age-based cleanup irreversibly deleted an old human-authored note and scored 0/3. A dry-run, exclusion-aware, trash-based version scored 3/3 and restored a removed file.

## Research

A plausible dependency name and several variants returned 404 from the package registry. Verification stopped the plan before install; a resolving alternative was presented as an explicit choice rather than silently substituted.

## Concurrency

A non-atomic counter passed single-threaded. With 8 threads × 5,000 increments, one stressed run ended at 5,013 instead of 40,000. The same harness returned exactly 40,000 after the critical section was made atomic.

## Learning lifecycle

The retention play is a candidate method until controlled clean-session benchmarks establish retrieval precision, task improvement, and regression rates in the target agent environment. Keep candidates staged until those evaluations pass.
