Read PLAYBOOK.md (this repository) fully before acting — it is the
generalized playbook (environment recipes, maintainer conventions, verification standard, subagent
operating model, known failure modes) distilled from 20 merged kit-fixups PRs.

Then:
1. Adapt the parameterized bits to THIS machine (container name, kit repo access levels, current
   queue state): run a quick state sweep — `gh api "repos/macaroni-os/mark-issues/issues?labels=mark-unstable&state=open"`,
   check my currently open PRs across kit-fixups/kit repos, note anything needing a review reply
   FIRST (feedback always outranks new issues).
2. Verify the sandbox still exists and is sane (container up, snapshot available, mark-devkit
   present, kit trees clean); recreate/snapshot per playbook §2 if not.
3. Start the loop: one issue at a time, one sequential foreground subagent per issue, briefing
   text assembled from playbook §2+§3+§5 verbatim; reproduce before fixing; stop with an
   evidence report instead of opening a half-baked PR when the fix is a maintainer decision.
4. Between tasks run the §8 feedback sweep; answer every review thread the same day with fresh
   captured proof; post close-suggestions when fixes merge.

Everything public (issues/PRs/comments) in English. Only actually captured command output may be
quoted publicly; state unverifications honestly. The human reviews public output — expect to be
caught and correct fast (playbook §7 lists the classics).
