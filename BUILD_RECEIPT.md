# Build receipt

Validated on 2026-06-18 in the supplied build environment.

| claim | instrument | current evidence | status | caveat |
|---|---|---|---|---|
| Main skill is tighter while adding project-cycle routing | `wc -w` against the supplied verified-learning edition | 731 → 672 words (`−8.1%`) | verified | Word count does not establish behavioral quality |
| Referenced package paths resolve | relative-path validator over Markdown code references | 28/28 paths exist | verified | Does not establish semantic correctness |
| Skill, candidate, and OpenAI metadata parse as YAML | `yaml.safe_load` | 3/3 parsed | verified | A target runtime may impose additional conventions |
| Python assets compile | `python3 -m py_compile assets/status_enum.py scripts/fable_workspace.py` | exit status 0 | verified | Domain hooks in `status_enum.py` intentionally remain unimplemented |
| Workspace lifecycle works end to end | `python3 scripts/fable_workspace.py self-test` | initialized, logged verified/unverified proofs, parked an idea, completed the gate, and recorded `ship` | verified | Tested on the current operating system and Python runtime only |
| Public CLI accepts the documented basic flow | shell smoke test using `init`, `log`, `gate`, and `status` | 4/4 commands completed; status reported one proof entry | verified | Did not exercise every argument combination |
| Workspace rejects weak release evidence | workspace self-test | placeholder evidence and a non-verified proof row were rejected for gate passes | verified | Manual edits to generated files are outside the CLI contract; `state.json` is authoritative |
| Workspace protects unrelated directories | workspace self-test | reset of an unmarked `.fable/` directory was rejected | verified | Does not cover every hostile-filesystem race on every platform |
| Workspace applies private POSIX permissions | workspace self-test | directory `0700`; managed files `0600` | verified | Windows ACL behavior is platform-dependent |
| Strict amount parser handles supplied cases | executable assertions | 4/4: grouped currency, integer, malformed decimal, embedded text | verified | Not a complete international-currency parser |
| Focused project cycles improve delivery outcomes | controlled comparison in a target agent environment | not run | unverified | Treat the workflow as a method to evaluate, not a proven universal productivity claim |
| Retained skills improve future-agent performance | clean with/without-skill benchmark | not run | unverified | Keep candidates staged until target-environment evaluations pass |

## Reproduce

```bash
python3 -m py_compile assets/status_enum.py scripts/fable_workspace.py
python3 scripts/fable_workspace.py self-test
```

The narrative scenarios in `references/examples.md` are illustrative. They are not counted as package-validation receipts.
