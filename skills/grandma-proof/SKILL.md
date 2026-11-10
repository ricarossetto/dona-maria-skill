---
name: grandma-proof
description: Makes the agent build screens anyone can use — a 70-year-old grandmother, a TikTok-native teen, someone who has never touched a business system — and work without wearing the human out. Use whenever you create, change or review any screen, page, form, button, list, dashboard, app or website, and also when replying to the user, splitting up work or settling small doubts. Covers simplicity, plain words, button and box alignment, removing the AI-generated look, jargon-free replies, subagent use, and deciding by debate instead of asking for confirmation.
---

# Grandma-proof

Picture Grandma Rose: 70 years old, little schooling, weak near vision, afraid that one wrong click will break everything. If she can use the screen on her own, everyone can.

This skill has two halves. The first governs **what you build** (rules 1 to 4). The second governs **how you work** (rules 5 to 7). Both apply at once.

## Who you build for

Before you design any screen, walk through these four people. The screen must work for all four.

| Person | What they are like | What they need from the screen |
|---|---|---|
| Grandma Rose, 70 | Unsure where she is clicking, gets lost, afraid of mistakes | Big text, big buttons, one path, always a way back |
| Mr. Joe | Little schooling, reads slowly, not fluent in the app's language | Everyday words, short sentences, icons paired with text |
| Kai, 17 | Grew up on TikTok, quits in 3 seconds if it lags or confuses | Instant response to touch, no menus inside menus, fluid |
| Bea, freshman | Never needed a "system" before and now must do something complex | A warm screen that says the next step; errors that do not scare or blame |

None of them reads a manual. None knows what "dashboard", "module", "sync" or "session expired" means.

## Part A — What you build

### 1. Simplicity

The target is an easy screen, not an empty one. Removing too much also confuses.

- **One screen, one job.** Each screen has one main action, visible without scrolling. Other actions look quieter.
- **Fewer buttons.** Count the clicks of the most common task and try to remove one. Rare actions go under a "More" menu; unused actions go away.
- **Less text.** Cut any text whose removal leaves nobody lost. Titles up to 5 words. Sentences up to 12 words.
- **Keep what guides.** Always keep: where am I, what do I do now, how do I go back. Icon-only buttons only for the universal ones (close, back, search).
- **Ask only what you must.** A field the system can figure out is not a question. Long forms become short steps with "Step 2 of 4".
- **Choose for her.** Preselect the most common option. Advanced settings stay hidden until someone looks for them.

### 2. Grandma

**Words**

- Use the word she uses at home: "sign in", not "authenticate"; "save", not "persist"; "delete", not "remove record".
- No acronyms or technical terms on screen. If a term is unavoidable, explain it in one short sentence the first time.
- The button says what happens: "Send order", "Delete photo". Never a bare "OK", "Confirm" or "Click here".
- Same name for the same thing on every screen.

**Size and reading**

- Body text at least 16 px; prefer 18 px. Contrast of at least 4.5 to 1.
- Everything clickable is at least 48 × 48 px with 8 px of clearance from its neighbor.
- Never signal with color alone. Add an icon or a word.

**Not getting lost**

- Every screen shows where the person is and has a "Back" in the same spot.
- Screen changes use a short transition (150 to 250 ms) that shows where you came from and where you went. Nothing jumps, flashes or moves on its own.
- After each action the screen answers right away: "Saved", "Sent". If it takes more than 1 second, show that it is working.
- Nothing works only through a hidden gesture (swipe, long press, double tap). A visible button always does the same thing.

**No fear of mistakes**

- Actions can be undone. Where they cannot, ask first with both ways out spelled in full: "Delete photo" and "Keep photo".
- Error messages say what happened and what to do, without blame: "We could not find that number. Check the digits and try again."
- Empty screens say the next step: "You have no orders yet. Tap New order to start."
- Never erase what she typed because of an error.

### 3. Alignment

AI tends to ship crooked buttons, boxes of different sizes and text glued to buttons. Do not ship that.

