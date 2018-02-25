---
layout: game
title:  "Yata - A DevOps game"
category: game
tags:
  - devOps
  - collaboration

publishdate: 2017-07-01 00:00:00

authors: 
  - Adrien Muller
  - Yoan Thirion
originators: 
  - Adrien Muller
  - Yoan Thirion
firstplayed: Luxembourg 2017
scale: Min 6, Max 10, can be played in multiple parallel groups
timebox: 45-60 mins

excerpt: This game will demonstrate major principles behind DevOps.

materials:
    - 1 set of 150-200 bricks/caplas
    - 2 pens
    - The printed rules
    - Whiteboard
    - Space

preparation:
    - Print the rules
    - Distribute the equipment as described below for each team
    - Explain the roles described below

images:
    - /images/games/yata/00.jpg
    - /images/games/yata/01.jpg
    - /images/games/yata/02.jpg
    - /images/games/yata/03.jpg
    - /images/games/yata/04.jpg

enableComments: true
---

### HOW TO PLAY
#### SETUP
Print the [rules]({{site.url}}/files/yata/Yata.pdf "Yata rules")

Space: You will need a large space with 2 tables to play.

As a facilitator explains the game from the rules,  then:
* Separate physically the Dev and Ops teams
* Put the “Dev” environment on the dev table
*	Put the “Pre-production” and “Production” environments on the ops table
*	Add the base structure for tower bases on each environment. The base must be as in the image below : (base structure represents the environments (DB, Frameworks, Languages, ...))
![Bases]({{site.url}}/images/games/yata/base.png "Bases")

#### RULES
Sprints: There will be 4 sprints during this game. Each sprint will be organized as described in the sprint image. For each sprint, the facilitator must distribute the cards corresponding (# sprint number). 

#### GOAL
The goal is to aim a maximum number of points by delivering features to production (deployment). We will use wooden bricks to do so.

### ROLES
![Roles]({{site.url}}/images/games/yata/roles.png "Roles")

### SPRINT Timing
![Sprint]({{site.url}}/images/games/yata/sprint.png "Sprint")

### SPRINT 1.
#### Documentation approach vs collaboration
*	DEV: 3 minutes to build and deliver to pre-prod
*	OPS: Refuse any non-documented tower

##### RETROSPECTIVE
*	Stop starting, start finishing / Work In Progress (W.I.P) limits
*	Keep It Simple & Stupid (K.I.S.S)
*	Production deployment requires collaboration and reveals problems.
*	**Silo breaks the collaboration**

### SPRINT 2.
#### Silo again
No collaboration: **it is forbidden to communicate with Ops (by the top management)**
*	DEV: Document the delivery + no cards for them
*	OPS: T shape base in pre-prod + prod

##### RETROSPECTIVE
*	**Opposite objectives between Dev & Ops** (accounting, different priorities/projects/visions)
*	Definition of done 
* Always think about the targeted environment

#### ACTION
Delivery and deployment in the presence of both teams.

### SPRINT 3. 
#### Culture of collaboration 
Move from siloed delivery to collaboration: **everyone in one room**.
*	DEV: construct, starting by taking back the previously tower + cards for Sprint 3
*	OPS: facilitates the deployment in pre-prod + prod

##### RETROSPECTIVE
*	Collaboration makes it possible to deliver
*	**Focus on culture/collaboration**
*	Collaboration saves time

### SPRINT 4.
#### Automation
*	DEV: construct, starting by taking back the previous tower + cards for Sprint 4
*	OPS: automate the deployment between pre-prod and prod

##### RETROSPECTIVE
*	Clone of production (blue/green deployment), could be simulated by swapping two pre-production and production post-its
*	Automate deployment and acceptance testing, instead of manually doing it
*	Pre-production environment for practicing before production
*	Continuous deployment card by card, ops manager sums the deployment times
*	**Automation saves time**

### Conclusion
*	Evolution of the metrics used on the boards, and aggregation into one shared board (performance, process, people, KPI linked to events)
* Collaboration is a skill that can be learned
* Explain the basic principles of DevOps (Be C.A.L.M.S)

![DevOps]({{site.url}}/images/games/yata/devops.png "DevOps")
