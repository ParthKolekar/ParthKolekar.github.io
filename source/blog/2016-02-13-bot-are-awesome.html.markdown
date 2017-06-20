---
title: Bots are Awesome!
date: 2016-02-13 10:40 UTC
tags: 
  - ctf
  - misc
  - recon
  - felicity
---

> Aren't they awesome ! 

## Write-up

by [ParthKolekar](https://github.com/ParthKolekar)

The bot in question was on the IRC channel. The bot was an instance 
of goircbot named teehee bot. The bot would respond to all queries of 
the form

    !teeheeBreakIn query

For getting the flag, a recon had to be made on the bot. The bot replied 
to `!teeheeBreakin about` and `!teeheeBreakin help` among other commands 
which would show the github page for goircbot.

The source code had a `breakin` branch with the following lines in the source
code

~~~ go
        bot.WriteMessage("This is where all the magic happens ;)", name[0])
    } else if flags[1] == "breakInEnter" {
    } else {
        bot.WriteMessage("I didn't get that, try '!teehee help' ??", name[0])
    }
~~~

This leads to the final solution

    !teeheeBreakIn breakInEnter

On giving the bot this command the bot replies with 

    sugarHowDoYouGetSoFlyyy

Which is the flag.
