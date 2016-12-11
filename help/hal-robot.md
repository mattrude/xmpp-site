---
layout: default
title: The HAL Robot User Guide
permalink: /help/hal-robot/
---

Some conference rooms, on this server, have a robot logged into them to help the users in the room with common tasks.

## List of Commands

* **ping** - This command sends a ping (a small packet to check latency) between the HAL bot and your client.  This will let you know how fast or slow the connection is between your client and the server.
* **slap** - Sends a message (in the 3rd person) to the room saying that the user who sent the message, slapped the user the message was going to.
* **tell** - This very use full command stores a message, then sends it to the room after the user it was sent to comes back on line.
* **version** - Displays the current version of the HAL bot.
* **xkcd** - This just a fun little command to display a link for the current [xkcd](http://xkcd.com/) comic or if you specify an ID number, HAL will look up and provide you with the URL for that specific comic.

## About HAL

HAL is free software licensed under the [BSD](http://code.matthewwild.co.uk/riddim/file/feafc98e8c78/COPYING) license, written by Matthew Wild.  More information can be found at [code.matthewwild.co.uk](http://code.matthewwild.co.uk/riddim) & [www.thiessen.im](http://www.thiessen.im/2010/10/riddim-a-neat-little-xmpp-bot-written-in-lua/).
