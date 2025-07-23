+++
authors = ["k4nnix"]
title = "Starting point"
date = "2025-07-23"
description = "Figuring out where to start"
tags = [
    "beginner",
    "security",
    "htb",
    "start",
]
categories = [
    "security",
    "diary",
]
series = ["The Beginning"]
+++

## Getting Our Hands Dirty
At the beginning of this journey, the question stands: “Where do I begin?”
I already had a Hack The Box account and did most of the Starting Point machines a while back—as part of my vacation evening program, actually. So Tier 0 and Tier 1 are done, and a solid 36% of Tier 2 is on the way.

![Starting point progress, Tier 0 = 100%, Tier 1 = 100%, Tier 2 = 36%](/img/startingpoint.png)

Some of the machines were already pretty challenging. I have very little experience when it comes to privilege escalation on both Linux and Windows, so there’s still a lot to learn.

One box I actually enjoyed (and thought, “Yep, that could happen in real life”) was a web machine where the target company had built a custom Node.js code editor. They thought they were being clever by overriding dangerous functions like `const { exec } = require('child_process');`, but forgot that you can simply restore the original function from the prototype. So we went from “cute code editor” to instant system access. Implemented a reverse shell, escalated privileges—classic.

## Don't Neglect Theory
That’s the hands-on part. On the theory side, I’m keeping things light and fun because work is already pretty busy.

Right now, I’m diving into Linux fundamentals. And I already stumbled across something worth noting:
A lot of devs don't keep their environment clean.
Secrets on disk, unencrypted. But even more basic—lots of devs just throw sensitive stuff straight into their shell environment.

Since I recently reread the env command, I’m officially adding it to my mental checklist. Could definitely reveal some interesting stuff here and there.

I once saw AWS creds just chilling in a coworker’s .bashrc. I mean… come on.

That’s when I realized: you don’t always need a buffer overflow to find something juicy.
Might even write a little helper script to grep for keywords like AWS, TOKEN, SECRET in the environment. Nothing fancy—just a quick sanity check. Could even be a simple grep pipe 🤔

## A Goal in Mind
What’s the goal anyway? Landing a job? Hitting a certain HTB rank?

Honestly... I’m not sure yet.

Of course, the dream would be to land a job in security. But from experience, I know that smaller, more achievable goals are better for your mentality.

So here’s the first one:

- ✅ Finish the next Starting Point machine this week.
- ✅ Take my time and write a detailed writeup about it.
- ✅ Keep journaling—one step at a time.