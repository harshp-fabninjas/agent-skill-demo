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

### The agent: `post-ninja`
📁 `.claude/agents/post-ninja.md`

A worker that turns a topic into a ready-to-post social media post. Give it something like *"our AgencyOS launch"* and it will:
- Open the brand skill so it uses the right colors, font, and voice
- Write the caption
- Make an actual image file
- Do it for Instagram, LinkedIn, and X
- Drop everything into the `social-posts/` folder, ready to upload

## How a run actually goes

1. You ask: *"Make a LinkedIn post about our AgencyOS launch."*
2. Claude sees that fits `post-ninja` and hands it the task.
3. `post-ninja` opens the `fabninjas-brand-design` skill to grab the brand rules.
4. It writes the caption, builds the image, and saves both into `social-posts/`.

That's it — nothing to set up. Everything lives in the `.claude/` folder, so any teammate who opens this project in Claude Code can just ask for a post.

## See the output
The `social-posts/` folder already has real examples made this exact way — an image and a caption for each:
- `linkedin-agencyos-launch.png` + `linkedin-agencyos-launch.txt`
- `instagram-laravel-mvp.png` + `instagram-laravel-mvp-caption.txt`

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
