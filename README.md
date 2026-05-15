# GDIM33 Vertical Slice
## Milestone 1 Devlog
I didn't see a Vertical Slice repo, so I created my own a little while ago. I'm so sorry. Below is the repo I made, and I have been committing my changes to it.
https://github.com/bexxxe/Racoon-Pawn-Shop
Visual Scripting Graph

The first graph I tried to make was a state machine for the NPC so they could transition states, but after 5 hours of trying to make it work, I gave up. It was too late, and I started it too late for any redos. So instead, I made a really simple state machine. It was when the mouse was hovering over an object in the inventory that the item would move up a little to indicate that you were selecting the item. There were 2 states, normal and hovered. They have connected transitions between them using on pointer enter and on pointer exit. The Hovered state had a transform that lifted the object slightly. The Normal state also had a transform, but for the original position. So when your mouse was over the object, it would move up to show that you were hovering over it.

I linked the breakdown below. I added two new Unity systems, the Timeline and Scriptable Objects—the Timeline I would use for the customers' cutscenes. Usually used for when the NPC is walking into the store, I want them to play a specific animation. Then I plan to add Scriptable Objects for the dialogue that are connected to the UI. I haven't done it yet, but I've found a workaround by using tags on my items, and I would like to try Scriptable Objects. I haven't added money yet, but im planning to.

My one visual scripting graph is my state machine. I was told it was okay, so I assume it is. As described in part 1, it's a simple 2-state graph. One Normal and one Hovered, each with connecting transitions. So that when your pointer is on the item, it lifts a little. The items already have a normal script that makes them draggable and allows them to be placed in the item slots. When the item lifts on hover, it gives the player a visual signal that the item is selectable and draggable. This directly feeds into the drag system that I made. The player hovers, sees the item lift, then clicks and drags. The state machine is essentially the first step in the interaction loop before DraggableItem takes over. Other than that, I was/am planning to make a larger state machine for the NPCs and all their different states/responses, but that didn't work out well, so I pushed it off. For the NPC state machine, I would need to combine scripts and visual scripting for it to work, but I feel like I haven't learned enough to pull it off. Hopefully it's ok that I was a little late; my Unity decided not to save, so I had to restart some parts, and I also have 2 midterms tomorrow/today.

https://docs.google.com/drawings/d/1z7B0QOzfWqonLkrC7Ff_KNYUN0jdluheUiCFFZj9QEc/edit?usp=sharing

## Milestone 2 Devlog
Devlog Question 1: Before Code
Big Steps:
1. Set up the data structure for customers and items using Scriptable Objects, and test that data can be stored and read correctly.
THEN
2. Build the GameManager to load customers in order, swap their data, and trigger their timelines.
THEN
3. Connect the customer system to the dialogue and money systems so the full loop works end to end.

Detailed Steps:
Step 1 — Scriptable Objects
1. Create ItemData ScriptableObject with fields for name, sprite, correct dialogue, wrong dialogue, and value.
2. Test by creating one asset and checking that the fields appear correctly in the Inspector.
3. Create CustomerData ScriptableObject with fields for name, sprite, request dialogue, required item, animator controller, and timeline.
4. Test by creating one asset and filling in all fields.
5. Assign ItemData to each item's DraggableItem component.
6. Test by adding Debug.Log in Start and running the game to confirm each item prints its name.

Step 2 — GameManager
1. Create a GameManager script with a CustomerData array and a GameObject array for customer objects. 
2. Test by adding Debug.Log in Start and running the game to confirm the first customer's name prints.
3. Write LoadCustomer to swap the sprite, animator, and timeline on the current customer object.
4. Test by running the game and confirming that the first customer appears correctly.
5. Add position resetting so each customer starts at the correct position.
6. Test by running the game and confirming the customer appears in the right place on screen.

Step 3 — Full loop
1. Connect ItemSlot to read requiredItem from the mat and compare it to the dropped item's ItemData.
2. Test by dropping the correct item and confirming the correct dialogue appears in the Console.
3. Call script after the customer slides out.
4. Test by serving a customer and confirming that the money counter updates correctly.
5. Test the full loop from start to finish — all customers appear in order, each accepts their correct item, and the day-end panel shows the correct total after the last customer leaves.

Devlog Question 2:
They didn't help out that significantly. I tend to build things as I go, step by step. Writing a plan beforehand helps me know all the features I'm planning to add, but implementing them is a different process. I don't use the preplanned routes sometimes because they didn't work for me, and I also don't like having such a tight constraint on what I need to do. If I Im planning not to add something later on, even when I already have a plan, it's a hassle.

Devlog Question 3:
I bridge visual scripting and code through the Item Hover State Graph for inventory items. The State Graph handles two states, Normal and Hovered, and transitions between them using  On Pointer Enter and On Pointer Exit event nodes. The C# script involved is DraggableItem.cs, which lives on the same object as the State Machine. The State Graph and DraggableItem.cs both are on the same item GameObject, meaning the visual scripting handles hover visual feedback while the C# script handles drag-and-drop logic.
<img width="781" height="288" alt="image" src="https://github.com/user-attachments/assets/1ffb141e-6cea-462f-9659-124676b19681" />
<img width="637" height="173" alt="image" src="https://github.com/user-attachments/assets/31b4a73a-dbd8-44b0-8c0f-18ba012fd673" />
<img width="549" height="178" alt="image" src="https://github.com/user-attachments/assets/366421d2-d727-4946-9e99-340546d4bc55" />
<img width="870" height="588" alt="image" src="https://github.com/user-attachments/assets/a6ecb7e8-1177-43bd-9039-36575193fe2f" />
<img width="747" height="575" alt="image" src="https://github.com/user-attachments/assets/c567d572-f95f-4264-b2ee-08e138f09564" />

Devlog Question 4:
I used the Scriptable Object feature most; I created 2: one for items and one for customers. 

## Milestone 3 Devlog
Milestone 3 Devlog goes here.
## Milestone 4 Devlog
Milestone 4 Devlog goes here.
## Final Devlog
Final Devlog goes here.
## Open-source assets
- Cite any external assets used here!
