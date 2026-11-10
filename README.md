# ADHD brain dump

**Tell your AI assistant everything on your mind. Get back one thing to do.**

When everything feels urgent at once, sorting it out turns into one more task. This skill lets you skip that part. You dump it all on your assistant (tasks, worries, half-ideas, in any order), and it keeps track of the whole pile. You get one concrete step you can start right now. When it's done, you get the next one. When it's too much, you get a smaller or different way in.

It's free and open source, and works in the Claude and ChatGPT apps as well as coding tools like Claude Code, Codex and Cursor. No account and no diagnosis needed.

## What it's like

> **You:** ok. rent is due friday and I haven't moved the money over. need to reply to Priya about the offsite. dentist, I keep forgetting to book it. half-written blog post. laundry. honestly I just feel behind on everything
>
> **Assistant:** That's a lot at once. Rent has the only hard deadline, so start there: open your banking app and move the rent money over. I'm holding the rest (Priya, the dentist, the blog post, laundry) for after.
>
> **You:** done. the blog post is the one that's actually bugging me but I can't face it
>
> **Assistant:** Then don't face the whole thing. Open the draft and write one rough sentence about what the post is trying to say. It doesn't have to be good.
>
> **You:** still too much
>
> **Assistant:** Try it out loud instead: tell me in a message what you'd say if a friend asked what the post is about. I'll turn that into an opening you can edit.

That conversation is made up, but it's how the skill behaves.

## How it's different from just asking a chatbot

A plain assistant can turn a list into steps. This skill changes what happens after that:

- **It holds the whole pile.** Ask "what's left?" any time and you get everything, grouped: in progress, not started, waiting on someone, set aside. Then it goes back to one step.
- **Feelings and someday-ideas stay what they are.** "I should learn pottery" doesn't become an assignment.
- **Stuck gets a new way in.** First a smaller step. If that still won't move, a different approach: say it out loud, let the assistant draft, start from another end.
- **Nothing gets ticked off early.** Opening the report isn't finishing it, so the rest of it stays held for you.
- **You can always pass.** Skip something, drop it, or say stop. It won't argue you back into it.
- **A new chat isn't a fresh start.** Ask for a summary of where you are, paste it into the new chat, and carry on.

## Install

**Claude app (claude.ai or desktop):** download [adhd-brain-dump.zip](https://github.com/yuchenbigpen1/donna-skills/releases/latest/download/adhd-brain-dump.zip). Then go to Settings → Capabilities, make sure code execution is on, and choose "Upload skill". Needs a Pro, Max, Team or Enterprise plan.

**ChatGPT:** download the same [zip](https://github.com/yuchenbigpen1/donna-skills/releases/latest/download/adhd-brain-dump.zip), then go to Skills → Create → Upload from your computer. Skills aren't on every ChatGPT plan yet.

Then start a new chat and dump whatever's on your mind.

**Claude Code, Codex, Cursor and other coding tools:**

```sh
npx skills add yuchenbigpen1/donna-skills --skill adhd-brain-dump -g
```

It asks which tools to install into, and `-g` makes it available in every project. Then start a chat and dump whatever's on your mind; saying "brain dump" or "I'm overwhelmed" usually brings the skill in. You can also call it directly with `/adhd-brain-dump` in Claude Code or `$adhd-brain-dump` in Codex.

Tested in November 2026 on 56 scripted conversations per model: 55 passed on Claude Sonnet 5.5 and 52 on GPT-6 Luna. The apps use the same skill file, but we haven't run the tests inside them yet. The misses were mostly overviews that left an item out, so if something seems missing, ask "what's left?".

## Already keep a to-do list somewhere?

If your assistant can already read your task app (through a connector you've set up), point it at a list or project. The skill reads only what you choose and never changes anything there. No connection? Paste or type the list instead.

## What it won't do

It doesn't save files, send messages, or remember across chats on its own (that's what the summary is for). Your dump stays in the conversation you're having. It's practical help with getting things done, not therapy or treatment.

## Made by someone with ADHD

I'm Yuchen. I have ADHD, and I've been working out how to get AI to actually help me get things done, rather than hand me a nicer list. This skill is one piece of that.

The bigger piece is [Donna](https://meetdonna.xyz/?utm_source=donna-skills&utm_medium=readme&utm_campaign=adhd-brain-dump&utm_content=about), an app built around the same idea: one page per day, one step at a time, sized to the time and energy you have. Donna remembers what you've said and done, so each day picks up from where you are. [Try it free for 14 days](https://meetdonna.xyz/sign-up?utm_source=donna-skills&utm_medium=readme&utm_campaign=adhd-brain-dump&utm_content=trial), no card needed.

## License

[MIT](LICENSE)
