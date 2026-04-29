# GDIM33 Vertical Slice
## Milestone 1 Devlog
I didn't see that there was a Vertical Slice repo, so I created my own a little while ago. I'm so sorry. Below is the repo I made, and I have been committing my changes to it.
https://github.com/bexxxe/Racoon-Pawn-Shop
Visual Scripting Graph

The first graph I tried to make was a state machine for the NPC so they could transition states, but after 5 hours of trying to make it work, I gave up. It was too late, and I started it too late for any redos. So instead, I made a really simple state machine. It was when the mouse was hovering over an object in the inventory that the item would move up a little to indicate that you were selecting the item. There were 2 states, normal and hovered. They have connected transitions between them using, on pointer enter and on pointer exit. The Hovered state had a transform that lifted the object slightly. The Normal state also had a transform, but for the original position. So when your mouse was over the object, it would move up to show that you were hovering over it.

I linked the breakdown below. I added two new Unity systems, the Timeline and Scriptable Objects—the Timeline I would use for the customers' cutscenes. Usually used for when the NPC is walking into the store, I want them to play a specific animation. Then I plan to add Scriptable Objects for the dialogue that are connected to the UI. I haven't done it yet, but I've found a workaround by using tags on my items, and I would like to try Scriptable Objects. I haven't added money yet, but im planning to.

My one visual scripting graph is my state machine. I was told it was okay, so I assume it is. As described in part 1, it's a simple 2-state graph. One Normal and one Hovered, each with connecting transitions. So that when your pointer is on the item, it lifts a little. The items already have a normal script that makes them draggable and allows them to be placed in the item slots. When the item lifts on hover, it gives the player a visual signal that the item is selectable and draggable. This directly feeds into the drag system that I made. The player hovers, sees the item lift, then clicks and drags. The state machine is essentially the first step in the interaction loop before DraggableItem takes over. Other than that, I was/am planning to make a larger state machine for the NPCs and all their different states/responses, but that didn't work out well, so I pushed it off. For the NPC state machine, I would need to combine scripts and visual scripting for it to work, but I feel like I haven't learned enough to pull it off. Hopefully it's ok that I was a little late; my Unity decided not to save, so I had to restart some parts, and I also have 2 midterms tomorrow/today.

https://docs.google.com/drawings/d/1z7B0QOzfWqonLkrC7Ff_KNYUN0jdluheUiCFFZj9QEc/edit?usp=sharing

## Milestone 2 Devlog
Milestone 2 Devlog goes here.
## Milestone 3 Devlog
Milestone 3 Devlog goes here.
## Milestone 4 Devlog
Milestone 4 Devlog goes here.
## Final Devlog
Final Devlog goes here.
## Open-source assets
- Cite any external assets used here!
