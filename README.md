

### Table of Contents
**[Intro](#intro)**<br>
**[AI types](#ai-types)**<br>
**[Functions](#functions)**<br>
**[Tells](#tells)**<br>
**[Behaviour](#behaviour)**<br>
**[Building the Extension Bundles](#building-the-extension-bundles)**<br>
**[Next Steps, Credits, Feedback, License](#next-steps)**<br>


### About me 

I am Pol Carrera Catalina, student of the Bachelor’s Degree in Video Games by UPC at CITM. This content is generated for the second year’s subject Project 2, under supervision of lecturer Ricard Pillosu.

## Intro

Artificial intelligence is an informatic program that allows systems choose reasoned decisions based on the current state and the necessities of the program. It tries to simulate a natural behavior through computer algorithms.

AI is a fundamental part of video games, that is used on enemies, neutral npcs and computer allies. 
During the years of the video game history the AI has evolved like the games itself, from the pong rival to Ellie from the last of us.

Every game has the same purpose that is making the players enjoy the experience, it’s made by creating an environment and flow comfortable or challenging to the player. So the AI has the same objectives, the entities in a game have to help the player achieve the game experience.

This intelligence tries to simulate a player or a living mind so the player can relate all the behavior that the NPC to a real person, at the end the main objective is to make the player feel like these entities have their own thoughts and make him able to empathize with code lines.
Also AI has to create memorable moments so we try to reach them by creating unique types of entities that has different behavior, that at the end is mixing and adapting existing behavior components that fits in the current situation. 
The design of the entities has to be focused on what the player is going to interact.

How are the memorable moments created? It has proven that the human brain retains more information if it’s a situation that causes emotional arousal, in other words, that the situations that the user feel more connected or scared, that touches his emotions are more memorable. 
Also memorable moments are strengthened if the brain generates stress hormones, so the brain remembers more if it’s a danger situation.
    
So the necessity that the humans to need of interaction with other living beings it’s accomplished.

## AI types

### Friendly
The friendly AI are those that support the player during his journey, it will aid the player and help fighting against the enemies.
The main goal of the friendly AI is to make the player two basic emotions that are the affection and the synergy. The affection is seeked by creating a bond between the player and the AI, the synergy is created by collaboration and codependence.

### Neutral
The neutral entities are those that are irrelevant to the main story. There are used in the situations where the game doesn’t have a high level of engagement, that the game slows the intensity, neutral AI fill these moments by adding more diversity and depth to the world. The examples of these AI are the typical walking people used in GTA or Assassin's Creed saga.

### Enemies

Enemies are the creatures that challenge the player that has to overcome using fighting mechanics. The enemies have several functions, that are explained later below, the enemies have to be fair, so in the design it’s included the tells, that is all the information that give to the player and the combat behavior.   



## Functions

The player is presented a series of challenging situation that he has to overcome. These situations have to be different from each other in order to make a memorable fight. But in order to make it fair the player has to find a way to win the battle, so first the enemy has to give information to the player so he can think the way to react. 

These information is given through sound and visual effects that the player can relate to the characteristic of the player, for example if one enemy is immune to sword attacks when the player hits it with a sword in can appear some sparks and a bounce back animation making him know that the attack doesn’t affect.  

Finally, to present these qualities the environment should help the player notice them and act in his favor. For example, if there is an enemy that push the player to pitfalls first there should be an area where the player can fall to safe place and when he has learnt that he can’t go near pitfalls when these enemies are near, the level changes to places with higher danger falls.

Some enemies can be focused in make the player train specific mechanics, so the reward is higher if the player uses the mechanic, it can be encouraging the users use it or forcing them and make the enemy unkillable unless if he uses the mechanic.
Some other enemies only exist for be killed, and give the player the satisfaction and fun of smashing several enemies. Are the most common enemies that are commonly used to introduce the combat.
And there are also enemies that are used to make the player struggle and test their skill in combat.   


## Tells

As I mentioned before the tells are those actions that make the player know what the enemy is going to do. The tell gives the player the chance to adapt and respond to the actions of the enemy.
It has to be clear and specific for each action, so if there is a strong attack the enemy will hold its position for a period of time with a unique animation. 
In Nier automata before every enemy attack it gives audio feedback and their eyes does a red blink.
These is also used in most of the stealth games where the player can hear the “conversations” between the AI about what are they going to do.


## Behaviour


All the creatures in a video game have a set of actions that determine what are they going to do. These actions have to be predictable but it can’t follow any patron, because when there is a behavior where the human brain can recognize a patron it will not assign it to a queue of actions pre prepared and it will break the player’s immersion. And also it has to be predictable because it has to be fair for the player. 
Some behavior is very simple and it’s only determined by one action, like the goombas of Mario where there are only programmed to walk in one direction. And fits with their purpose which is make the player jump. 
But there is also more complex behavior that allows the AI choose the actions in consequence of the in game situation. There are three main commonly used methodologies that are:


### Finite state machine

The finite state machine is a system used for simple AI where there is a short amount of actions that are connected between them. It can only be one action active and it transition to the others. This is a closed loop that it’s only broke if the unit is destroyed.

The finite state machine is a graphic representation between these boundaries of actions.
The flow of the nodes is determined by a series of Booleans that choose the path of the actions. So if one variable is true the AI will switch to the next action.

Finite state machine example


### Behaviour trees 

Ai also can be organized in a hierarchical structure, instead of a closed loop like the finite state machine systems. The behaviour trees separate the actions and connects them through a branching system. These branches can be expanded limitless and there are highly iterable.  

These method has a particularity that is that for checking the current state it has to traverse all the path since the root. 
It follows a path build by different branches, the branches are determined by the nodes
Each node has a current status, which can be Success, Failure or Running, that are the results if the action is done or if they are running.  

Not all the nodes are the same, there are:

#### Composites: 
The composites are nodes that can be travelled more than one time in a path and in iterates between its children.
-	Sequence: This iteration its running until one of its children returns a failure. It’s used to execute a set of actions that have to be consecutive.
-	Selector: It's the inverse to the sequence, runs until one of its children returns true, it’s used to iterate between actions with the same purpose, when the action is done the other ones are not useful so the selector stops. 
-	Random Selector: Only executes a child choose randomly.


#### Decorators:
It can only have one child and are used to change the returned status of the its child. 
-	Inverter: Inverts the result of the leaf.
-	Sucseder: Make that always return success, so a sequence can continue even though one action has failed.
-	Repeater: Makes one action be repeated a several times.
-	Repeat Until Fail: Repeats one action until it returns failure.


#### Leafs: 
The leafs are the actions, like walk to a certain position. And are incapable of follow a branch. 

 
### Goal Oriented Action Planning

As the names indicates the main purpose of this system is make the AI get to a set of goals and are obtained by doing a set of actions. The goals are consequences of actions, an example is kill the player, because it’s a consequence of attacking the player.
The actions are can be distributed with an importance scale and then check which is the highest valid action. 
These goals need a basic requirement that is the previous action, also called the desired world state, it’s the only way to reach that objective.

The AI will also have a list of actions that carries to basic concepts, which of the world states satisfies and which state requires, from where is going to where to go. 
Some actions will satisfy more than one world state or will require a variety of world states.


| **Action** | **Satisfies World State** | **Requires World State** |
| --- | --- | --- |
| Attack target | Damage target | Be near target |
| Chop a tree | Chopping | Axe equippedBe near tree |


The Ai has one or more current world states and this is used to chain different actions to reach the goal.
So the way that is the action plan build is, first choose a valid goal, then see if there is an action that satisfies the world state of the goal, if the current world state isn’t the same that the action required world state it’s added another action in the action chain that satisfies this required world state and repeating the loop until an optimal world state. 
So we keep adding actions to a queue that connects the required state of the goal to the current state.

In order to calculate the set of actions we have to create a path through all of them, so it’s used a similar system, the A* pathfinding, where each action is a node and the world requirement is the cost. 

The A* pathfinding is a system that finds the most optimal path between two nodes and also it takes account if one node is available to cross. Each node transition it has a cost, this cost is determined by the difference between the next node requirements to the current state. And also it has a cost so far, that compares the goal required state to the current state.

### Monte Carlo Tree Search

The Monte Carlo tree search is an algorithm used in strategy games, this methodology was used for defeating the chess world winner in 1997. 
The Monte Carlo tree search uses all the possible actions and generates a tree with all the actions used. 

It is done by:
At the beginning of the game the AI will open a X amount of nodes that are born from a main node, (each node is an action).

Then it will run a simulation of random actions that the player and the AI can do, until the game ends, then it checks which of the actions has succeeded result or a failure, if wins or loses. Then in will open a new branch from the most successful node.

If one node has won the simulation it’s opened a new X number of children and repeats the same calculation with every child.
Then it runs the simulation from the other non-winner children.

When all the possibilities are covered it’s used a formula to check which is the most optimal path:

It is based in four basic rules:

Selection Expansion Simulation Update

