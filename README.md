# Fourfold

A shedding card game that plays by the official UNO rules, with classic-style cards. Single-file HTML; open `index.html` in a browser. Built for phones first, in portrait or landscape, and works on desktop.

- Play against 1–3 computer opponents, or online with friends (see below)
- Colors: Red, Yellow, Green, Blue
- Action cards: Skip, Reverse, Draw Two, Wild, Wild Draw Four
- Wild Draw Four is only legal when you hold no card of the current color. The next player can challenge it, and a challenge shows the hand it was played from
- Call **Last card!** when you play your second-to-last card. Opponents can catch you before the next turn starts, and you can catch them
- The first card turned up takes effect, and the dealer rotates each round
- A round that ends on a Draw Two or Wild Draw Four still makes the next player draw
- Score to 500 (official), or play a shorter game to 100 or 250

The in-game **Rules** button explains every card.

## Playing with friends

Up to four people, each on their own phone. Bots fill any empty seats.

1. The host taps **New game → Host a room** and gets a 4-character code such as `K7QX`.
2. Friends open the same page, tap **New game → Join a room** and enter the code, or open the host's invite link (`?room=K7QX`).
3. The host picks the seat count and score, then taps **Deal**.

The host's browser runs the game and sends each player only their own hand. Guests connect directly to the host over WebRTC using [PeerJS](https://peerjs.com); PeerJS's free public server only introduces them. That means:

- The page must be reachable by everyone, so it needs to be hosted (any static host works). A local server only works for phones on the same Wi-Fi.
- The game ends if the host closes the tab. A guest who drops, or reloads, gets a bot in their seat and can rejoin from the same tab with the same code.
- Some VPNs and very strict networks block direct connections.
