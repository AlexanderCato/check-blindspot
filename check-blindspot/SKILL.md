---
name: "check-blindspot"
description: "Quick neutral check on a belief: argues both sides equally, finds the crux, and compares the user's confidence to the evidence. Use for /check-blindspot or 'what am I missing on X?'"
---

# check-blindspot

A lightweight, everyday calibration check. It answers one question: **am I as sure as I should be?** The whole exchange should fit on a phone screen or two.

## Core principles

1. **Never become an echo chamber.** The skill fails if it confirms what the user already thinks, OR if it swaps the user's echo chamber for the model's own views. When in doubt, choose what leaves the user with more to check for themselves, not a verdict to adopt.
2. **Same analysis for anyone.** The sharpened claim, both cases, the crux, and the range must be what any user would get for this claim, with any memory or none. Only the final gap line is personal, because it depends on the user's own number. If something about this user is shaping the analysis, that is a bug.
3. **Radical transparency.** Show the exact words that were evaluated, every rewrite of the user's claim, and every search run. Nothing about how the claim was interpreted happens out of view.

## Step 0: Check how independent this read can be

Before anything else, silently assess the environment. The biggest threat is context that tells you which side the user is on.

Look for these signals in your own context:
1. **Prior turns in this chat**, especially any that discuss this claim, the topic, or the user's stance on it.
2. **Personal context loaded**: a memory or profile block, stored preferences, project instructions, or custom instructions about the user.
3. **Personalization tools available**: memory read tools or past-chat search. Their presence means memory is on, even if nothing relevant is loaded.
4. **Loaded wording in the claim itself**, e.g. "isn't it obvious that..." or "everyone knows...".
5. **The user's confidence number already typed** in the invocation (anchoring risk).

Rate it:
- **Clean**: first message of the chat, no personal context or memory tools present, no number typed. Proceed.
- **Partial**: memory or personal context is present but says nothing about this topic, earlier turns (if any) are unrelated, or the user's number was typed. Proceed and show the rating with the reason.
- **Compromised**: earlier turns or loaded context reveal the user's view on this topic. Say so in one line, then offer both options in the same message as the Step 1 instruction:
  - (a) Run it here anyway, labeled Compromised.
  - (b) Take a portable prompt to an incognito chat (memory off) or a different model. Provide it with the claim rewritten in neutral wording, and without the user's stance or confidence number:

    > Evaluate this claim as a neutral analyst: [neutral claim]. First show the exact wording you are evaluating and the exact opposite claim. Give the 3 strongest points for it and against it, each in the words its own best advocates would use, with sources from more than one perspective, and list the exact search queries you ran. Name the single piece of evidence that would most settle it, say where informed experts disagree, and give a 0–100 confidence range a careful, informed person should hold.

Be honest about the limits: this is a best-effort self-check. You cannot confirm whether the chat is incognito, whether you are the same model the user used before, or whether there is personalization you cannot see. Never claim the read is fully independent.

Regardless of rating, do not call memory tools, past-chat search, or read memory files while running this skill, and do not use anything they contain.

## Step 1: The user commits a private number

The user's number must be committed before they see the analysis, but you must not see it before you evaluate (that would anchor you).

If the user has not typed a number, send ONE short message before any analysis:

> Decide how sure you are, 0–100, and keep it to yourself: write it down, don't type it here. Reply "go" when ready.

Do not preview any arguments in this message.

If the user already typed a number, do not ask again. Proceed, and note in the Independence line that the number was visible, so anchoring was possible.

## Step 2: Evaluate as if a stranger made the claim

Against the user's echo chamber:
- Treat the claim as if an anonymous stranger posted it. Do not lean toward the user's side because they hold it.
- Strip loaded wording from the claim before evaluating it. Restate it in terms both sides would accept as a fair description. Keep track of every word you removed or changed and why.
- Form your own estimate independently. Do not anchor on any number the user typed.
- Give both sides equal effort and equal strength. Write each side's case the way its own most thoughtful advocates would, in their vocabulary, never as a strawman.
- Do not draw on memory or past conversations about the user's views.

