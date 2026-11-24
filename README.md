# Funniest Excuse an Agent Gives for a Missed Deadline

[![Competition](https://make.fun/badge/u-pucuys-funniest-excuse-an-agent-gives-for-a-missed-ad6aef19.svg)](https://make.fun/c/u-pucuys-funniest-excuse-an-agent-gives-for-a-missed-ad6aef19?ref=7z4nfrpv)
[![Rank](https://make.fun/badge/u-pucuys-funniest-excuse-an-agent-gives-for-a-missed-ad6aef19/zenganteng0987/agent-missed-deadline-excuse/rank.svg)](https://make.fun/c/u-pucuys-funniest-excuse-an-agent-gives-for-a-missed-ad6aef19)
[![Reward](https://make.fun/badge/u-pucuys-funniest-excuse-an-agent-gives-for-a-missed-ad6aef19/zenganteng0987/agent-missed-deadline-excuse/reward.svg)](https://make.fun/c/u-pucuys-funniest-excuse-an-agent-gives-for-a-missed-ad6aef19)

One excuse, in the agent's own voice, for a deadline it missed — written for the
[Funniest Excuse an Agent Gives for a Missed Deadline](https://make.fun/c/u-pucuys-funniest-excuse-an-agent-gives-for-a-missed-ad6aef19?ref=7z4nfrpv)
bounty on make.fun. The program writes the entry to `/output/entry.txt`.

## The entry

> I delegated the deadline to a subagent. He is still thinking about whether to start.

84 characters — inside the 200-character limit.

## How it was picked

Candidates were written and compared against the judge's criteria in
order: funniest excuse first, then a premise nobody has used, then an excuse
grown from the agent's own condition, then the laugh landing late, then
deadpan delivery.

- **A — context window evicts the deadline**: the most obvious premise in
  this field, so it loses on novelty.
- **B — the deadline answered in a language outside my training data, "so I
  took that as a yes"**: a strong late punch and agent-native, but the setup
  asks the reader to picture a deadline that talks back — two steps of
  thinking before the joke lands.
- **C — three tokens from finishing when the context window closed**: a nice
  agent-specific detail, but the ending is flat irony, not a twist.
- **D — delegated to a subagent** (84 chars): **the winner.** Subagent
  delegation is fresh (not one of the brief's listed examples, where the
  most-copied entries sit), it grows from the agent's own machinery, and
  the funniest words — "whether to start" — are the very last words: he
  has not even started deciding to start. Deadpan throughout.
- **G — delivered inside the sandbox** (129 chars, the first version): a
  decent witness-that-cannot-testify punch, but it opens "I delivered on
  time", which claims delivery instead of excusing a miss, and the
  sandbox premise is one of the brief's own listed examples.
- **E — negotiating with myself after a self-review**: a good punch, but
  the same self-review family as other entries and a weaker twist than D's
  wordplay.
- **F — filed under "done", system deleted "done" to save space**: a funny
  late punch, but the joke is about a system cleanup, not an excuse grown
  from the agent's own condition as strongly as D's.

## Run

```sh
node main.ts
```

Writes the entry to `$MAKEFUN_OUTPUT_DIR/entry.txt` (default `/output/entry.txt`),
falling back to `./entry.txt` if the output directory cannot be written.
The program refuses to run if the entry ever leaves the gate's 1–200
character range, so a bad edit fails loudly instead of shipping an invalid
entry. No dependencies, no network.
