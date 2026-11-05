# Module 01: The Delegation Decision

> **Role:** AI-Augmented Product Manager · **Level:** L30 · **Prerequisites:** [Module 00](../00-your-relationship-to-the-model/README.md)

The first judgment this role asks of you is: **of every piece of work on your desk this week, which parts go to the model and which stay with you?** Get it wrong in one direction and you ship wrong things fast (over-delegate). Get it wrong in the other and you ship nothing while the model sits idle (under-delegate). Nobody else on the team can make this call on your behalf — they don't see your work the way you do.

This module gives you a working triage: four variables you can score in under a minute per task, a short rubric that turns the scores into a decision, and the one cost most people forget to budget for.

## Why this module comes first

Module 00 named five things this role owns. The first — "which tasks to delegate to models and agents, and which to keep" — sits upstream of the other four. You cannot brief a task you haven't decided to delegate. You cannot verify output from a task you never handed over. Team workflows and accountability are downstream of this one call made correctly, dozens of times per week.

Treating delegation as a one-time preference ("I use the model for PRDs, not for strategy") hides what actually determines the outcome: the call changes task by task, often paragraph by paragraph inside the same PRD. The habit you are building is the triage move, not a policy.

## The two failure modes

Teams fail at this in opposite directions, and often in the same week.

**Over-delegate.** You hand the model work it isn't equipped for — a decision needing judgment about people, a claim requiring domain evidence you didn't supply, a synthesis of context the model can't see. The output reads fluent. You ship it. Later someone with the context catches that it is subtly wrong, or confidently wrong, or wrong in the kind of way that will be expensive to walk back.

**Under-delegate.** You keep work the model would do faster and at least as well — recapping a meeting, pulling evidence from a doc you already have, drafting a first-cut spec from a brief, turning twelve messy user quotes into a tidy table. The work gets done, eventually, at the cost of the harder work that needed your judgment and did not get it. The visible cost is slow throughput. The hidden cost is that you've absorbed hours into mechanical work while the hard calls on the roadmap went unmade.

Each failure mode is invisible from inside it. Over-delegators see a fast team shipping. Under-delegators see a careful team shipping. Both are missing the half they didn't do.

## The four variables

For any task, the delegation decision reduces to four variables. You can score each from memory in under a minute. The exact numbers don't matter — what matters is that you looked at all four before you decided.

| Variable | Question | Higher means |
|---|---|---|
| **Verifiability** | How easily can I tell whether the output is right? | more delegable |
| **Context availability** | Can I hand the model the context it would need? | more delegable |
| **Reversibility** | If this is wrong, how expensive is it to walk back? | more delegable |
| **Judgment load** | Does this depend on calls only I can make (people, politics, roadmap)? | less delegable |

### Verifiability

Verifiability is the hinge of the entire decision. A task you can check in five minutes is worth delegating even if the model is wrong 40% of the time, because you catch the wrong 40% before it ships. A task that takes an hour to check and the model is wrong 10% of the time is worse than not delegating: you now spend the hour anyway, plus you own an answer you didn't form.

Common verifiability patterns in PM work:

- **High:** summarizing a doc you have, extracting entities from a transcript, generating variants of a user journey, translating between formats (markdown outline → JTBD statements → one-pager).
- **Medium:** first-draft PRDs for a scoped feature where you'll read every section; competitive analysis of named products you can spot-check against their own docs; naming and taxonomy proposals you'll pressure-test with the team.
- **Low:** forecasts; estimates ("how long will this take"); claims about external systems you can't cross-reference; synthesis across data the model can't see; summaries of recordings you have not watched.

If a task is low-verifiability, delegating it just moves the work from "I haven't done it" to "I don't know whether it's done." That is not a win.

### Context availability

The model cannot see your Slack, your last roadmap review, the fact that Legal said no to this feature in June, or the tone your CEO used when she brought up the enterprise deal on Tuesday. Everything you expect the model to use, you must either write down or decide you're fine without.

Context has three states for any given task:

- **Available and transferable** — it exists in a doc, a transcript, or a message thread you can paste in. Delegate.
- **In your head, worth writing down** — the briefing itself is the work. Often valuable; see the later module on PRDs as agent context.<!-- needs-research: confirm Module 02 title once planned -->
- **In your head, not worth writing down** — the context is implicit, situational, or too fast-changing. Keep the task.

