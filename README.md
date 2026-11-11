# Campaign Agent — Abu Margarita

**An AI agent that runs the social media of a small home kitchen — and measures what actually sells.**

Abu Margarita is a family kitchen that makes traditional dishes, cakes and cookies. Like most small food businesses, it has no marketing team: posts go out when someone remembers, nobody knows which dish or which channel brings in orders, and the time that should go into cooking goes into the phone.

This project is an agent that takes care of that loop: it prepares each post, asks for approval, gets it published on schedule, and reports back which posts turned into real orders.

---

## The problem

Posting is easy. Knowing what worked is not.

- Likes and views don't pay the bills: orders do, and most orders arrive as a private message on WhatsApp, where no dashboard can see them.
- "Best time to post" articles disagree with each other, and none of them describe *this* audience.
- Fully automated tools happily publish the wrong thing, or flood contacts until the account gets restricted.

## What the agent does

- **Prepares the week.** From a simple calendar sheet it drafts every post for every dish (photo, text, price, call to action) for Instagram, Facebook, Telegram and WhatsApp.
- **Traces every order back to its post.** Each post carries its own order link with a short code, so an incoming message already says which dish and which channel it came from. Attribution without a pixel.
- **A second reviewer checks the work.** Every post is scored against a quality checklist by a reviewer separate from the writer. If it falls below the bar, it goes back for rework.
- **A human approves anything that goes public.** Publishing, sending or spending always needs explicit approval. The agent drafts; people decide.
- **Measures, then adjusts.** It collects reach, interactions and orders at 24 h and 72 h, and closes each week with what to keep and what to change: dishes, channels, posting times.
- **Grows into automation gradually.** Week one is assisted. Steps get automated only after they've been proven by hand, and only if automating them pays off.

## Design principles

- **Real food photos, no generated ones.** AI builds the layout, never the dish.
- **Organic first.** Paid ads only later, with a hard daily cap and automatic cut-off.
- **No mass messaging.** Account safety comes before reach.
- **Nothing fails silently.** Every scheduled run is logged, safe to repeat, and reports missed runs instead of hiding them.

## How it's built

Python · Meta Graph API · Telegram Bot API · spreadsheet-driven calendar · test-first development.

Developed under **AIEF**, an engineering method that turns rules such as test-first, traceability and keeping secrets out of the code into checks the AI cannot skip.

---

*The source code lives in a private repository. This page describes the project; it doesn't contain it.*