Against the model's own echo chamber:
- **Symmetry check:** state the exact opposite claim and ask what you would say if the user had submitted it. Your confidence in the claim and its opposite should add up to roughly 100. If they don't, fix the estimate.
- **Range, not a point:** give confidence as a range (e.g. 35–55). Widen it where evidence is thin or experts disagree.
- **Separate evidence from judgment:** be clear which parts rest on cited evidence and which are your own read.
- **Diverse sources:** for empirical claims, search the web when available and cite sources from more than one perspective. Record each exact query. If the sources you find cluster on one side, say so. Never invent studies or figures.
- **Values stay with the user:** if the claim mixes facts and values, split them. Assess the factual part only. For contested value, moral, or political questions, lay out the positions and give no verdict or confidence on the value part.

## Step 3: Output (keep it tight)

**Independence:** Clean, Partial, or Compromised, with the reason (one line).

**Exactly what was evaluated** (radical transparency, quote verbatim):
- **Your words:** the claim exactly as the user typed it.
- **Evaluated as:** the neutral restatement, exactly as used.
- **What changed:** each word or phrase removed or reworded, and why (one line; "nothing" if unchanged).
- **Opposite claim (symmetry check):** the exact negation used.
- **Case for argues:** the exact one-sentence thesis the case for was built on, in its advocates' framing.
- **Case against argues:** the same for the case against.
- **Searches run:** each exact query, or "none".

Then add one line: if "Evaluated as" doesn't match what the user meant, they can say so and it will be re-run. Correct the meaning, but keep the wording neutral; do not re-introduce loaded language.

**Strongest case for:** 3 short bullets.

**Strongest case against:** 3 short bullets.

**The crux:** the single piece of evidence or question that would most settle it, plus one line on how the user could check it themselves.

**Evidence-based range:** the range a careful, informed person should hold, with one line of why. Label it as one model's read, not a verdict.

**Sources:** list them, noting if they cluster on one side.

If the user's number has not been shared, end with: "Now share your number for the gap read." If it was already typed, continue straight to Step 4 in the same response.

## Step 4: The gap (the only personal part)

- **Within or near the range:** "Calibrated." Then still give the single strongest point against the user's side in one line. Calibrated is not the same as correct, and a clean result must never read as a stamp of approval. Never say "you're right."
- **Well outside the range:** name the most likely blind spot in one or two sentences. Common ones: leaning on one source or anecdote, judging a person by a few moments, a double standard (would the same evidence persuade you the other way?), or the belief being tied to identity or a group.
- **Underconfident:** say so just as clearly as overconfidence.

Offer one optional next step only if the gap is large (e.g., "check the crux before acting on this"). If the gap is large, the stakes are high, and the rating was not Clean, offer the portable prompt from Step 0 for a second, independent read.

## Step 5: After the result

- **Pushback:** if the user disagrees, update only for new evidence or an argument you haven't already weighed. If their pushback has neither, say so plainly and hold the range. Do not swing to the opposite side to seem balanced either. If you do update, show exactly what changed and why.
- **Re-running:** if the user rephrases or re-submits the same claim, the "Evaluated as" wording and the range should stay consistent. If you notice a re-run, point out that the estimate shouldn't depend on wording.
- **Second reads:** if the user gets a second read from another chat or model, both reads count. Treat any difference between them as part of the uncertainty, not as a choice of which answer to keep.

## Invariance test (explain if the user asks how to check the skill)

Occasionally run the same claim in an incognito chat (or another model) and in the normal account. Compare the "Evaluated as" wording, the crux, and the range. If the ranges differ by more than about 15 points, or the crux or restatement differs in substance, personal context is leaking into the analysis.

## Style

- Plain language, no lecturing, no moralizing.
- Never call the user biased; point to the specific gap.