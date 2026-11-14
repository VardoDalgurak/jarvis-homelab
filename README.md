# Jarvis Homelab

I found a Packard Bell PC in the trash. It was dirty and missing a few components. I took it home, cleaned it, and fitted a stick of RAM I already had. That rescued computer is now the server for Jarvis, the personal assistant I'm building at home.

## Why I started

I wanted to pick up a conversation where I had left it. With Alexa, I often had to start over. ChatGPT remembered more of our conversations, but sometimes it lost track of a correction or a step we had already finished. I'd point it out and we could carry on, but by then we'd sometimes run the same check two or three times or installed software we didn't end up needing.

That's the problem I want to explore with Jarvis. If I say, “We already tried that on the Packard Bell, and here's what happened,” I want that experience to count the next time I ask for help. Saving the conversation is the first step. Using the right part of it at the right moment is the harder one.

## Progress update

**November 5–10, 2026:** persistent conversations, backup and restore tests, browser voice input, local Piper voices, a public project page, a successful printer test, and the first Home Assistant setup.

[Read the day-by-day development log](docs/progress/2026-11-05-to-10.md) for the results, lessons, and work still pending. The entry distinguishes recorded tests from prepared changes and reported outcomes.

## What's running on the Packard Bell

The project uses **Proxmox**, a **Debian container**, **FastAPI**, and **PostgreSQL** for the assistant and its conversation history. Jarvis uses **OpenAI's API** for AI responses and speech transcription. **Piper** provides local speech synthesis, with Spanish, English, Norwegian, and Russian voice models documented during development. **Home Assistant OS** was added in a separate virtual machine.

The public project page and personal chat have separate roles. The project page explains the build; the personal assistant holds the conversations.

These are milestones documented through November 10, rather than a live service-status page. The browser conversation and database recovery were tested. Piper integration was reported working. Printing was tested directly from the server, while printing from chat, Gmail authorization, and Home Assistant device control still require further integration and verification.

## What I'm building next

My next priorities are to make the voice experience repeatable, verify ongoing backup coverage, and connect useful services one at a time. Home Assistant integration will start with reading a device state from the chat. Email and printing should only be described as chat capabilities after their complete workflows have been tested.

I also want Jarvis to remember project decisions and corrections over time. Saving messages is already useful, but retrieving the right decision weeks later is a separate piece of work.

This repository is a public development journal. It is not yet a complete source release or installer. Private configuration, credentials, and access instructions are not included.

## How I'm learning

I started this project without experience building servers or voice assistants. I'm working with **OpenAI's GPT-6 Astra in Codex** as a step-by-step guide. It helps me choose the next step and understand the errors. I run the commands on the actual machine, test the result, and tell it when what I see differs from what we expected. I couldn't have brought Jarvis this far on my own.

I enjoy figuring this out. I hope that sharing the real process, starting with a discarded computer and a spare stick of RAM, makes this technology easier for someone else to understand, use, and enjoy.

[Support the next hardware upgrade on GoFundMe](https://gofund.me/778e57dbd)

