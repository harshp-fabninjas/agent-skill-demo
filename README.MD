# Agent + Skill Demo

A hands-on demo that shows how **Skills** and **Agents** work in Claude Code.

## Two simple ideas

- **Skill = the knowledge.** A set of rules Claude can read and follow. On its own it doesn't *do* anything — think of it as a rulebook. Ours holds the FabNinjas brand rules.
- **Agent = the worker.** A helper you hand a task to. It does the work, and it can use a skill to do it the right way. Ours writes social posts.

This demo has one skill and one agent, wired together.

## What's inside

### The skill: `fabninjas-brand-design`
📁 `.claude/skills/fabninjas-brand-design/`

The FabNinjas brand rulebook, taken straight from the brand guidelines. It tells Claude:
- The exact brand colors
- Which font to use
- How to use the logo
- How the brand should sound

**🛠️ Try it — build your own skill**

It can be anything like a `writing-style` skill with your tone-of-voice rules.

### The agent: `post-ninja`
📁 `.claude/agents/post-ninja.md`

A worker that turns a topic into a ready-to-post social media post. Give it something like *"our AgencyOS launch"* and it will:
- Open the brand skill so it uses the right colors, font, and voice
- Write the caption
- Make an actual image file
- Do it for Instagram, LinkedIn, and X
- Drop everything into the `social-posts/` folder, ready to upload

**🛠️ Try it — build your own agent**

It can be anything like a `ppt-ninja` that builds ppt slides.

## How a run actually goes

1. You ask: *"Make a LinkedIn post about our project AgencyOS launch."*
2. Claude sees that fits `post-ninja` and hands it the task.
3. `post-ninja` opens the `fabninjas-brand-design` skill to grab the brand rules.
4. It writes the caption, builds the image, and saves both into `social-posts/`.

That's it — nothing to set up. Everything lives in the `.claude/` folder, so any teammate who opens this project in Claude Code can just ask for a post.

## How do skills and agents get triggered?

You never have to "turn them on." There are just two ways Claude reaches for one:

**1. You name it directly.**
Say it out loud and Claude uses it:
> "Use the **fabninjas-brand-design** skill and check these colors."
> "Run **post-ninja** for our AgencyOS launch."

Simple and certain — good when you want a specific one.

**2. Claude matches your request to the description (the usual way).**
Every skill and every agent has a short `description:` at the top that says *when* to use it. When your request sounds like that description, Claude picks it automatically — you don't have to know its name.

That's why *"Make a LinkedIn post about our launch"* is enough to wake up `post-ninja`, even though you never said the word "post-ninja." Your sentence matched its description, so Claude connected the dots.

**The takeaway:** the `description:` line *is* the trigger. A vague description gets missed; a clear *"Use when…"* description gets picked up at the right moment.

## See the output
The `social-posts/` folder already has real examples made this exact way — an image and a caption for each:
- `instagram-laravel-developer-hiring` + `instagram-laravel-developer-hiring-caption.txt`

## The folders
```
.claude/
  agents/
    post-ninja.md              the subagent — what it does and which skill it uses
  skills/
    fabninjas-brand-design/
      SKILL.md                 the brand rules
      palette.json             the brand colors, in code
      assets/logo/             logo + favicon files
      references/              extra detail (colors, fonts, logo usage)
social-posts/                  generated posts saves here (image + caption each)
```

## Try it
Open this project in Claude Code and ask for a post on anything, e.g.:
> "create an Instagram post about 'we are hiring laravel developer at fabninjas. with 5+ years of experience'."

## Why it's worth knowing
This is the small version of a big patterns: write your rules once as a skill, then reuse it across as many sub-agents as you need — a post-maker today, maybe a landing-page or ppt agent tomorrow, and the brand will remain the same.
