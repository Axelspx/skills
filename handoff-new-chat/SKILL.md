---
name: handoff-new-chat
description: Handoff the current conversation compacted to continue in a new chat in this project.
argument-hint: "What will the new chat session be used for?"
disable-model-invocation: true
---

Write a compact handoff summarizing the current conversation to continue the current work in a genuinely new Codex chat with a fresh context window within the same project.

Do not fork the current chat and do not create or save a handoff file unless explicitly requested. Return the handoff directly in the response.

The new chat should use the same current model and reasoning effort settings unless the user specified otherwise.

Include the current task, implementation state, important decisions and constraints, relevant files/artifacts, completed work, and suggested skills the next agent should call.

Do not duplicate content already captured in other artifacts (specs, plans, ADRs, issues, commits, diffs). Reference them by path or URL instead.

If the user passed arguments, treat them as the intended name or focus of the new chat and tailor the handoff accordingly.

End by instructing the next agent to verify the current repository state, load any referenced artifacts or suggested skills, and continue directly from the stated next steps rather than re-planning from scratch.
