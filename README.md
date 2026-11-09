# ADHD brain dump

Get scattered thoughts out of your head, choose a useful starting point, and work through one step at a time. If a step does not fit, the assistant helps change the approach while keeping unfinished work available in the conversation.

This is a free, standalone assistant skill from [Donna](https://meetdonna.xyz). You do not need a Donna account or an ADHD diagnosis to use it.

## Install in Codex

Run this command from the project where you want to use the skill:

```sh
npx skills add yuchenbigpen1/donna-skills --agent codex --skill adhd-brain-dump
```

Then invoke `$adhd-brain-dump` in Codex and type what is on your mind. You can include the dump in the same message. There is no required format.

Codex installation and behavior have been tested with authored conversations. Other assistants and additional task-app connections remain unverified. The skill can help draft work, but drafts may include reasonable assumptions. Check the details before using or sending them.

## What using it can look like

This example illustrates the flow; it is not a user testimonial or a recorded result.

> **You:** I need to send the workshop outline today. I also need groceries, and the expense claim is waiting for a receipt from Sam. The outline is the thing I want to finish first.
>
> **Assistant:** Write the three points you want people to leave the workshop understanding. Those can become the outline's main sections.
>
> **You:** Still too big. I can't decide what belongs.
>
> **Assistant:** Tell me one thing you want someone to be able to do after the workshop. We can build from that.

You can ask for the whole overview, add a thought, switch priorities, skip an item, or stop. Finishing a step does not automatically mark the whole task finished. The aim is useful progress, not clearing every item.

## Existing task apps

If you start without a dump, the assistant asks whether you already have a task app you can connect or would rather type your thoughts here. Connections are optional and depend on the assistant you use and the tools available to it. This package adds no integrations.

When an authorized read is available, choose the list, project, or task to read. The skill uses that scope and does not write changes back. If a connection is unavailable or a read fails, you can paste or type instead. Voice input depends on your assistant's dictation support.

## Returning to the work

The assistant can use the history still available in the conversation. It does not create cross-chat memory. Before moving to another conversation, ask for a handoff, edit out anything you do not want to carry, and paste it into the new chat with the skill invoked.

The skill does not initiate file saves, workspace scans, account changes, messages to other people, or extra transmission of your dump. Your assistant's own data and history policies still apply. Asking it to forget an item removes the item from this workflow, not from the host's stored chat history.

This is practical help with work, not diagnosis or treatment. It does not run background reminders, timers, or monitoring.

## License

[MIT](LICENSE).
