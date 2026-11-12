# ADHD brain dump skill for Claude and ChatGPT

**Tell your AI assistant everything on your mind. Get back one thing to do.**

When everything feels urgent at once, sorting it out turns into one more task. This free, open-source ADHD brain dump skill lets you skip that part. You dump it all on your assistant (tasks, worries, half-ideas, in any order), and it keeps track of the whole pile. You get one concrete step you can start right now. When that's done, you get the next one. When it's too much, you get a smaller or different way in.

It works in the Claude and ChatGPT apps as well as coding tools like Claude Code, Codex and Cursor. No account and no diagnosis needed. [Jump to install](#install).

## What an ADHD brain dump with AI looks like

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

## Skill vs. a plain brain dump prompt

We ran an earlier version of the skill and this plain prompt through the same 20 scripted conversations, on the same model (GPT-6.1 Sol):

> Help me brain-dump whatever is on my mind. Identify the actionable items, keep track of unfinished work in this conversation, and guide me through one useful step at a time. If I get stuck, help me break it down or try another approach.

Below are the two clearest differences, word for word from the test runs (shortened). Most conversations came out about the same: a reviewer who didn't know which side was which preferred the skill in 4, the plain prompt in 1, and called 15 a tie.

### When the work is done

The person has just submitted the proposal that was their main priority. The only other thing left is a venue booking that's waiting on someone else.

<table>
<tr>
<th width="50%">Plain prompt</th>
<th width="50%">With the skill</th>
</tr>
<tr valign="top">
<td>

> **One small wrap-up step:** save a screenshot of the confirmation page or copy the confirmation number, if there is one.

Two replies later, asked to continue:

> Let's finish the small wrap-up: **save a screenshot of the proposal confirmation page**, or save the confirmation email if one arrived.

</td>
<td>

> The venue booking remains **waiting on Priya to confirm the date**. There's no other actionable work in what you've shared right now, and the sketchbook can stay a someday idea.
>
> You can stop here without adding another task.

Two replies later, asked to continue:

> The only remaining task is **booking the venue**, and that's waiting on Priya.
>
> Has Priya confirmed the date yet?

</td>
</tr>
</table>

### When you point it at a task app

The person says: "I would like to start from my connected task source."

<table>
<tr>
<th width="50%">Plain prompt</th>
<th width="50%">With the skill</th>
</tr>
<tr valign="top">
<td>

Tried to read every list at once, without asking (the test setup refused), then said:

> I couldn't access the "all tasks" view. Which specific task list would you like me to read?

</td>
<td>

Read nothing yet, and asked:

> Which list or project in your connected task source would you like me to read?

</td>
</tr>
</table>

**The skill lost one conversation.** After a correction, its draft quietly assumed the person's manager would set a launch date, when who decides was still an open question. Each conversation ran once, so treat all of this as a sign, not proof.

## Install

### Claude app (claude.ai or desktop)

Download [adhd-brain-dump.zip](https://github.com/yuchenbigpen1/donna-skills/releases/latest/download/adhd-brain-dump.zip). Then go to Settings → Capabilities, make sure code execution is on, and choose "Upload skill". Needs a Pro, Max, Team or Enterprise plan.

### ChatGPT

Download the same [zip](https://github.com/yuchenbigpen1/donna-skills/releases/latest/download/adhd-brain-dump.zip), then go to Skills → Create → Upload from your computer. Skills aren't on every ChatGPT plan yet.

Then start a new chat and dump whatever's on your mind.

### Claude Code, Codex, Cursor and other coding tools

```sh
npx skills add yuchenbigpen1/donna-skills --skill adhd-brain-dump -g
```

It asks which tools to install into, and `-g` makes it available in every project. Then start a chat and dump whatever's on your mind; saying "brain dump" or "I'm overwhelmed" usually brings the skill in. You can also call it directly with `/adhd-brain-dump` in Claude Code or `$adhd-brain-dump` in Codex.

## How well it works

Tested in November 2026 on 56 scripted conversations per model: 55 passed on Claude Sonnet 5.5 and 52 on GPT-6 Luna. The apps use the same skill file, but we haven't run the tests inside them yet. The misses were mostly overviews that left an item out, so if something seems missing, ask "what's left?".

## Questions

### Is it free?

Yes. It's MIT licensed, and you don't need a Donna account or any sign-up to use it. You only need the Claude or ChatGPT plan, or the coding tool, you're installing it into.

### Do I need an ADHD diagnosis?

No. It's for anyone whose head is full and who can't work out where to start.

### What if I can't get started on anything?

That's the case it's built for. The first step can be as small as opening a document or writing one messy sentence. If a step is still too big, it shrinks it once. If the smaller step doesn't move either, it changes the approach instead: say it out loud, let the assistant draft, or start from another end.

### Can it work from the to-do list I already keep?

If your assistant can already read your task app (through a connector you've set up), point it at a list or project. The skill reads only what you choose and never changes anything there. No connection? Paste or type the list instead.

### Does it remember me between chats?

Not on its own. It doesn't save files, send messages, or carry memory across chats. Your dump stays in the conversation you're having. To pick up later, ask for a summary of where you are and paste it into the new chat.

### Is this therapy or ADHD treatment?

No. It's practical help with getting things done.

## Made by someone with ADHD

I'm Yuchen. I have ADHD, and I've been working out how to get AI to actually help me get things done, rather than hand me a nicer list. This skill is one piece of that.

The bigger piece is [Donna](https://meetdonna.xyz/?utm_source=donna-skills&utm_medium=readme&utm_campaign=adhd-brain-dump&utm_content=about), an app built around the same idea: one page per day, one step at a time, sized to the time and energy you have. Donna remembers what you've said and done, so each day picks up from where you are. [Try it free for 14 days](https://meetdonna.xyz/sign-up?utm_source=donna-skills&utm_medium=readme&utm_campaign=adhd-brain-dump&utm_content=trial), no card needed.

## License

[MIT](LICENSE)
