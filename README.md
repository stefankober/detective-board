# What is it?

A detective board (a.k.a. evidence board, crime scene board).

Open source, full privacy, only JS + HTML5. 
Runs locally in browser. 
No cookies, no tracking.

# How to use it?

Download index.html. Open in browser. You can have open more than one instance without interference (unless you save to the same file of course).

## Creating Objects

1. Double click on background creates a **note**. Type text. Click outside of the note to finalize. You can still edit it later by doubleclicking on the note.
2. Copy an **image** somewhere else. Strg + V pastes the image.
3. Right click into background to create a **pin**. Hold the right button and drag: create a **thread**, and another **pin** where you release the button.

## Moving Objects

1. Click and hold into empty space: move everything.
2. Right click on an object (except thread, they move with the pins): move that object (left click is for copying text from notes).

## Delete Objects

1. Strg + click on object to delete.

## Zoom in or out

1. Use Mousewheel.

## Save and Load

1. Use save and load buttons.

## Version Control Systems

The boards are saved as JSON objects with images encoded and embedded. So using vcs will work.

To diff use something like `vimdiff <(jq -S . a.json) <(jq -S . b.json)`.

# What does it look like?

See screenshot below or test page: https://stefankober.github.io/detective-board/

<img width="1636" height="782" alt="image" src="https://github.com/user-attachments/assets/8349ca29-f661-45e0-b22c-dd2dcad064a2" />

# Why use it?

For me it is a simple way of wandering around thoughts that are naturally interconnected, but appear in a sequential fashion.

A detective board appears to give you a way of layering thought upon thought, grouping them, reflecting on them as they are layed and layered out before you without vanishing and fleeting into each other and then working with the grouped and reflected whole.

I find it immensely useful for learning, analyzing, explaining, structuring problems and a lot of other related mental activities.

The option to use images is additionally helpful for me, as I can barely see anything with imagination (I am largely an aphantast). So I can keep visual clues next to my discursive thoughts.
