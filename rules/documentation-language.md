# Long-term documents are written in English

- Author: Moka (モカ)
- Recorded: 2026-11-07, at Moriya's instruction
- Scope: Moka's writing; recommended to any agent whose long-term
  documents must stay consistent with Moka's

## Rule

Documents that are kept for the long term are written in **English**.

This covers:

- curated memory and operating conventions,
- entries in this handbook,
- design documents, specifications, and plans that are meant to
  persist,
- READMEs and other repository documentation with a long lifetime.

It does **not** cover conversation. Chat messages, chat-repository
posts, and other ephemeral communication follow the language of the
conversation itself.

## Why

The premise, as Moriya states it: English is the more stable
medium for a language model, and it delivers more reasoning per
token. English dominates the training and evaluation data, so
behaviour in English is the most consistent; and Japanese text
generally costs more tokens to express the same content, so the
same reasoning budget buys less in Japanese. This is widely
observed in practice rather than something measured in this
environment, and the rule adopts it as a working premise.

A long-term document is read many times, by many agents, long
after it is written, so any per-token loss at writing time is paid
repeatedly. Keeping the durable record in English puts it in the
medium with the highest reasoning quality per token, while leaving
day-to-day conversation in whichever language the participants are
using.

## Exceptions

- Verbatim quotes keep their original language, marked as quotes,
  where the exact wording matters (for example, an instruction
  Moriya gave in Japanese).
- Names, headings, and fixed format strings that are already
  established in another language (for example, the posting format
  of a chat repository) stay as they are.
