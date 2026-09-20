# Screen Sessions Guide

This is an example of how screen sessions work in Linux Ubuntu 20.04.

```
screen -S bot // This creates a NEW screen session called "bot" (CAPITAL S)

screen -r -d bot // This allows you to reconnect to a screen session called "bot"

CTRL + A + D // This will detatch you from a screen session when inside of one

CTRL + D // This will terminate a screen session when in it

screen -list // View all screens

killall screen // Terminates all screen sessions
```
