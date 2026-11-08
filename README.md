# Jarvis Homelab

I found a Packard Bell PC in the trash. It was dirty and missing a few components. I took it home, cleaned it, and fitted a stick of RAM I already had. That rescued computer is now the server for Jarvis, the personal assistant I'm building at home.

## Why I started

I wanted to pick up a conversation where I had left it. With Alexa, I often had to start over. ChatGPT remembered more of our conversations, but sometimes it lost track of a correction or a step we had already finished. I'd point it out and we could carry on, but by then we'd sometimes run the same check two or three times or installed software we didn't end up needing.

That's the problem I want to explore with Jarvis. If I say, “We already tried that on the Packard Bell, and here's what happened,” I want that experience to count the next time I ask for help. Saving the conversation is the first step. Using the right part of it at the right moment is the harder one.

## What's running on the Packard Bell

The PC runs **Proxmox**. Inside it, a **Debian 13 container** runs Jarvis. **FastAPI** serves the chat, **PostgreSQL 17** stores the conversations, and **Cloudflare** lets me reach it from my phone when I'm away. The server and its memory live at home. Jarvis uses OpenAI's API for AI responses and speech transcription.

One test I can already repeat: I speak into my SteelSeries Arctis Nova 7 headset, see the words appear in the browser, and send the message. Jarvis replies in writing and saves the exchange.

## What I'm building next

First, I want to sign in once and return to the same conversation on my phone or PC. Then I want to put the headset down, say “Jarvis” from my desk, and hear an answer through a speaker connected to the Packard Bell. I'll document the tests here, including the ones that don't work.

## How I'm learning

I started this project without experience building servers or voice assistants. I'm working with **OpenAI's GPT-6 Astra in Codex** as a step-by-step guide. It helps me choose the next step and understand the errors. I run the commands on the actual machine, test the result, and tell it when what I see differs from what we expected. I couldn't have brought Jarvis this far on my own.

I enjoy figuring this out. I hope that sharing the real process, starting with a discarded computer and a spare stick of RAM, makes this technology easier for someone else to understand, use, and enjoy.

[Support the next hardware upgrade on GoFundMe](https://gofund.me/778e57dbd)
