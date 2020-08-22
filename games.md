---
title: Gaming
layout: default
category: info
public: true
order: 9
---

# Gaming Schedule
{:.no_toc}

You can find all the gaming happening in our discord, in the "Digital Gaming" section. Go to the #enter-the-game-room channel and click the emoji associated with the game you want to play!

* Toc will go here
{:toc}

{% assign gametypes = "Horizons SBS,Artemis SBS,JackBox" | split: "," %}
{% for gametype in gametypes %}
## {{ gametype }}
{% assign games = site.data.games | where: "game", gametype %}
{% for game in games %}
- {{ game.day }} {{ game.time }} - {{game.description}}
{% endfor %}
{% endfor %}