# /check-blindspot

**Am I as sure as I should be?** A skill for Claude and ChatGPT that gives any belief a fair, two-sided read and checks whether your confidence matches the evidence.

```text
/check-blindspot your belief
```

**[Download for Claude (.zip)](https://github.com/AlexanderCato/check-blindspot/releases/latest/download/check-blindspot.zip)** · **[Download SKILL.md for ChatGPT](https://github.com/AlexanderCato/check-blindspot/releases/latest/download/SKILL.md)** · [Install](#install) · [Example](#example-run) · [How it works](#how-it-works) · [Limitations](#limitations)

`one command` · `both sides argued equally` · `shows every word it used` · `Claude or ChatGPT`

---

## What it does

Tell it something you believe, in your own words. In about two minutes you get:

- **What it checked:** your exact words, the neutral wording it actually checked, and what it changed and why.
- **How sure the evidence lets you be:** a 0–100 range a careful, informed person should hold, with what sets each end of it.
- **What it comes down to:** the single fact that would most settle the question, and how to check it yourself.
- **The best case for and against**, each argued the way its own best advocates would.
- **Your number vs. the evidence:** how the number you picked privately compares with that range.

The detailed working (the opposite claim it tested, every search, every source, and a setup check) comes at the end, for anyone who wants it.

| It does | It doesn't |
| :-- | :-- |
| Argue both sides the way their best advocates would | Tell you you're right |
| Name the single fact that would settle it | Decide moral or political values for you |
| Give a confidence range, with reasons | Read your saved memory or past chats |
| Show exactly how it read your claim | Replace real research for big decisions |

## Quick start

1. [Install it](#install) in Claude or ChatGPT.
2. In a new chat, type `/check-blindspot` followed by your belief, written the way you'd say it. Don't say how sure you are.
3. It asks you to pick a number from 0 to 100 **and keep it to yourself**. Write it down, then reply `go`.
4. Read the result. The answer comes first; the working is at the end.
5. Share your number. You'll hear whether it fits the evidence, or what your most likely blind spot is.

Typing `/check-blindspot` is the most reliable way to start it. Plain questions like `What am I missing on [your belief]?` usually work too.

**Useful follow-ups**

- **"That's not what I meant. I meant…"** It re-runs with your meaning, still in neutral wording.
- **Push back with new evidence.** It updates the range and shows exactly what changed. Push back without new evidence and it holds its ground.
- **"Give me the portable prompt."** You get a neutral version of the check to paste into a temporary chat or a different AI for a second read.

## Example run

> Real output from one run in an incognito chat. The reader's 80 is an example number.

**You:** `/check-blindspot Trees get most of their material from the ground.`

**Claude:** Decide how sure you are, 0–100, and keep it to yourself: write it down, don't type it here. Reply "go" when ready.

**You:** `go`

<details>
<summary><b>Claude's result</b> (click to expand)</summary>

<br>

### What I checked
- **You said:** "Trees get most of their material from the ground."
- **I checked:** "Most of a tree's mass comes from what its roots take up from the ground (water and minerals), rather than from the air."
- **What I changed and why:** "material" → "mass," so it can be weighed. "The ground" → "water and minerals," so both sides agree on what counts as coming from the ground.

*Neutral wording gives both sides a fair hearing. If I changed your meaning, tell me and I'll re-run it.*

### How sure the evidence lets you be: **10–30** out of 100
**Why:** Read plainly, "material" means what the tree is built from, the wood itself, and about half of dry wood is carbon pulled from the air while soil minerals make up only around 1%.

**Why not lower:** If you count the water a living tree holds, which is half or more of its weight and all of it comes up from the ground, the claim becomes mostly true, and that reading sets the top of the range.

*This is one AI's read, not a final ruling.*

> **What it comes down to:** Whether you count the water inside a living tree, or only the dry wood.
>
> **Check it yourself:** Weigh a fresh-cut branch, dry it in a low oven for a day, and weigh it again to see how much was water.

### Best case for
- **A living tree is mostly water from the ground.** Actively growing tissues like leaves and root tips are about 75–90% water, trunk wood is about 45–60% water, and roughly half to two-thirds of a tree's mass is water. All of that comes up through the roots.
- **Even dry wood carries atoms from ground water.** All the hydrogen in wood comes from water, and dry wood is about 6% hydrogen and 44% oxygen. Tree-ring studies find that while wood is being built, a large share of its oxygen swaps places with root water: about 40% in one pine study, and around 70% on average at some alpine sites.
- **The soil part is small but can't be skipped.** Wood also contains small amounts of minerals such as calcium, potassium, sodium, magnesium, iron and manganese, all from the soil, and the tree can't grow without them.

### Best case against
- **The solid stuff is mostly carbon from the air.** Dry wood is about 50% carbon, with only trace amounts of minerals. Every bit of that carbon comes from carbon dioxide gas that enters through the leaves.
- **The soil barely shrinks as a tree grows.** In the classic 1600s experiment, a willow grew from 5 pounds to 169 pounds over five years, while the dry weight of its soil dropped by only 2 ounces.
- **Minerals are a tiny share of the wood.** The ash left after fully burning wood ranges from about 0.08% to 2.3%, and that ash is roughly everything the soil itself contributed.

---

#### Show my work

**Opposite claim I tested:** "Most of a tree's mass comes from the air, rather than from what its roots take up from the ground."

I put this at 70–90. My confidence in this and in your claim should add up to about 100.

**Each side's main argument**
- **For:** A living tree is mostly water, and that water, plus some of the atoms locked into wood, comes from the ground.
- **Against:** The dry, solid part of a tree is about half carbon from the air, and the soil contributes only a percent or two.

**Searches I ran**
1. "where does a tree's mass come from carbon dioxide air"
2. "wood elemental composition carbon hydrogen oxygen ash percent dry weight"
3. "green wood moisture content percent water living tree weight"
4. "van Helmont willow tree experiment soil weight result"
5. "tree ring cellulose oxygen isotope exchange with source water carbonyl"

**Sources**
- [Wood chemistry chapter, USDA Forest Service](https://research.fs.usda.gov/treesearch/22043): government research reference
- [Where does a tree's mass come from? Teacher notes](https://ns1.serendipstudio.org/exchange/files/PlantMassFromTN.pdf): classroom teacher notes
- [van Helmont, Jan](https://encyclopedia.com/science/news-wires-white-papers-and-books/van-helmont-jan): reference encyclopedia
- [Wood properties course material](https://www.hnee.de/_obj/CD8F42A0-B396-40E7-9F36-FF60A55DEFF7/outline/5%20Eures_WoodPropertiesPDF.pdf): university course material
- [Wood composition summary](https://lenz.io/c/93139f1c): compiled summary of wood-science sources
- [EGU 2011 abstract on tree-ring isotopes](https://meetingorganizer.copernicus.org/EGU2011/EGU2011-2564.pdf): research conference abstract
- [EGU 2011 abstract, alpine sites](https://meetingorganizer.copernicus.org/EGU2011/EGU2011-11690.pdf): research conference abstract

Most sources on this topic are classroom explainers teaching the "trees come from air" answer, so I leaned on wood-science and research sources for both sides; no source I found argues your claim directly.

**Notes**
- The "for" case is pieced together from wood-science and tree-ring research, not from anyone making the claim outright.
- From my own knowledge, not the sources: oxygen in sugars also trades places with leaf water during photosynthesis, so the share of wood's oxygen that traces back to water could be higher than the trunk-level figures. School lessons usually count that oxygen as coming from carbon dioxide instead, so how you count it depends on the bookkeeping.
- Carbon from the air alone is about half of dry wood, so even with the most generous oxygen counting, the dry-wood reading stays close to a split rather than clearly "most from the ground."

**Setup check:** All clear. This is an incognito chat with no memory, there are no earlier messages about this topic, and your number wasn't typed. I can't rule out personalization I can't see.

---

**Your turn:** share your number and I'll tell you how it compares.

</details>

**You:** `80`

**Claude:** **You're more sure than the evidence supports.** Your 80 vs. 10–30.

**Likely blind spot:** The everyday picture of roots "feeding" a tree makes it feel like the solid wood must come from the solid ground, but about half of dry wood is carbon pulled out of thin air. Your number only fits if you mean the tree's living weight, water included.

**Next step:** Decide which you mean, dry wood or living weight with water, before relying on this, since the answer flips depending on which one you pick.

## How it works

A skill is a set of written instructions the AI follows when you call it. This one is a single file, [`check-blindspot/SKILL.md`](check-blindspot/SKILL.md), built on four rules:

| Never an echo chamber | Same analysis for anyone | Radical transparency | Plain and clear |
| :-- | :-- | :-- | :-- |
| It shouldn't echo your views back to you, or quietly swap them for the AI's own. | Anyone who checks the same claim should get the same analysis. Only the final comparison depends on you. | Every rewrite of your claim and every search is shown, word for word. | The answer comes first, in everyday words. The detailed working comes last. |

**What happens on each run**

1. **Checks the setup.** It looks for anything that reveals your side, like earlier messages about the topic or a number you typed. It never reads your memory or past chats while it runs.
2. **Has you commit a number in private.** The AI can't be pulled toward a number it hasn't seen, and you can't quietly change yours after reading the arguments.
3. **Reads your claim as if a stranger said it.** It rewords loaded language into terms both sides would accept, builds each case the way its best advocates would, and searches for each side's strongest case when web search is on.
4. **Tests itself.** It asks what it would say about the opposite claim (the two confidence levels should add up to about 100), anchors the range on the plain reading of your claim, and names what sets each end.
5. **Compares the range to your number.** If your number fits, it still gives you the strongest point against your side, since fitting the evidence isn't the same as being right. If not, it names your most likely blind spot. Being too unsure gets flagged too. It never says "you're right."

**The setup check**

Every result ends with a setup check, under "Show my work":

| Status | What it means | What it does |
| :-- | :-- | :-- |
| **All clear** | Nothing in the chat shows where you stand on this topic. Having memory turned on doesn't change this. | Runs normally |
| **Mostly clear** | Something could nudge the read a little, like typing your number before the result | Runs, and says what it was |
| **Heads-up** | Earlier messages or saved info show where you stand on this topic | Tells you before it starts, and offers a neutral prompt to use in a fresh or temporary chat |

## Install

> [!IMPORTANT]
> Use the downloads from the Releases page: **[check-blindspot.zip](https://github.com/AlexanderCato/check-blindspot/releases/latest/download/check-blindspot.zip)** for Claude, or **[SKILL.md](https://github.com/AlexanderCato/check-blindspot/releases/latest/download/SKILL.md)** for ChatGPT. GitHub's green **Code → Download ZIP** button packages the whole repository, which isn't laid out the way Claude expects a skill upload.

### Claude

> [!NOTE]
> Install it from a web browser or the desktop app, not the Claude phone app. On a phone, open claude.ai in Safari or Chrome and sign in. Once it's installed, it works in the app too.

**Before you start**

- A Claude account on the Free, Pro, Max, Team or Enterprise plan
- File creation turned on: **Settings → Capabilities → Create and edit files** (older menus call it "Code execution and file creation")
- `check-blindspot.zip`, still zipped

**Steps**

1. On claude.ai or in the desktop app, go to **Customize → Skills**.
2. Click **+**, then **Create skill**.
3. Choose **Upload a skill** and select `check-blindspot.zip`. Don't unzip it first.
4. Find **check-blindspot** in your skills list and make sure its toggle is on.
5. Start a new chat and try it:

   ```text
   /check-blindspot breakfast is the most important meal of the day
   ```

### ChatGPT

Works on every ChatGPT plan, Free included, through a Project. Set it up at chatgpt.com in a web browser; after that, the project is there in the app too. Free plans allow 5 files per project, and this uses 1.

1. Download **[SKILL.md](https://github.com/AlexanderCato/check-blindspot/releases/latest/download/SKILL.md)**. It's the same instructions Claude uses, in one plain-text file.
2. In the ChatGPT sidebar, click **New project** and name it **check-blindspot**.
3. Open the project and add `SKILL.md` to its files. Don't paste it into a chat.
4. Start a new chat **inside the project** and try it:

   ```text
   /check-blindspot breakfast is the most important meal of the day
   ```

### Claude Code

Copy the skill folder into your personal skills directory:

```bash
git clone https://github.com/AlexanderCato/check-blindspot.git
mkdir -p ~/.claude/skills
cp -r check-blindspot/check-blindspot ~/.claude/skills/
```

Start a new session and type `/check-blindspot`. To install it for a single project instead, copy the folder into that project's `.claude/skills/` directory.

### Other AI tools

`SKILL.md` follows the open [Agent Skills](https://agentskills.io) format, so the folder can be loaded by other tools that support it. It has been tested with Claude and ChatGPT. Steps that involve memory or web search depend on what the tool offers.

### If something's off

- **No Customize or Skills option in Claude:** turn on file creation in Settings → Capabilities, and use a browser rather than the phone app. On Team or Enterprise plans, an admin may need to enable skills.
- **Claude doesn't use the skill:** check that the toggle is on, start a new chat, and type `/check-blindspot` with the slash.
- **ChatGPT doesn't follow the steps:** make sure the chat is inside the project and `SKILL.md` is in the project's files. Then start a new chat there.

### Look inside first

The skill is one plain-text instruction file with no code or scripts. Since it comes from someone else, [read `SKILL.md`](check-blindspot/SKILL.md) before you use it. It takes a few minutes.

### Updating

Updates don't arrive on their own. To hear about new versions, click **Watch → Custom → Releases** at the top of this page. To update in Claude, remove the old copy from your skills list and upload the new ZIP. In ChatGPT, replace `SKILL.md` in the project's files.

## Limitations

- **It's one AI's read.** The range is an informed estimate, not a ruling. Check the sources yourself before acting on anything important.
- **It can't fully confirm its own setup.** It sees what's in the chat, but it can't confirm a chat is temporary or rule out personalization it can't see. For high-stakes beliefs, run it in a temporary chat or a different AI.
- **Results vary a little between runs.** Wording changes, and the range can move a few points. A big swing on the same claim is a warning sign.
- **Sources depend on web search.** With web search off, it works from general knowledge and can't cite current sources.
- **It won't decide values for you.** For moral or political questions it separates facts from values, checks the facts, and lays out the positions on the rest without picking a side.
- **It's built to be quick.** For big decisions, treat it as the start of your research.
- **You choose what to test.** If you only check beliefs you already doubt, it can't help with the ones that matter most.

## Check the skill itself

You can test whether personal context is leaking into the analysis. Run the same claim in a temporary or incognito chat (or another AI) and in your normal account, then compare the **I checked** wording, **what it comes down to**, and the range. If the ranges differ by more than about 15 points, or the rewording or what it comes down to differs in substance, something about you is shaping a result that should be the same for everyone.

If you find a case like that, or a run where one side was argued as a strawman, please [open an issue](https://github.com/AlexanderCato/check-blindspot/issues) with the claim and both results.

## Repository layout

```text
check-blindspot/
├── check-blindspot/
│   └── SKILL.md     ← the skill
├── LICENSE
└── README.md
```

Each [release](https://github.com/AlexanderCato/check-blindspot/releases) attaches two files: `check-blindspot.zip` (the inner `check-blindspot/` folder, zipped, for Claude) and `SKILL.md` (the same file on its own, for ChatGPT).

## License

[MIT](LICENSE) © 2026 Alexander Cato

This is an independent project, not affiliated with or endorsed by Anthropic or OpenAI. Install steps follow Claude's Help Center article [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude) and OpenAI's [Projects in ChatGPT](https://help.openai.com/en/articles/10169521-projects-in-chatgpt); menus may change over time.

---

**The best habit:** run `/check-blindspot` most often on the beliefs that feel most obviously true.