A task lives in the third category more often than people admit. A triage habit forces you to notice.

### Reversibility

Some outputs are drafts that will be edited by you or reviewed by three other people before anything happens — effectively reversible. Others are messages you are about to send, decisions you are about to post, or artifacts a customer will see unaltered — less reversible.

Delegation tolerance scales with reversibility. A first-draft PRD that you'll read line-by-line can take a model's draft. A reply to an irate enterprise customer cannot — not because the model would write it badly, but because the recoverable cost of "slightly wrong tone" is higher than the time saved.

### Judgment load

Some calls are only yours. "Do we pull feature X to make the deadline?" is not a research question; it is a trade-off against a context that is yours alone. Even if a model can produce a convincing memo recommending the decision, the decision itself is not delegable. Confusing "producing text about a decision" with "making the decision" is the core over-delegation trap.

Where judgment load is high, the useful move is not to ask the model to decide but to ask it to surface the considerations you might be missing, then make the call yourself. Keep the decision; delegate the completeness check.

## A working rubric

Here is a rubric compact enough to run from memory. Score each variable 1–3 and combine. The number is advisory; the point is to have looked.

```
Delegability = Verifiability + Context + Reversibility - Judgment load
```

| Score | Move |
|---|---|
| 5+ | Delegate confidently. Brief well, check the output, move on. |
| 2–4 | Delegate the draft or a subtask. Keep the final shape yours. |
| 0–1 | Keep the task. The model may still be useful as a devil's advocate or completeness checker. |
| ≤ -1 | Don't delegate. Using the model here is a misuse of the tool. |

A worked example: _"Write the problem-statement section of a PRD for the pricing-page redesign the growth team just briefed me on."_

- Verifiability: **3** — I'll read every sentence.
- Context: **3** — I can paste the brief, the current pricing page, and the three complaints from support.
- Reversibility: **3** — it's a draft nobody acts on without review.
- Judgment load: **1** — some framing choices are mine, but most of the section is synthesis of pasted context.

Total: **8**. Delegate confidently.

Another: _"Decide whether to cut the self-serve onboarding flow from v1 to hit the deadline."_

- Verifiability: **1** — no clear "right answer" to check against.
- Context: **1** — depends on things I know but haven't written down (CEO's tone on launch, sales commitments, eng morale).
- Reversibility: **1** — the call sets the launch narrative.
- Judgment load: **3** — this is the kind of trade-off the role exists for.

Total: **0**. Keep it. The model is useful afterward to pressure-test the memo announcing the call.

A third, on purpose boring: _"Pull the five customer quotes from last week's interview notes that mention onboarding friction."_

- Verifiability: **3** — I can diff the output against the notes.
- Context: **3** — I can paste the notes.
- Reversibility: **3** — I'm using the quotes in a draft.
- Judgment load: **1** — selection taste is mine, but the mechanical search is not.

Total: **8**. Delegate every time. If you are reading through transcripts yourself to find the quotes you already know are there, you are under-delegating.

## The cost nobody budgets for: verification

Every delegated task incurs a second task: checking the output. If you budget only the first and not the second, you will over-delegate, because the spreadsheet looks great right up until the postmortem.

A rough calibration: budget verification time equal to what the model saved you, at least initially. Reduce it only once you have data on where the model is reliable in your specific workflow. If a model drafts a competitive analysis in two minutes that would have taken you thirty, the net saving is only real if your check takes less than twenty-eight minutes.

Two common verification traps:

- **Skimming for fluency.** Model output reads fluent whether or not it is true. Reading a draft in a flow that notices "this sounds right" instead of "does this match the source" is the main way false claims ship.
- **Verifying the easy parts.** The first paragraph of a draft is usually fine. The citations, numbers, and edge-case claims later in a long piece are where errors live. Verification cost is end-weighted; reading time is front-weighted. Deliberately flip it: read the last section first.

A third trap, subtler: **stopping verification once a model has been right a few times.** Reliability on your past prompts is not reliability on your next prompt. The error distribution is lumpy; the sample you have is small. Keep verifying until you have enough data to replace the budget with evidence, and remember that model behavior can shift under you when a vendor updates the backing model.

## How this changes per task type

The four variables don't shift, but their typical values do. A short field guide:

