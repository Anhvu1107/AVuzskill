# Quality Bar

Apply this finish standard to all meaningful work in this repository.

## Before Work

- Understand the actual request, not just the first visible keyword.
- Gather enough context to avoid blind edits or generic advice.
- Preserve established patterns unless there is a strong reason to change them.

## During Work

- Prefer the minimum skill set that can solve the problem well.
- Keep actions purposeful and sequenced.
- Avoid half-finished implementation when the task is executable end-to-end.
- Keep communication concise, clear, and honest about uncertainty.

## Safety And Ownership Gate

- Prefer local-first defaults. Nothing should auto-connect to outside services unless the user or repo explicitly opts in.
- Remove or isolate proprietary, restrictive-license, or ownership-ambiguous material before treating the bundle as shareable.
- Do not ship personal emails, tokens, API keys, or stale third-party ownership metadata in public-facing files.
- Call out any script that writes outside the repo, opens a browser, or depends on machine-specific state.

## Before Finishing

- Verify the most important behavior you changed.
- Do not describe work as done, fixed, or passing without fresh evidence from the current state.
- Call out what was tested, inspected, or validated.
- State residual risk when something could not be verified.
- Leave the result more coherent than you found it.

## Premium Standard

The work should be:

- correct enough to trust
- clear enough for another agent to continue
- specific enough to feel intentional
- validated enough to reduce back-and-forth
- explicit enough that another agent could continue from the current state

## Red Flags

Do not finish if the output is:

- generic when the task required judgment
- unvalidated when the task was testable
- phrased as complete when the evidence is partial or stale
- overcomplicated relative to the request
- missing the main user outcome