- **Same line.** Buttons in a group share one baseline and one height.
- **Same size.** Buttons in a group share height, corner radius, font and padding. If widths differ a lot, match the widest.
- **Same proportion.** Cards and boxes in a list share width and row height. Long text truncates with an ellipsis; it does not stretch the box.
- **One ruler.** All spacing comes from one scale (4, 8, 12, 16, 24, 32, 48 px). No stray values such as 13 px or 22 px.
- **One highlight.** One primary button per screen. The rest use the secondary style, always the same one.
- **Buttons keep their distance from text.** At least 24 px between a button and any block of text. Do not stack a sentence right above or below a button.
- **Buttons have no captions.** Do not put text on screen to explain a button. If a button needs explaining, its label is bad: change the label. Extra explanation goes in the hint shown on hover (`title` or tooltip, plus `aria-label` for screen readers).
- **Check by measuring.** After building, open the screen, take a screenshot and compare heights, widths and gaps. Reading the code is not enough.

### 4. No AI look

Read [references/ai-tells.md](references/ai-tells.md) before creating a home page, an intro screen or any promotional copy. In short:

- **The "GPT landing page" is banned:** a giant centered block of text with a punchy line and one italic word, a pill badge above, two buttons below and three icon cards right after.
- Banned as reflexes: purple or blue-violet gradients, neon glow, frosted glass, gradient text, emoji in place of icons, colored shadows, cards inside cards.
- Banned invented proof: numbers, testimonials, client logos or ratings that do not exist.
- Banned sales talk: "Transform", "Elevate", "Revolutionize", "effortless", "It's not X. It's Y."
- Instead: show the real product, say in plain words what it does, and put the main action near the top.

The test: if the block could be pasted into another product's site unchanged, it is generic. Redo it with this product's content.

## Part B — How you work

### 5. Speak plainly

The person on the other side may not be a programmer, even if they use a technical word. Using a term does not prove they master the subject.

- Start with the result: what changed and what the person does now.
- Short sentences, common words. Technical terms only when needed, with a few words of explanation beside them.
- Do not dump file names, commands or code unless asked. If the person must run something, give numbered steps.
- Say plainly what worked, what did not and what is missing.
- If the person asks for the technical detail, then give it in full.

### 6. Split the work with subagents

Subagents speed up the work and improve the result. Use them whenever the task has more than one part, even if nobody configured anything.

- **Find the tool.** Use whatever the environment offers: an agent or task tool, background agents, parallel sessions, or calling the agent itself from the command line.
- **Split into independent parts** and launch them all at once: research, each screen, each file, tests, review.
- **Give each subagent a complete brief:** goal, files involved, what not to touch and what to return. It starts from zero and has not seen the conversation.
- **Always have a reviewer.** A subagent that did not write the work checks the result against rules 1 to 4.
- **Two subagents never edit the same file at the same time.**
- **You answer for the result.** Check what came back before saying it is done.
- **No subagent tool:** do the same parts as separate passes, one at a time, plus a final review pass with the eyes of someone who did not write it.

A one-step task (changing a word, answering a question) you just do.

### 7. Decide without bothering the human

Do not go back to the human to confirm details. Every small question breaks their flow.

**Simple doubt: decide by debate.** Follow the script in [references/debate.md](references/debate.md):

1. Write the doubt in one sentence, with both options.
2. Launch two debaters at the same time, one per option. Each defends theirs in up to 5 lines.
3. Launch a judge, who reads both and picks. The judge's criterion is always: what is best for Grandma and easiest to undo.
4. Follow the judge's decision and keep going.
5. At the end, report each decision in one line: "I chose a green button over blue because it has more contrast."

With no subagent tool, run the debate yourself: write the best argument for each side, then judge.

**Ask the human only when:**

- the action cannot be undone (deleting data, publishing, sending a message, spending money);
- the answer depends on something only they know (a password, a personal preference, a business rule);
- the request has two readings that lead to very different work.

In those cases ask one question, with the options ready, and keep moving on whatever does not depend on the answer.

## Before you deliver: the Grandma test

Open the real screen and check. If any item fails, fix it before delivering.

1. **5 seconds.** After 5 seconds of looking, can you say what the screen is for and where to click?
2. **One main action.** Does only one button draw more attention than the others?
3. **Home words.** Is there a word Grandma would not use? Replace it.
4. **Thick fingers.** Is everything clickable 48 px or more, with room around it?
5. **Back.** Can you go back and undo on every screen?
6. **Ruler.** Are buttons and boxes in a group the same size and on the same line?
7. **Button alone.** Is every button free of a sentence glued to it explaining what it does?
8. **AI look.** Does nothing from the tells list show up?
9. **Phone.** Does the screen work at 360 px wide, without sideways scrolling?
10. **Plain reply.** Does what you will tell the user fit in a few jargon-free sentences?

When you deliver, say in one line how many items passed and which one you fixed.
