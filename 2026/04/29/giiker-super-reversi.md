---
date: '2026-04-29T10:00:00-05:00'
draft: false
title: "GiiKER Super Reversi"
slug: "giiker-super-reversi"
author: "Tipa"
disqusIdentifier: "2026/04/29/giiker-super-reversi"
summary: "This handheld game wants to teach you the game of Othello/Reversi. But how does it do against... ninja turtles?"
categories:
  - "Strategy"
tags:
  - "giiker"
  - "Othello"
  - "super reversi"
relatedPosts:
  - url: "/2023/09/04/retro-world-find-othello-world/"
    title: "Retro World Find: Othello World"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2023/09/Screenshot-2023-09-04-162409.png"
  - url: "/2026/02/13/othello-trigger-for-the-gameboy-color/"
    title: "Othello Trigger for the Gameboy Color"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/02/othellotrigger.png"
  - url: "/2026/02/03/the-end-of-the-othello-world-saga/"
    title: "The End of the Othello World Saga"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/02/Screenshot-2026-02-02-20-11-59.png"
  - url: "/2026/01/30/othello-world-i-killed-the-dragon/"
    title: "Othello World: I Killed the Dragon"
    thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/01/Screenshot-2026-01-29-21-40-06.png"
coverImage: "https://tipa16384.github.io/wkblog/uploads/2026/04/1-IMG_5762.jpg"
thumbnailImage: "https://tipa16384.github.io/wkblog/uploads/2026/04/1-IMG_5762.jpg"
---
This handheld game wants to teach you the game of Othello/Reversi. But how does it do against... ninja turtles?
<!--more-->

I was scrolling through the YouTubes and happened to come across a demo of the latest handheld game from GiiKER, "{{< youtube h7yjKNN_q_A >}}". GiiKER makes a business from making premium handhelds for games like *Mastermind* and *Sudoku*, and they're intended for children just learning these classic games.

I was really intrigued by the packaging. *Super Reversi* is a circular game with a square OLED screen against a black background. Circling the play area is a light bar that lights up white or green to indicate who is winning. The lightbar is surrounded by a movable ring that lets you select your moves. The screen itself shows the Othello/Reversi (Othello is the branded name for a popular Reversi variant; despite the name, this handheld plays Othello in that it skips the first two moves to start from a standard opening).

A large button on the face turns the game on and off, and is used to confirm a selected move. A sliding switch selects between one player, two player, and challenge mode. Challenge mode are a selection of 500 games in progress that are progressively harder to win.

In the header picture (which should be way greener than it appears here), you can see the "new game" arrangement. White and Green in a checkerboard pattern. In *Super Reversi*'s solo mode, the player always plays Green and the computer always plays White. The potential moves are shown dimmed, aside from the currently selected move, which glows fully Green. Rotating the dial would select one of the others. Pressing the large button locks in the move.

The ads say straight out that the game will learn your moves and improve its game as you play. I've played almost a dozen games with it, and it hasn't really improved, though I have noticed it taking longer to consider its moves, so perhaps it is getting better or perhaps I'm imagining it. There's nothing in the manual about resetting the learning, so either they are wrong about it, or it only improves its play until you turn it off. In any event, I haven't lost a game with it that I was paying attention to.

{{< image src="https://tipa16384.github.io/wkblog/uploads/2026/04/image-4-1024x768.png" title="Donatello won. Again." classes="center" >}}

A couple of months ago, I wrote a console version of Othello with the intent to beat my personal Othello nemesis, *Othello World* for the Super Famicom. I wrote a genetic algorithm to tune the very best board state scoring algorithm without getting insane about "frontier" pieces and "quiet moves". Then I paired it with the [negamax algorithm](https://en.wikipedia.org/wiki/Negamax). I could win on the lowest setting, but the deeper searches just punished me for any bad move. It did beat the final boss of *Othello World* (who was God, btw. Japanese games do not shy away from gamifying Christianity).

So after I'd played with the *Super Reversi* game a bit, I got to wondering how it would do against my game. I was fixing it to let me choose to play White (so the computer would make the Black moves), when I had an insane idea to use my game as the back end to a browser front end.

See, we've been doing exactly this at work. The place I work at is making the transition from Java to Python, and so I have been building up a lot of expertise with FastAPI and Pydantic. We have *also* begun moving to agentic development -- vibe coding, corporate-style. So I decided to bring these work skills home and develop a front end with agents.

I know there's people out there who will react with disgust to any mention of AI in any capacity whatsoever. And they value software made without the use of any AI tools. I *get* that. This is my job, and I *like* coding by hand. But my goal was to review this device without having to spend several nights writing the FastAPI layer and the browser front end.

So I switched the VSCode Copilot to the "Plan" agent and described to the agent what I wanted to do. Turn my CLI game into a FastAPI back end, with complete unit testing verifying the game still worked in CLI mode and verified the REST API. Then I explained what I wanted from the front end, how I wanted the user to interact, and to use the Teenage Mutant Ninja Turtles as the difficulty levels, with Michelangelo as the "easiest" and Donatello as the "hardest", with Raph and Leonardo providing the intermediate challenges. And I wanted the turtle portraits. *And*, and this is the important thing, I told it to set up a Playwright testing layer that would run the game in a headless Chrome instance and essentially use the UI to play the game at speed without letting me see it until it was not only working, but *proven* to work.

The first time I ran the game, it was playable. I then spent several hours playing it and suggesting improvements and finding bugs with edge cases (such as both players passing while there were still open spaces on the board).

Anyway, even Michelangelo had no trouble beating GiiKER, which is fair, because Mike and I are about 50/50. Donatello just laughs when I challenge him to a game, unless I bring pizza. Later: GiiKER did eventually beat Michelangelo. Maybe it *is* upping its game; maybe it resets when the batteries are pulled?

**So the review part of this.**

The GiiKER *Super Reversi* is a lot of fun. It looks slick, the controls are simple and innovative, and it's going to teach you the game. Being brutally honest, sometimes I just like flipping discs and am not looking to spend ten minutes on a move. Othello is a game where two players try to trick the other player into making a Bad Move by removing all of their Good Moves. It's stressful! GiiKER *Super Reversi* won't punish you for the occasional wrong move.

This game isn't made for Othello pros.

*That said*, I believe the game is upping its challenge, it's just that I keep playing it against Turtle Othello in order to debug my game which just potentially improves *both* games.

**So the AI part of this.**

I am required to use agentic coding tools at work. They paid a lot of money for them, and so I have to use them. I am telling you now that every coder I talk to, in or out of the company I work for, is using AI codebots to some extent. Maybe they aren't up to agentic coding, but it's done. If you will only play a game that has been coded with no AI help whatsoever, you are going to be playing very few modern games because I promise you, all the game studios are using AI to some extent. Maybe not AI art, but code? Yeah.

Working, testable and tested code, full coverage, able to follow your bright ideas wherever they lead? It's a game changer. A literal game changer. I get to spend more time playing the game and iterating toward the fun than dodging syntax errors and 12AM spaghetti code. So, yeah. Like it or not, it's isn't happening, it has already happened.
