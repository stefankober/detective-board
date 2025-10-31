# What is it?

A detective board (a.k.a. evidence board, crime scene board).

Open source, full privacy, only JS + HTML5. 
Runs locally in browser. 
No cookies, no tracking.

# How to use it?

Download index.html. Open in browser. You can have open more than one instance without interference (unless you save to the same file of course).

Or use the test page here: https://stefankober.github.io/detective-board/

Autobackup data is stored only locally in browser storage and does not leave your device.

## Creating Objects

1. Double click on background creates a **note**. Type text. Click outside of the note or Enter to finalize (shift + enter = newline). You can still edit it later by double clicking on the note again.
2. Copy an **image** somewhere else. Strg + V pastes the image.
3. Right click into background to create a **pin**. Hold the right button and drag: create a **thread**, and another **pin** where you release the button.
4. Click on the arrow button to pick an **arrow**. Move it where you need it.

## Moving Objects

1. Click and hold into empty space: move everything.
2. Click and hold on an object (except threads, they move with the pins): move that object.

## Delete Objects

1. Shift + click on object to delete.

## Zoom in or out

1. Use Mousewheel.

## Save and Load

1. Use save and load buttons.

## Autobackup

Autobackup checks every minute if there are changes, and if so backs up your work to local browser's indexedDB (since v0.2.0) if the board is not empty, and keeps the last 10 versions **per open instance**.
A click on the button, and you can chose to restore any.
Works between sessions and after crash or accidental closing.
But note: **stale backups are deleted after 30 days**.

If you want to change any of the parameters, change these numbers in the code:
- backup interval (in milliseconds):
`setInterval(autoBackup, 60000); // every minute`
- keep last n:
`function cleanupBackups(maxCount = 10) {`
- delete after x days:
`const cutoff = now - maxAgeDays * 24 * 60 * 60 * 1000;`

## Version Control Systems

The boards are saved as JSON objects with images encoded and embedded. So using vcs will work.

To diff use something like `vimdiff <(jq -S . a.json) <(jq -S . b.json)`.

# What does it look like?

See screenshot below or go to test page: https://stefankober.github.io/detective-board/

<img width="1516" height="794" alt="image" src="https://github.com/user-attachments/assets/077ba943-a9c7-490c-a16f-1d382cbb54b8" />


# Why use it?

For me it is a simple way of wandering around thoughts that are naturally interconnected, but appear in a sequential fashion.

A detective board appears to give you a way of layering thought upon thought, grouping them, reflecting on them as they are layed and layered out before you without vanishing and fleeting into each other and then working with the grouped and reflected whole.

I find it immensely useful for learning, analyzing, explaining, structuring problems and a lot of other related mental activities.

The option to use images is additionally helpful for me, as I can barely see anything with imagination (I am largely an aphantast). So I can keep visual clues next to my discursive thoughts.

I tried a lot of tools to fit my thinking style: note taking apps like Loqseq or Joplin. Diagram as code tools. Draw.io. Plain Vim. Novelwriter. 

Those are all good tools, and you should try them too if you have not found yours.

But this detective board is what I am using now for a lot of things, and it fits my thinking style perfectly.

I find myself taking notes mainly related to the following tasks:

- Incident analysis: trace events, actors, and evidence until the story becomes clear.

- Learning: take screenshots from scripts or books, annotate them, and follow questions outward. Trace the logic with arrows.

- Research or writing: cluster related ideas, sources, and arguments as they develop.

- Exploration: wander around a thought without losing it to scrolling or switching tabs.

And for these use cases, this board is exactly what I need.

Here is a slightly blurred version of reading a technical book (slighty blurred because I do not own the rights to the screenshotted snippets):

<img width="1431" height="862" alt="image" src="https://github.com/user-attachments/assets/d9b9e818-b080-441e-acfe-bcf6608bfec5" />


# Kudos

I took some inspiration from https://github.com/Fungeey/detectiveboard.
