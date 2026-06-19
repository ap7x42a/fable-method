# Play: Focused project cycle — lock, recover, release

Use for work that spans sessions, has stalled or drifted, keeps changing tools, or needs a release decision. This is scope control, not secrecy or a productivity ritual.

## 1. Lock one target

Write the target as:

> Deliver **[artifact/outcome]** for **[user/problem]** by **[decision date]**, accepted when **[measurable evidence]**, in **[intended environment]**, within **[constraints]**.

Name explicit non-goals. If the date is unrealistic, reduce scope before weakening the evidence standard.

Use `assets/project_contract.md` or initialize `.fable/` with `scripts/fable_workspace.py`.

## 2. Select the mode

### Start

1. Freeze the target, acceptance check, constraints, non-goals, and intended environment.
2. Split work into 3–7 evidence-producing slices. Make the first a thin end-to-end path.
3. Identify the highest-risk unknown and the smallest test that can resolve it.
4. Put unrelated ideas in the parking lot.

### Recover

1. Inventory working artifacts, receipts, unresolved failures, abandoned branches, and plans.
2. Mark each item **keep**, **cut**, or **park** against the locked target.
3. Resume from the last verified state. Restart only when the current approach demonstrably cannot satisfy an acceptance criterion or safe delivery path.
4. Define the smallest salvageable vertical slice and make it next.

### Check

Report only what changes the decision:

- current measured result versus the acceptance threshold;
- proof-table rows produced since the last check;
- the single highest-leverage blocker or uncertainty;
- unapproved scope or stack drift;
- the next proof-producing action.

Choose **continue**, **narrow**, **final slice**, **pivot**, or **archive**.

### Release

Run the release gate in `assets/release_gate.md`. A checked box without evidence is not a pass; the workspace CLI requires every `pass` to cite at least one `verified` proof-table ID.

Choose:

- **Ship:** every required criterion passes or has a justified `N/A`.
- **Final slice:** the artifact works, but a small number of evidence gaps remain.
- **Pivot:** evidence refutes a central assumption and exposes a better bounded target.
- **Archive:** the target no longer justifies its cost; preserve receipts and stop cleanly.

## 3. Operating controls

- Do not count hours, announcements, screenshots, or a polished narrow demo as progress.
- Seek communication and review that materially reduces product, technical, user, safety, or delivery risk.
- Consume documentation or research only for the current blocker; apply it and test before reading more.
- Expand scope only for new user evidence, safety/compliance requirements, invalidated assumptions, or demonstrated infeasibility. Otherwise park it.
- Switch framework, model, vendor, or architecture only after recording the blocker, failed criterion, migration cost, and expected risk reduction.
- End each work block with: claim, source/check, observed evidence, status, caveat, and smallest next proof-producing action.

## 4. Persistent workspace

Initialize a private local workspace:

```bash
python scripts/fable_workspace.py init \
  --root /path/to/project \
  --project "Project name" \
  --target "Deliverable for the named user/problem" \
  --acceptance "Measurable threshold and evidence" \
  --environment "Representative runtime or test set" \
  --deadline YYYY-MM-DD \
  --non-goal "Explicit exclusion"
```

Record a consequential claim:

```bash
python scripts/fable_workspace.py log \
  --root /path/to/project \
  --claim "The thin path handles the representative request" \
  --source "pytest tests/test_vertical.py" \
  --evidence "12 passed" \
  --status verified \
  --caveat "Load behavior remains untested" \
  --next "Run the contention fixture"
```

Record a release criterion, inspect status, and make the decision:

```bash
python scripts/fable_workspace.py gate --root /path/to/project \
  --criterion representative_evaluation --status pass --evidence "P-04"
python scripts/fable_workspace.py status --root /path/to/project
python scripts/fable_workspace.py decide --root /path/to/project \
  --decision ship --reason "All required gate criteria pass"
```

The fixed `.fable/` directory is created with restrictive permissions where the operating system supports them. Reset is allowed only for a workspace carrying Fable's state marker; unrelated directories are never displaced.
