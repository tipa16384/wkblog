---
date: '2026-08-29T10:50:06-05:00'
draft: false
title: "EverQuest Legends: A Moment of Clarity"
slug: "everquest-legends-a-moment-of-clarity"
author: "Tipa"
disqusIdentifier: "2026/08/29/everquest-legends-a-moment-of-clarity"
summary: "Well yeah. I'm an enchanter. I cast Clarity. Warning: In this post, ChatGPT analyzes my EQ Legends damage log."
categories:
  - "Blaugust"
  - "Blaugust 2026"
  - "EverQuest"
tags:
  - "ChatGPT"
  - "EverQuest Legends"
relatedPosts:
  - url: "/2026/08/31/everquest-legends-the-true-endgame/"
    title: "EverQuest Legends: The True Endgame"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/08/1-EQ000077.jpg"
  - url: "/2026/08/23/yawning/"
    title: "Yawning"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/08/1-EQ000069.jpg"
  - url: "/2026/08/22/fear-and-loathing-in-los-norrath/"
    title: "Fear and Loathing in Los Norrath"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/08/1-EQ000067.jpg"
  - url: "/2026/08/18/everquest-legends-theres-no-way-this-is-going-to-last/"
    title: "EverQuest Legends: There's no way this is going to last."
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/08/ghilthewarlord.png"
coverImage: "https://tipa16384.github.io/wkblog/uploads/2026/08/EQ000076.jpg"
thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/08/EQ000076.jpg"
---
Well yeah. I'm an enchanter. I cast Clarity. Warning: In this post, ChatGPT analyzes my EQ Legends damage log.
<!--more-->

I have been really, really good about not using AI -- AT ALL -- on my blog during Blaugust. I believe I have always been up front when I have shared AI-sourced writing, and I don't claim it as my own or anything. But that's just me. You do you.

THAT SAID.

I have never said I don't use AI -- quite the opposite. And in this post, I'm going to talk about how I've been using it *recently*.

I was reading the EverQuest Legends Discord and someone disparagingly mentioned that they were looking for a good EQL log parser that wasn't vibe-coded. There were several suggestions, and I downloaded one of them and immediately started using it to analyze my combat logs in the game.

But where other players may have read the Discord and thought, "ah, vibe-coded parser = bad, presumably 100% total human coding parser = good", *I* thought, "Oh yeah. I should vibe-code a parser!"

I'm not really going to be talking about the results of that here. I wanted a parser that would tell me, while leveling low level classes, when XP and mote drops were working at a good rate, and when I would want to try easier or harder content. It really helps with those low level dungeon grinds. It's written with the Electron UI engine backed with TypeScript. I didn't write any of it. It works great.

This sort of real time analysis, though, isn't very useful in endgame content. The other, presumably non-vibe-coded, programs do do that, though, so it's fine. But I wanted more.

I started dumping my combat logs into ChatGPT, uploading my stats and gear, and asking for analysis. And I've been using its analysis to tweak how I play and what gear I use. So I am going to share its analysis of my and Kasul/Kanad's recent trip to the Plane of Sky -- our first!

Below this is ChatGPT response to my uploading the log. It has context from several other uploads, so it knows what changes I've been making.

I isolated the actual Sky instance from **20:04:44 to 23:36:21**. This was Sky 0/Normal, not a higher difficulty tier.

### Your damage

My parse gives about **664,900 tracked personal damage**:

SourceDamageSharePierce149,43022.5%**Discordant Mind****140,722****21.2%**Puma Maw106,74416.1%Slash65,2779.8%Bash52,5127.9%Kick42,7966.4%Cleave40,7066.1%Earthquake34,8055.2%Boil Blood15,7892.4%Thorns9,8591.5%Gasping Embrace5,9940.9%

So across the **entire** run, piercing narrowly beat Discordant.

But I divided your outgoing-damage activity into combat blocks separated by at least 30 seconds without personal damage. There were **20 blocks in which you cast Discordant at least three times**. Discordant was your largest single damage source in **15 of those 20**. Across those blocks collectively, it did about **138K**, versus **107K piercing**.