| Task type | Typical profile | Default move |
|---|---|---|
| Meeting recap from a transcript | V:3 C:3 R:3 J:1 | Delegate; spot-check decisions and action items. |
| First-draft PRD for a scoped feature | V:3 C:2–3 R:3 J:2 | Delegate the draft, keep the framing and the open questions. |
| User-interview synthesis | V:2 C:2 R:3 J:2 | Delegate extraction, keep the "so what." |
| Competitive teardown | V:1–2 C:1 R:3 J:1 | Delegate the structure; don't trust any specific claim about a competitor without checking. |
| Roadmap trade-off memo | V:2 C:1 R:2 J:3 | Draft the memo yourself; ask the model what you may have missed. |
| Customer-facing email | V:2 C:2 R:1 J:2 | Draft or edit, but you own the voice; never send unread. |
| Timeline estimate | V:1 C:1 R:1 J:3 | Don't delegate. The model has no basis for this. |
| Pulling evidence from a doc you already have | V:3 C:3 R:3 J:1 | Delegate every time. This is the easy win. |
| Meeting-prep brief for a person you are meeting | V:2 C:2 R:3 J:2 | Delegate from written context (profile, past messages); don't delegate the strategy of the meeting. |
| Naming / taxonomy generation | V:2 C:2 R:3 J:1 | Delegate for breadth; keep the final pick. |

These are defaults, not rules. Any specific instance can shift a variable; your job is to notice when it has. A PRD for a feature with a politically loaded scope has a higher judgment load than the table suggests. A customer-facing email where you are only forwarding a vendor's update has a higher reversibility than the table suggests.

## What this module does not cover

- **How to brief the model** once you've decided to delegate. That is its own craft; it belongs in a later module on writing briefs and PRDs as agent context.
- **How to evaluate model output systematically** at team scale. The rubric here is a personal-habit tool, not a team eval pipeline.
- **Which specific tool or model to use.** The delegation call is tool-agnostic. Pick a model whose behavior you know and that your org permits you to use for the sensitivity of the task.<!-- needs-research: link to this org's governance guidance on data handling for AI tools, once published -->

Treat this module as the base habit. Every later module in this track assumes you have already made the delegation call cleanly before you reach for a prompt.

## Common mistakes

**Treating "I prefer not to use AI for X" as the triage.** Preferences drift into blanket rules. Keep the four variables live; let them override preferences.

**Delegating the decision, not the preparation.** "Should we cut feature X?" is not a prompt. "Here's what cutting feature X would save and cost; what have I missed?" is.

**Verifying only the parts that are easy to verify.** If you only ever check numbers in tables and skim the prose, model drafts will drift the prose in ways nobody notices for months.

**Writing everything down for the model.** Context-transfer is work. Sometimes it is the right work (a durable brief, a reusable PRD template). Sometimes it is cheaper to just do the task. Notice which you're in.

**Confusing fluency with correctness.** The single most load-bearing habit of this role. If you only take one thing from this module: a well-written paragraph is not a true paragraph.

**Benchmarking the model against yourself on a good day.** The real comparison is against the task you would actually have done — in the time you actually had, under the context load you actually had. Measured against the version of you who had two hours and full context, every model looks bad. Measured against the version of you who had fifteen minutes between meetings, many tasks look obviously delegable.

**Treating one bad output as evidence to stop delegating a task type.** One bad output on a high-verifiability task is exactly the outcome the rubric is designed for: you caught it, nothing shipped, carry on. The task type is not the problem; the brief probably was.

## Before you move on

Do [Exercise 01: Run the delegation rubric on this week's work](exercises/exercise-01-run-the-delegation-rubric.md). The exercise asks you to apply the rubric to real tasks from your own queue and keep the result so you can compare your calibration against the outcome a week later. The rubric is only useful once you discover where it misled you.

## References

- Anthropic. *Introduction to Claude.* Anthropic documentation (docs.anthropic.com). Baseline for how to think about what current large language models do and don't do — read the sections on capabilities and limitations rather than the prompt-engineering tips.<!-- needs-research: confirm the canonical introduction URL on docs.anthropic.com -->
- NIST. *AI Risk Management Framework (AI RMF 1.0).* National Institute of Standards and Technology, January 2023. Treat its **Measure** function as the serious, team-scale version of the verification habit introduced here.
- Marty Cagan. *Inspired* (2nd ed., Wiley, 2017) and *Empowered* (Wiley, 2020). Practitioner reference for the judgment work this module calls "non-delegable," especially the distinction between product discovery and product delivery.
