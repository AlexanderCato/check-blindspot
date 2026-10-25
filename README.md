# /check-blindspot

**Am I as sure as I should be?** A Claude skill that gives any belief a fair, two-sided read and checks whether your confidence matches the evidence.

```text
/check-blindspot your belief
```

**[Download check-blindspot.zip](https://github.com/AlexanderCato/check-blindspot/releases/latest/download/check-blindspot.zip)** · [Install](#install) · [Example](#example-run) · [How it works](#how-it-works) · [Limitations](#limitations)

`one command` · `both sides argued equally` · `shows every word it used` · `one text file, no code`

---

## What it does

Tell it something you believe, in your own words. In about two minutes you get:

- **The strongest case for and against**, each argued the way its own best advocates would argue it.
- **The crux:** the single fact that would most settle the question, and how you could check it yourself.
- **An evidence-based range:** the 0–100 confidence a careful, informed person should hold.
- **The gap:** how the number you committed to privately compares with that range.

| It does | It doesn't |
| :-- | :-- |
| Argue both sides the way their best advocates would | Tell you you're right |
| Name the single fact that would settle it | Decide moral or political values for you |
| Give a confidence range, with reasons | Read your saved memory or past chats |
| Show exactly how it read your claim | Replace real research for big decisions |

Use it when you feel most certain: in the middle of a debate, just before you repeat something to someone, or right after you read something that told you exactly what you wanted to hear.

## Quick start

1. [Install the skill](#install).
2. In a new chat, type `/check-blindspot` followed by your belief, written the way you'd say it. Don't say how sure you are.
3. Claude asks you to pick a number from 0 to 100 **and keep it to yourself**. Write it down, then reply `go`.
4. Read the result: the exact wording it evaluated, both cases, the crux, and the range.
5. Share your number. You get **Calibrated**, or the most likely blind spot behind the gap.

Typing `/check-blindspot` is the most reliable way to start it. Plain questions like `What am I missing on [your belief]?` usually work too.

**Useful follow-ups**

- **"That's not what I meant. I meant…"** It re-runs with your meaning, still in neutral wording.
- **Push back with new evidence.** It updates the range and shows exactly what changed. Push back without new evidence and it holds its ground.
- **"Give me the portable prompt."** You get a neutral version of the check to paste into an incognito chat or a different AI model for a second, independent read.

## Example run

> Real output from one run, lightly edited for readability. The reader's 80 is an example number.

**You:** `/check-blindspot Trees get most of their material from the ground.`

**Claude:** Decide how sure you are, 0–100, and keep it to yourself: write it down, don't type it here. Reply "go" when ready.

**You:** `go`

<details>
<summary><b>Claude's result</b> (click to expand)</summary>

<br>

**Independence:** Clean. Fresh chat, no personal context, no number typed.

**Exactly what was evaluated**

| Item | Exactly as used |
| :-- | :-- |
| **Your words** | "Trees get most of their material from the ground." |
| **Evaluated as** | "Most of a tree's mass comes from substances it takes up from the soil through its roots (water and minerals), rather than from the air." |
| **What changed** | "Material" became "mass" so it can be measured. "From the ground" was spelled out as soil uptake through roots, so water counts as from the ground. Left open whether "mass" means fresh weight (with water) or dry weight, because the answer turns on that. |
| **Opposite claim** | "Most of a tree's mass does not come from substances taken up from the soil; it comes mainly from the air." |
| **Case for argues** | "A living tree, weighed as it stands, is largely water drawn up from the soil, plus soil minerals, so the ground supplies most of its mass." |
| **Case against argues** | "The solid stuff a tree is built from is mostly carbon and oxygen taken from CO2 in the air, so trees are mostly made of air." |

**Searches run**

- `where does a tree's mass come from carbon dioxide air soil`
- `tree dry weight elemental composition carbon oxygen hydrogen minerals percent`
- `green wood moisture content percent of fresh weight living tree water`
- `van Helmont willow tree experiment soil weight lost`
- `living tree percent water by weight fresh biomass`

If "Evaluated as" isn't what you meant, say so and I'll re-run it. Correct the meaning, but the wording will stay neutral.

**Strongest case for**

- A living tree is about 50% water by weight on average. Fresh aspen wood is over 65% water and leaves are 77–90%+. Almost all of that water comes up through the roots from the soil.
- Green wood can hold anywhere from under 30% to over 200% of its dry weight in water. In wet species, water from the ground is literally most of what you'd put on a scale.
- The hydrogen in wood (about 6% of dry mass) comes from water, and all the nitrogen and minerals come from soil. Van Helmont, after his famous 1648 willow experiment, concluded the tree's mass came from water.

**Strongest case against**

- Dry wood is about 50% carbon, 42–44% oxygen, about 6% hydrogen, and less than 1% ash/minerals. The carbon, and most of the oxygen, comes from CO2 in the air through photosynthesis.
- In van Helmont's experiment the willow gained about 74 kg over five years, while the soil lost only about 57 grams. Soil contributes almost nothing in bulk.
- The water in a tree passes through it rather than being built in. Most of it is transpired, and the amount changes with season and tissue. The permanent structure of wood, bark, and roots is about 90%+ air-derived by dry weight.

**The crux:** it depends on what you mean by "material."

- *Just the solid tree* (wood, bark and leaves, dried out): only about 5–10% comes from the ground. The rest came from the air.
- *The whole living tree, water included:* it's close to half and half, and in wetter trees the ground can come out ahead, because the water is pulled up from the soil.

*Try it yourself:* weigh a fresh branch, dry it in a low oven until the weight stops dropping, then weigh it again. The weight it lost was water from the ground. About half of what's left is carbon that came from the air.

**Evidence-based range: 10–25 out of 100** that the claim is true.

- *Why so low:* when scientists and teachers talk about what a tree is "made of," they usually mean the solid part, and by that measure the claim is mostly wrong.
- *Why not zero:* counting the water is also a fair way to read the claim.

This is one AI's read, not a final ruling.

**Sources**

- [Where does a Tree get its Mass?](https://genwise.substack.com/p/where-does-a-tree-get-its-mass) (GenWise, Substack)
- [What Elements Are in Wood? From Atoms to Molecules](https://scienceinsights.org/what-elements-are-in-wood-from-atoms-to-molecules/) (ScienceInsights)
- [Wood Species – Moisture Content and Weight](https://www.engineeringtoolbox.com/weigt-wood-d_821.html) (Engineering ToolBox)
- [How Much of a Tree Is Water?](https://biologyinsights.com/how-much-of-a-tree-is-water/) (BiologyInsights)
- [Jan Baptist van Helmont](https://en.wikipedia.org/wiki/Jan_Baptist_van_Helmont) (Wikipedia)

*About the sources:* the "made of air" view is everywhere in popular explainers, while support for the claim comes mainly from water-content and wood-engineering sources. These are explainers and reference pages, not peer-reviewed primary studies.

Now share your number for the gap read.

</details>

**You:** `80`

**Claude:** **Gap:** Your 80 is well above the evidence-based range of 10–25. That's overconfident.

**Most likely blind spot:** You may be picturing roots "feeding" the tree with soil, the way a stomach takes in food. That picture is intuitive, but it's the one van Helmont's own measurements ruled out: 74 kg of growth for 57 grams of soil. The claim only gets close to true if you count the water the tree is holding at the moment.

**Optional next step:** Check the crux before relying on this. Decide whether you mean dry structure or live weight with water, then try the branch-drying test.

## How it works

A skill is a set of written instructions Claude follows when you call it. This one is a single file, [`check-blindspot/SKILL.md`](check-blindspot/SKILL.md), built on three rules:

| Never an echo chamber | Same analysis for anyone | Radical transparency |
| :-- | :-- | :-- |
| It shouldn't echo your views back to you, or quietly swap them for Claude's own. | Anyone who checks the same claim should get the same analysis. Only the final gap line depends on you. | Every rewrite of your claim and every search is shown, word for word. |

**What happens on each run**

1. **Checks how independent it can be.** It looks for anything that reveals your side: earlier messages about the topic, saved memory or profile details, loaded wording in your claim, or a number you typed. It rates the setup (below) and never reads your memory or past chats while it runs.
2. **Has you commit a number in private.** Claude can't be pulled toward a number it hasn't seen, and you can't quietly revise yours after reading the arguments.
3. **Reads your claim as if a stranger made it.** It rewrites loaded wording into terms both sides would accept, builds each case the way its best advocates would, and searches sources from more than one perspective when web search is on.
4. **Tests itself.** It asks what it would say about the opposite claim (the two confidence levels should add up to about 100) and gives a range that widens when evidence is thin.
5. **Compares the range to your number.** In or near the range, it says *Calibrated* and still gives you the strongest point against your side, since calibrated isn't the same as correct. Far outside, it names the most likely blind spot. Underconfidence gets flagged too. It never says "you're right."

**Independence ratings**

| Rating | What it means | What it does |
| :-- | :-- | :-- |
| **Clean** | Fresh chat, no personal context or memory, no number typed | Runs normally |
| **Partial** | Memory or personal context is present but unrelated, or you typed your number | Runs, and says why it's Partial |
| **Compromised** | The chat or your memory already shows where you stand on this topic | Offers a neutral prompt for an incognito chat or a different model, or runs anyway with the label |

## Install

> [!IMPORTANT]
> Use the **[check-blindspot.zip](https://github.com/AlexanderCato/check-blindspot/releases/latest/download/check-blindspot.zip)** from the Releases page. GitHub's green **Code → Download ZIP** button packages the whole repository, which isn't laid out the way Claude expects a skill upload.

### Claude (web, desktop and mobile)

**Before you start**

- A Claude account on the Free, Pro, Max, Team or Enterprise plan
- Code execution turned on in your Claude settings (skills need it)
- `check-blindspot.zip`, still zipped

**Steps**

1. In Claude on the web or the desktop app, go to **Customize → Skills**.
2. Click **+**, then **Create skill**.
3. Choose **Upload a skill** and select `check-blindspot.zip`. Don't unzip it first.
4. Find **check-blindspot** in your skills list and make sure its toggle is on.
5. Start a new chat and try it:

   ```text
   /check-blindspot breakfast is the most important meal of the day
   ```

Once installed, it works on web, desktop and mobile.

<details>
<summary><b>If something's off</b></summary>

<br>

- **No Customize or Skills option:** make sure code execution is turned on. On Team or Enterprise plans, an admin may need to enable skills.
- **Claude doesn't use the skill:** check that the toggle is on, start a new chat, and type `/check-blindspot` with the slash.
- **On a Team or Enterprise plan:** once it's installed, you may be able to share it with colleagues from your skills list, if your organization allows sharing.

</details>

### Claude Code

Copy the skill folder into your personal skills directory:

```bash
git clone https://github.com/AlexanderCato/check-blindspot.git
mkdir -p ~/.claude/skills
cp -r check-blindspot/check-blindspot ~/.claude/skills/
```

Start a new session and type `/check-blindspot`. To install it for a single project instead, copy the folder into that project's `.claude/skills/` directory.

### Other AI tools

`SKILL.md` follows the open [Agent Skills](https://agentskills.io) format, so the folder can be loaded by other tools that support it. It has only been tested with Claude, and steps that involve memory or web search depend on what the tool offers.

### Look inside first

The skill is one plain-text instruction file with no code or scripts. Since it comes from someone else, [read `SKILL.md`](check-blindspot/SKILL.md) before you turn it on. It takes a few minutes.

### Updating

Updates don't arrive on their own. To hear about new versions, click **Watch → Custom → Releases** at the top of this page. To update, remove the old copy from your skills list and upload the new ZIP.

## Limitations

- **It's one AI's read.** The range is an informed estimate, not a ruling. Check the crux and the sources yourself before acting on anything important.
- **It can't fully confirm its own independence.** It can see what's in the chat, but it can't confirm a chat is incognito or rule out personalization it can't see. For high-stakes beliefs, run it in an incognito chat or on a different AI model.
- **Results vary a little between runs.** Wording changes, and the range can move a few points. A big swing on the same claim is a warning sign.
- **Sources depend on web search.** With web search off, it works from general knowledge and can't cite current sources.
- **It won't decide values for you.** For moral or political questions it separates facts from values, assesses the facts, and lays out the positions on the rest without picking a side.
- **It's built to be quick.** For major decisions, treat it as the start of your research.
- **You choose what to test.** If you only check beliefs you already doubt, it can't help with the ones that matter most.

## Check the skill itself

You can test whether personal context is leaking into the analysis. Run the same claim in an incognito chat (or another model) and in your normal account, then compare the **Evaluated as** wording, the crux, and the range. If the ranges differ by more than about 15 points, or the crux or restatement differs in substance, something about you is shaping a result that should be the same for everyone.

If you find a case like that, or a run where one side was argued as a strawman, please [open an issue](https://github.com/AlexanderCato/check-blindspot/issues) with the claim and both results.

## Repository layout

```text
check-blindspot/
├── check-blindspot/
│   └── SKILL.md     ← the skill
├── LICENSE
└── README.md
```

Each [release](https://github.com/AlexanderCato/check-blindspot/releases) attaches `check-blindspot.zip`, which is the inner `check-blindspot/` folder, zipped.

## License

[MIT](LICENSE) © 2026 Alexander Cato

This is an independent project, not affiliated with or endorsed by Anthropic. Install steps follow Claude's Help Center article [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills); menus may change over time.

---

**The best habit:** run `/check-blindspot` most often on the beliefs that feel most obviously true.