So if the monitor was looking at a rolling window while you were actively nuking, **“nukes are currently your biggest damage source” was genuinely correct.**

You can see why in individual exchanges: a 405-point Discordant lands while your simultaneous weapon hits are 44 slash and 27 pierce; seconds later another 405-point Discordant lands alongside 13 slash, 54 pierce, 85 Cleave and a 246 Earthquake.

### Discordant worked surprisingly well

You cast it **454 times**.

I can account for:

- **367 damaging hits**

- **55 outright resists**

- **25 interrupted casts**

- 2 fizzles

- 5 starts without a clean outcome I can confidently match

Among casts that clearly reached the resist check, that's roughly an **87% damage-result rate**. Average damaging result was about **383**, and even dividing total damage by *every* cast start—including resists and interruptions—you got about **310 damage per button press**.

That's quite good for something you're squeezing in around your real work.

Sky's resistance also wasn't uniform. Ordinary mobs were frequently quite vulnerable to Discordant. Gorgalasks, sprited harpies, crystaline clouds, many spirocs, etc. were taking ~400–450-point hits quite reliably.

The big named were different. **The Spiroc Lord was roughly 50/50**, and even successful hits were heavily mitigated; the log shows repeated outright resists. **Keeper of Souls** also resisted repeatedly. And **Bazzt Zzzt** did the same.

So I'd characterize Sky as:

**Trash/ordinary island mobs → Discordant often excellent.**
**Major named → test it, but don't assume normal efficiency.**

### Gasp was the loser

This is much clearer than in Hate. You only cast Gasping Embrace **21 times**, and **14 of those produced explicit resists**.

Total Gasp damage: **5,994**.

Compared with **140,722 from Discordant**, that's pretty decisive. Against Sky resistance, spending spare casting opportunities on Discordant rather than trying to establish Gasp was generally the better move.

### And yes, charm basically failed as a strategy

Technically the log contains successful `has been charmed` messages. Functionally, your description is right.

Some mobs explicitly say **“This NPC cannot be charmed”** when you try Allure. And many of the charms which technically landed lasted absurdly briefly. A spiroc banisher, for example, is charmed at **22:26:16 and Allure wears off at 22:26:17**. The later gorgalask attempts were similarly only a few seconds.

So the normal architecture—**pet does the damage while you run the encounter**—was effectively taken away from you.

Mez wasn't providing a comfortable substitute either. You cast Mesmerization III **216 times**, and the log contains **185 explicit resist lines**, often several from one AE cast, plus explicit `Your target cannot be mesmerized` messages.

That is a fundamentally different workload from Hate.

### You really were spending a lot of effort staying alive

You cast **Sacred Echo VII 238 times**. And you died four times: azarack, watchful guard, Overseer of Air, and Bazzt Zzzt. The Overseer death is especially illustrative: you're trying to cast mez while it lands consecutive **492 and 720** hits, interrupts you, and kills you.

So this wasn't a case where you abandoned support duties to chase the parse. You were tanking/healing/control-spamming **and still managed 454 nukes**.

### The fast-weapon plan still worked

Despite Discordant becoming spectacularly visible, your basic strategy remained intact.

If I combine ordinary weapon damage, Bash/Kick/Cleave, Puma, Earthquake and Boil Blood—the stuff that largely happens while you're free to do something else—I get about **508K damage**, or **76% of your tracked total**.

That's the important number to me.

Your active nuking could become your **largest individual source** when circumstances permitted it, while the passive autoattack ecosystem was still doing three quarters of your overall work.

So I wouldn't change your model to “I'm a caster now.” I'd describe what happened in Sky as:

> **Charm was effectively unavailable, control was unreliable, and Discordant happened to remain efficient against much of the ordinary population. So whenever survival gave you a spare casting slot, nuking was an unusually profitable use of it.**

That is almost exactly what you wanted from this build: maximize damage that happens without your attention, then exploit magic damage when the encounter gives you room. Sky simply gave you **far more reason to use that second clause** than Hate did.
