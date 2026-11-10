# Deciding by debate

Use this when a simple doubt comes up mid-task. The whole cycle should take seconds, not minutes.

## When to use it

- There are two reasonable options and neither is dangerous.
- Being wrong costs little and can be undone.
- Examples: button color, field order, a label's wording, which already-installed library to use, whether a warning goes in a dialog or next to the field.

Do not use it for actions that cannot be undone, for spending money, or for something only the human knows. In those cases, ask.

If one option wins by a mile, skip the debate: pick it and move on.

## Steps

1. Write the doubt in one sentence and name options A and B.
2. Launch both debaters **at the same time**.
3. When both return, launch the judge with both arguments.
4. Apply the decision. Do not reopen the debate.
5. Keep one line for the final summary to the user.

One round only. If the judge calls it a tie, the option that is easier to undo wins.

At most 3 subagent debates per task. Beyond that, decide directly by the judge's criteria.

## Debater brief

```
You defend option {A or B} in this doubt:
{doubt in one sentence}

Context: {what the screen or task is, in 2 or 3 lines}

Users: people with little computer practice, including a 70-year-old grandmother.

Write the best argument for your option in up to 5 lines.
Be concrete. Also name the biggest risk of the other option.
Do not edit any file.
```

## Judge brief

```
Two agents debated this doubt:
{doubt in one sentence}

Argument A: {text}
Argument B: {text}

Pick one option. Criteria, in this order:
1. What is easiest for a 70-year-old with little practice.
2. What is easiest to undo later.
3. What takes the least work.

Reply only with: the chosen option and the reason in one line.
Do not edit any file.
```

## No subagent tool

Play the three roles in sequence, in writing:

1. Best argument for A (up to 5 lines).
2. Best argument for B (up to 5 lines).
3. Judgment by the three criteria.

Write both arguments before judging. This keeps you from picking the first idea.

## How to tell the user

In the final summary, one line per decision, in plain words:

> I chose to show the warning next to the field, not in a dialog, so the person does not lose what they were typing.

If the user disagrees, switch without arguing.
