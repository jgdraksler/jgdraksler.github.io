---
layout: post
title:  "Final Stretch"
date:   2023-12-03
---
## Introduction

This is my final blog post detailing my work on Project Quest. We've decided to extend the project for another several months, but as there is little-to-no design work left to be done on Project Quest, I will likely be moving onto the studio's next project in the coming months. Before then, we're attempting to get the project ready enough for a showcase in the coming days before we officially conclude this cycle in a week. 

## Play testing and bug fixing

I focused most of my initial attention this week on two issues I noticed in the village area. The first of these was related to dialogue; the lower right portion of the text box was displaying incorrectly, covering up text that would go under where it would be. I played through the village portion several times, trying to figure out what it could be related to, and then I finally noticed that it would disappear following the player making a choice when given dialogue options. With that I began disabling the dialogue response objects in Unity's hierarchy (which appeared to be disabled already due to one of its parents also being disabled), and ran through the village again until I eventually determined which object could be disabled to both solve the problem without introducing new bugs as far as I could determine. This took about an hour and a half.

From there, I moved on to another issue I noticed in my playtesting; the cutscenes I had previously made for the hide and seek quest had broken. The child would not have their sprite appear at the designated hiding spot (though entering the area would trigger the cutscene as normal, which would play out without issue), and rather would teleport back to the spot they were just found at following the cutscene's end. I was totally at a loss for how to solve this, and spent time looking at various places to see if I noticed anything had changed, but nothing stood out to me that was clearly wrong. I spent around 3.5 hours poking around, testing out various things with the hierarchy and timelines, but nothing worked. I decided to leave this issue as it was and move on, but when I went to record footage of the bug in the making of this post I found that someone else apparently went ahead and solved it. 

When I shifted focus from the prior issue, I did so because I was requested by Glen to shift focus to the forest area, which we intend to be the only area we show off at the showcase in a few days. The #1 priority here was fixing the various start; in prior weeks, the starting cutscene would loop upon completion (softlocking the player), but things had progressed to the point that the cutscene would "only" lock the player in place upon finishing. I spent time trying to locate the cause, but once again came up short; everything on the player was enabled and the animations were actually working as well, but the player just couldn't move. I took a deeper look at the timeline to see if something was going wrong there, but nothing stood out to me as wrong. When I manually moved the player object in the scene view during this softlock, they constantly snapped back to the location they'd get stuck at; this let me know that it was clearly an issue where something external was setting the player's position. We managed to resolve this issue during our meeting earlier today, but I spent about an hour of my own time on it before that.

## Time Breakdown
Meetings: 4 hours

Playtesting & Bugfixing: 6 hours

Total: 10 hours
