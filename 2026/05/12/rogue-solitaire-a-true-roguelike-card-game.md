---
date: '2026-05-12T12:00:00-05:00'
draft: false
title: "Rogue Solitaire: a TRUE Roguelike Card Game"
slug: "rogue-solitaire-a-true-roguelike-card-game"
author: "Tipa"
disqusIdentifier: "2026/05/12/rogue-solitaire-a-true-roguelike-card-game"
summary: "I have written a 100% authentic Rogue experience in a standard deck of cards. Complete rules inside!"
categories:
  - "Card Games"
  - "Rogue-Likes"
tags:
  - "Rogue"
relatedPosts:
  - url: "/2024/08/13/breakhack-fight-die-repeat/"
    title: "Breakhack: Fight, Die, Repeat"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2024/08/1-20240812215759_1.jpg"
  - url: "/2024/04/29/the-nightmare-of-druaga-ps2/"
    title: "The Nightmare of Druaga (PS2)"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2024/04/Nightmare-of-Druaga_SLUS-21071_20240421183241.jpg"
  - url: "/2023/08/09/games-that-defined-me-part-1/"
    title: "Games That Defined Me (Part 1)"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2023/08/gamesthatdefinedme.png"
  - url: "/2021/11/01/quick-look-unexplored-2/"
    title: "Quick Look: Unexplored 2"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2021/11/mainmenu.png"
coverImage: "https://tipa16384.github.io/wkblog/uploads/2026/05/RogueSolitaire.png"
thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/05/RogueSolitaire.png"
---
I have written a 100% authentic Rogue experience in a standard deck of cards. Complete rules inside!
<!--more-->

A couple of weeks ago, I was browsing BlueSky, as one does, during "Wishlist Wednesday", the day when indie game devs link to their game demos on Steam in the hopes people will add the game to their wishlists, which can increase the game's visibility when it launches. I came across this game:

> Say hello to the classiest new deckbuilder in town 🍸
> #wishlistwednesday
> Travel back 100 years to the roaring '20s in this trick-taking roguelike
> Play the demo ► store.steampowered.com/app/4225430/...
> [[image or embed]](https://bsky.app/profile/did:plc:ndojggll7catsmimor5cxzgm/post/3mknol7grkc2g?ref_src=embed)
> — 2 Left Thumbs ([@2leftthumbs.bsky.social](https://bsky.app/profile/did:plc:ndojggll7catsmimor5cxzgm?ref_src=embed)) [Apr 29, 2026 at 2:01 PM](https://bsky.app/profile/did:plc:ndojggll7catsmimor5cxzgm/post/3mknol7grkc2g?ref_src=embed)

*Overtrick* is a partner trick-taking game as if bridge were played with a pinochle deck, no bidding, and you could look at your partner's cards. I played the demo; it lets you buy special powers between rounds. But what got me was that this game was described as a *rogue-like*. In what way was this like *Rogue*, I asked the developer. They replied:

> "Roguelike" has grown a ways beyond something seen as similar to Rogue. It mostly comes down to procedural generation, run variety, and permadeath.
> "Traditional roguelike" however is a tag used to narrow down more closely to Rogue-like games. Silly as that is 😅
> — 2 Left Thumbs ([@2leftthumbs.bsky.social](https://bsky.app/profile/did:plc:ndojggll7catsmimor5cxzgm?ref_src=embed)) [Apr 29, 2026 at 8:09 PM](https://bsky.app/profile/did:plc:ndojggll7catsmimor5cxzgm/post/3mkod4xuakk23?ref_src=embed)

Fair enough. *Traditional* rogue-likes are those that are like the game of *Rogue* in some way. Rogue-likes have *procedural generation*, *run variety* and *permadeath*. I will point out, that when I played *Overtrick*, none of the participants died or seemed likely to. Procedural generation was shuffling the cards. Run variety was... shuffling the cards.

I don't want to spend a lot of time talking about *Overtrick*, though. I got wondering -- was it possible to make a card game that was more of a *traditional* rogue-like?

Procedurally generated dungeon, that you descend through, reach the goal, battle your way out, monsters move only when you do, permadeath, save scumming prevention, damage, health, weapons, magic, monsters and player represented abstractly... Could you do all this in a *card game*?

I think you can. I have spent the last couple of weeks working on a solitaire variant that is as much like *Rogue* as I can make it. All it takes to play is a standard deck of 52 cards (plus the two Jokers), a place to lay down some cards, and the rules below. I have playtested this at least a dozen times, and I got Kasul to give it a shot tonight. I think it is ready to reveal to the wider world.

{{< image src="https://tipa16384.github.io/wkblog/uploads/2026/05/image-4-300x200.png" classes="center" >}}

*Rogue Solitaire* is the answer to the question nobody asked: Can someone make a true "traditional rogue-like" with just a deck of cards? The answer is: yes, and I have done it. (Don't consider this a roguelike? See the definition section).

Just as in *Rogue*, the object of *Rogue Solitaire* is to descend to the bottom level of a dungeon and get back out alive[1](#4cb5ccc3-8460-4051-9d34-89cb2335e7d3). Each floor has an exit to the next floor[2](#35511bf9-5de8-4a90-904b-15907f5bb64d), and this exit is locked. You must fight monsters for the key and then make your way to the exit. On the bottom floor, the ghosts of the monsters you've defeated pursue you to the exit. Can you make it there before you die to wounds or hunger and become a **True Rogue**?

Even the bravest adventurer may decide the challenge is too much and turn back after only one floor. This is the **Quick Play** mode and takes about ten minutes. The dungeon campaign, a full run of ten floors plus feasting at the Victory Buffet, will probably take around two hours. However, the game can be saved after any floor.

{{< image src="https://tipa16384.github.io/wkblog/uploads/2026/05/image-5.png" title="The play area" classes="center" >}}

*Rogue Solitaire* is played on three 3x3[3](#5f7e0c58-a165-43e8-a847-ddcf9c92f2cd) grids of cards. Before you, in the center, is the player grid. The card in the center is your *inventory*. The cards surrounding the center are your armor, weapons and health.

To the right is a 3x3 grid representing the exit. The card in the center is always a Joker. The cards surrounding the center represent the location of the exit. When all the cards in your player board match either the suit or rank of the card in the corresponding spot on the exit, then you are at the exit. If you have a Joker in your inventory -- it is the center card of the player board, then you unlock the exit and enter the next floor (or escape the dungeon!).

To the left is a 3x3 grid representing the monster. There will always be a monster. You must defeat monsters to find the hidden Joker that is the key to the exit, and you'll have to be clever with attacking, defending and healing to survive.

**Setting Up**

Remove the Jokers from the deck and shuffle the deck. Deal nine cards face up in a 3x3 grid in front of you. This is your player board. Place one of the Jokers (the lock) to the right of the player board and deal eight cards face up around it. This is the exit. Return the other Joker to the deck, shuffle again, and deal nine cards in a 3x3 grid face down to the left of the player board. This is the monster.

Set aside a spot for discards. Cards are always discarded face down. Set aside a spot next to it for the Victory Buffet. Victory Buffet cards are always discarded face up. You start the game with no cards in your hand -- you must win them from monsters. Cards in your hand are kept... well, in your hand.

## Playing the Game

- **Discard** -- discard down to five cards in your hand.

- **Play** -- you may take one *and only one* of the following actions, or skip to the next step

Swap the position of two cards, both on your player board

- Move a card on your player board to an empty space

- Turn a face down card on your player board face up

- Swap a card in your hand with one on the player board

- Place a card from your hand in an empty spot on your player board

- Take a card from the player board and put it in your hand

- **Escape** -- if you are at the exit and the second Joker (the key) is in your inventory, you win the floor and move on. See the **Did I Just Win?** section below.

- **Attack the monster** -- you *must* attack the monster by selecting one of your non-inventory (non-center) cards and dueling the corresponding card in the same position on the monster grid. If your card is face down, it is first turned face up, and the attack continues. See the **Combat** section below for rules on resolving combat.

- **Monster retaliates** -- if the monster has a card on the opposite side of the center from your attack, then it *retaliates*. It chooses a card on the player board in the same relative position. If that spot is empty, it continues searching counter-clockwise until it finds one. See the **Combat** section below for rules on resolving combat.

- **Death**

If the player board is missing all the cards in any row or column, then the game is over[4](#9aafdf1e-1bce-45cd-97b1-dc880713b8f5).

- If the monster board is missing all the cards in any row or column, then the monster is dead. All the cards remaining on the monster board are added to the player hand (but keep the **Discard** phase in mind). Deal a new monster grid, shuffling the discards into a new deck if the deck is or becomes empty.

- **Continue with Step 1, Discard phase.**

## Combat

In a simple duel, high card is returned face up to its original position and low card is discarded. If there is a tie, both cards are discarded. Cards are ranked from 2-10, Jack, Queen, King, Ace and Joker. Joker wins every duel.

Sometimes, though, the monster reveals itself as a **Named Monster**, and things go a little differently.

If the center card of the monster grid is face down, and during combat a card on the monster grid is turned face up *and it is a face card*, then stop immediately and swap the face up face card with the face down card in the center, flip over this new card, and continue the duel as before. But see next paragraph.

If the monster is a Named Monster, which is to say its center card is a face card, and during combat a card on the monster grid is turned face up and it is a face card, and the player would lose the duel, then after the duel resolves, the monster does a **Special Attack**.

*However,*

If the monster is a Named Monster, and during combat a card on the monster grid is turned up and it is an Ace or a Joker, and the player would lose the duel, then after the duel resolves, the monster does a **Critical Attack**.

It is very possible to flip a card on the monster grid, it turns out to be a face card, the monster becomes named, and then the newly swapped card is flipped and revealed to be the Joker, the player loses the duel and the monster does an immediate **Critical Attack** all in the same combat phase. The world of *Rogue Solitaire* is no place for someone who hates surprises.

**Special Attacks**

Both critical and special attacks vary depending upon the suit of the card in the center.

- **Heart** -- Hearts are the healing suit

If the monster is undamaged, nothing happens

- If the monster has taken damage, then a card from the deck is played face down in an empty spot in the monster grid in a space of the player's choice, if there is more than one.

- If there are no cards left in the deck, shuffle the discards and deal one from the new deck.

- **Clubs** -- Clubs are the damage suit

If the player has cards in their hand, select one and discard it

- If the player has no cards in their hand, the attack misses

- **Diamonds** -- Diamonds are the greedy suit

One face down card in the monster grid is swapped with a card in the corresponding position on the player board (player choice). You've been pickpocketed!

- If the monster grid has no face down cards, this does nothing.

- The player must choose a face down card on the monster board that corresponds to a card on the player board. If there is no face down card on the monster board that corresponds to a card on the player board, the attack does nothing.

- **Spades** -- Spades are the magic suit

If the monster card that won the duel is not a Joker, then it is swapped with the corresponding card in the *exit grid*.

- If the monster card that won the duel *is* the Joker, then nothing happens.

**Critical Attacks**

Critical attacks are similar to special attacks, only more so.

- **Heart** -- Hearts are the healing suit.

If the monster is undamaged, nothing happens

- Otherwise, complete heal -- the deal cards from the deck into the empty spaces on the monster board, shuffling discards into a new deck if necessary.

- **Clubs** -- Clubs are the damage suit.

If the player has cards in their hand, they are all discarded.

- If the player has no cards in their hand, nothing happens.

- **Diamonds** -- Diamonds are the greedy suit.

It's a mugging! All face down cards in the monster grid are swapped (and remain face down) with the corresponding card in the player grid. Again, if the player doesn't have a card in the corresponding position, the swap doesn't occur.

- **Spades** -- Spades are the magic suit.

Teleport! The cards (except for the Joker) from the exit are picked up, shuffled together, and redealt. Now you have no idea where you are!

{{< image src="https://tipa16384.github.io/wkblog/uploads/2026/05/image-6-1024x386.png" title="Actual gameplay showing the player about to unlock the exit" classes="center" >}}

## Did I Just Win?

Congrats! You've found the exit, unlocked it, dashed through and slammed it shut against the monster champing at your heels. If you were just doing a **quick play**, you won! Grab your **Achievement** below!

If, however, you're a **True Rogue**, then you'll be continuing deeper.

Take a face card from your player board, the exit, the discard pile or your hand (check in that order) and add it, face up, to the Victory Buffet. That card is no longer available to play until the final gauntlet. If after discarding to the Buffet there are fewer than ten cards in the Buffet, then set aside the Jokers, reshuffle the discards into the deck, and reset the game board. You should have five or fewer cards in your hand. If you *don't*, then something is wrong.

If there *are* ten cards in the Victory Buffet, then turn the Buffet over so that all the cards are face down, and the face card from the first floor is on top. Now you are in a race. The game is played as normal with the following changes.

- New monsters are immediately identified and named from the top card in the Victory Buffet.

- If the Victory Buffet is empty when a monster is required to be made, then the player dies of hunger and the game ends immediately[5](#61046a32-10ab-4f19-81c2-df519bdad850).

- If the player makes it to and through the exit before this happens, then the player is a **True Rogue** or perhaps even a **Master Rogue**! (See **Achievements** below).

It's possible, though improbable, that the final monster from the Victory Buffet contains the Joker you need to escape. That would mean that you had the Joker but a monster special or critical attack stole it from your hand or player board. Better luck next time.

## How To

- **Save the game?** You can save the game at the end of any floor by setting aside your player hand (if any), the victory buffet and both Jokers, shuffling the remaining cards and placing the cards you set aside in a stack face up with the face down other cards and putting them back in the card case. You may later continue by separating your saved hand, the victory buffet and the Jokers and laying out the next floor of the dungeon as normal. Your saved game becomes impossible to retrieve once you continue.[6](#16a9e2e5-34e4-465d-9e72-aaec33e00747)

## Definitions

- **Dying from hunger:** You die from hunger when you are on the final floor of the dungeon, all monsters are dead, and the Victory Buffet is empty.

- **Finding the exit:** You have found the exit when a Joker is in the center square of the player board, and all eight other cards match either the suit or rank of the corresponding card of the exit board. If any match the suit *and* rank, please return your deck to the manufacturer.

- **Named Monster:** Once a monster has been identified, it becomes a named monster. Prior to that, it was just a pair of eyes peering from the darkness. Or something.

- **Traditional Roguelike:** Usually meant to refer to a turn-based dungeon crawler with a procedurally generated dungeon, monsters, and permadeath. This term is redefined every year during the "7DRL" roguelike development competition, where game developers are challenged to write a complete roguelike game in just seven days. The rules basically throw up their metaphorical hands and say, "if the gamedev believes it's a roguelike, then it's a roguelike". Whether anyone else agrees, well...

- **Victory Buffet:** The stack of face cards formed by discarding a face card at the end of each dungeon floor. It is used to spawn named monsters on the dungeon's final floor. Your current floor is 1 + the number of cards in the Victory Buffet.

## Achievements

Escaping the dungeon is all well and good. But the test of a true rogue is how stylishly you leave! Here's some achievements to prove your worth.

- **Zero to Hero:** Escape the dungeon in quick play mode.

- **Where did I leave my keys?** Die from hunger without having found the key to the exit.

- **It's too dark in here!** Die from hunger without even finding the exit.

- **True Rogue:** Escape the dungeon before dying from hunger.

- **Master Rogue:** Escape the dungeon before dying from hunger *with all four aces in your hand*.

- **Call me... Rodney:** Complete all the other achievements.
