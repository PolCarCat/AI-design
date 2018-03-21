

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

Artificial intelligence is an informatic program that allows systems choose reasoned decisions based on the current state and the necessities of the program. It tries to simulate a natural behaviour through computer algorithms.

AI is a fundamental part of video games, that is used on enemies, neutral npcs and computer allies. 
During the years of the video game history the AI has evolved like the games itself, from the pong rival to Ellie from the last of us.

Every game has the same purpose that is making the players enjoy the experience, it’s made by creating an environment and flow confortable or challenging to the player. So the AI has the same objectives, the entities in a game have to help the player achieve the game experience.

This intelligence tries to simulate a player or a living mind so the player can relate all the behavior that the NPC to a real person, at the end the main objective is to make the player feel like these entities have their own thoughts and make him able to empathise with code lines.
Also AI has to create memorable moments so we try to reach them by creating unique types of entities that has different behaviour, that at the end is mixing and adapting existing behavior components that fits in the current situation. 
The design of the entities has to be focused on what the player is going to interact.

How are the memorable moments created? It has proven that the human brain retains more information if it’s a situation that causes emotional arousal, in other words, that the situations that the user feel more connected or scared, that touches his emotions are more memorable. 
Also memorable moments are strengthened if the brain generates stress hormones, so the brain remembers more if it’s a danger situation.
    
So the necessity that the humans to need of interaction with other living beings it’s accomplished.

## AI types

### Friendly
The friendly AI are those that support the player during his journey, it will aid the player and help fighting against the enemies.
The main goal of the friendly AI is to make the player two basic emotions that are the affection and  the synergy.The affection is seeked by creating a bond between the player and the AI, the synergy is created by collaboration and codependence.
 
### Neutral
The neutral entities are those that are irrelevant to the main story. There are used in the situations were the game doesn’t have a high level of engagement, that the game slows the intensity, neutral AI fill these moments by adding more diversity and depth to the world. The examples of these AI are the typical walking people used in GTA or Assassin's Creed saga.

### Enemies

Enemies are the creatures that challenge the player that has to overcome using fighting mechanics. The enemies has several functions, that are explained later below, the enemies have to be fair, so in the design it’s included the tells, that is all the information that give to the player and the combat behavior.  



## Functions

The player is presented a series of challenging situation that he has to overcome. These situations has to be different from each other in order to make a memorable fight. But in order to make it fair the player has to find a way to win the battle, so first the enemy has to give information to the player so he can think the way to react. 

These information is given through sound and visual effects that the player can relate to the characteristic of the player, for example if one enemy is immune to sword attacks when the player hits it with a sword in can appear some sparks and a bounce back animation making him know that the attack doesn’t affect.  

Finally to present these qualities the environment should help the player notice them and act in his favor. For example if there is an enemy that push the player to pitfalls first there should be an area where the player can fall to safe place and when he has learnt that he can’t go near pitfalls when these enemies are near, the level changes to places with higher danger falls.

Some enemies can be focused in make the player train specific mechanics, so the reward is higher if the player uses the mechanic, it can be encouraging the users use it or forcing them and make the enemy unkillable unless if he uses the mechanic.
Some other enemies only exists for be killed, and give the player the fatisfaction and fun of smashing several enemies. Are the most common enemies that are commonly used to introduce the combat.
And there are also enemies that are used to make the player struggle and test their skill in combat.   


## Tells

As i mentioned before the tells are those actions that make the player know what the enemy is going to do. The tell gives the player the chance to adapt and respond to the actions of the enemy.
It has to be clear and specific for each action, so if there is a strong attack the enemy will hold its position for a period of time with a unique animation. 
In Nier automata before every enemy attack it gives audio feedback and their eyes does a red blink.
These is also used in most of the stealth games where the player can hear the “conversations” between the AI about what are they going to do.

## Behaviour


## Building the Extension Bundles

"Building" is really just zipping. Create all archives relative to the `src` directory.

Before zipping, delete the `src/common/test` directory. This will prevent the autotests from ending up in the release.

An important preparatory step is to remove any system-generated hidden files that shouldn't be included in the release file (like Windows' `desktop.ini` and OS X's `.DS_Store`, etc.). This shell command will delete those unwanted files:

```
find . -name "desktop.ini" -or -name ".*" -and -not -name "." -and -not -name ".git*" -print0 | xargs -0 rm -rf
```

### Chrome and Opera extension

Create a file with a `.zip` extension containing these files and directories:

```
manifest.json
common/
chrome/
```

### Firefox/Thunderbird extension

Create a file with a `.xpi` extension containing these files and directories:

```
chrome.manifest
install.rdf
common/
firefox/
```

### Safari extension

The browser-specific code is located in the [`markdown-here-safari`](https://github.com/adam-p/markdown-here-safari) project.

Use the Safari Extension Builder.

## Next Steps

See the [issues list](https://github.com/adam-p/markdown-here/issues) and the [Notes Wiki](https://github.com/adam-p/markdown-here/wiki/Development-Notes). All ideas, bugs, plans, complaints, and dreams will end up in one of those two places.

Feel free to create a feature request issue if what you want isn't already there. If you'd prefer a less formal approach to floating an idea, post to the ["markdown-here" Google Group](https://groups.google.com/forum/?fromgroups=#!forum/markdown-here).

It also takes a fair bit of work to stay up-to-date with the latest changes in all the applications and web sites where Markdown Here works.

## Credits

*Markdown Here* was coded on the shoulders of giants.

* Markdown-to-HTML: [chjj / marked](https://github.com/chjj/marked)
* Syntax highlighting: [isagalaev / highlight.js](https://github.com/isagalaev/highlight.js)
* HTML-to-text: [mtrimpe / jsHtmlToText](https://github.com/mtrimpe/jsHtmlToText)

## Feedback

All bugs, feature requests, pull requests, feedback, etc., are welcome. [Create an issue](https://github.com/adam-p/markdown-here/issues). Or [post to the "markdown-here" Google Group](https://groups.google.com/forum/?fromgroups=#!forum/markdown-here).

## License

### Code

MIT License: http://adampritchard.mit-license.org/ or see [the `LICENSE` file](https://github.com/adam-p/markdown-here/blob/master/LICENSE).

### Logo

Copyright 2015, [Austin Anderson](http://protractor.ninja/). Licensed to Markdown Here under the [MDH contributor license agreement](https://github.com/adam-p/markdown-here/blob/master/CLA-individual.md).

### Other images

[Creative Commons Attribution 3.0 Unported (CC BY 3.0) License](http://creativecommons.org/licenses/by/3.0/)

---

![Dos Equis man says](https://raw.github.com/adam-p/markdown-here/master/store-assets/dos-equis-MDH.jpg)
