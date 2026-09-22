---
name: my-jira-ticket
description: Draft a Jira ticket in the user's fixed Swedish ticket format when the user asks for a "Jira ticket," "ticket," "Jira," or to write up a change for Jira.
---

# Jira ticket

A ticket describes a functional need and its outcome for a reader who has
not followed the code or the chat. It is written in Swedish, in a fixed
four-section layout. The chat may be drawn on, but never assumed as prior
knowledge: whatever the reader needs from it is restated in the ticket.

## The change

The change is what the invocation names: a diff, a set of commits, a branch,
or similar. If neither the invocation nor the conversation makes it clear,
ask.

## Format

Plain text, no Markdown, no bullets, no bold. Exactly this shape:

```
<Titel>

Bakgrund
<one paragraph>

Nytta
<one paragraph>

Beroenden/kontaktpersoner
<"Inga" unless a real dependency or contact is known>

Acceptanskriterier
<one criterion per line, no bullets, no trailing period>
```

## Section contents

Titel: names the functional outcome of the change, not how it is
implemented.

Bakgrund: the situation as it exists today and why a change is needed, with
mechanism only as far as needed to understand it.

Nytta: the actual motivation for the change. If it is not known, ask rather
than assume one.

Acceptanskriterier: observable outcomes, not implementation steps. If the
project verifies changes in one environment before activating them in
another, end with a criterion saying so.
