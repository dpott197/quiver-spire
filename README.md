# Quiver Spire

A TowerFall-style archery arena that runs in the browser. Fight AI archers solo, or host an online room and send friends a link.

**Play:** https://dpott197.github.io/quiver-spire/

## Modes

Every mode is played in rounds. A round lasts until one archer (or one team) is left, or 90 seconds pass.

| Mode | How you score |
| --- | --- |
| **Head Hunters** (default) | 1 point per KO. First to the KO target wins. |
| **Last Man Standing** | 1 point for being the last archer alive in a round. |
| **Team Head Hunters** | Red against Blue. Every KO scores for your team. Teammates can't hurt each other. |

Your own arrows never hurt you. A match ends at the end of a round once someone has reached the target with a clear lead.

## Treasure

Chests drop into the arena during each round. Touch one to open it. Power-ups last until the round ends.

| Power-up | Effect |
| --- | --- |
| Bomb arrows | Two arrows that explode on impact |
| Laser arrows | Two fast arrows that fly straight and bounce off walls |
| Bramble arrows | Two arrows that leave thorns rivals can't touch |
| Drill arrows | Two arrows that bore through one block |
| Shield | Blocks the next hit |
| Wings | Flap as often as you like in mid-air |
| Speed boots | Run faster |

Chests can be turned off in the match setup.

## Online play

1. Click **Host online**. You get a link like `https://dpott197.github.io/quiver-spire/#K7QX5`.
2. Send it to up to three friends. They open it, pick a name and join.
3. In Team Head Hunters, click a seat's team button in the lobby to move it between Red and Blue.
4. Click **Start match**. AI archers fill any empty seats, and take over if someone leaves.

### Fixed room codes

Type a code (4–16 letters or digits) in **Room code** before hosting to get the same link every time, for example https://dpott197.github.io/quiver-spire/#MONSIEUR. Anyone who opens that link while the room is open joins it. If nobody is hosting, the page offers **Host this room**, so whoever arrives first can open it.

The host's browser runs the match and friends connect to it directly over WebRTC ([PeerJS](https://peerjs.com/) handles the connection setup). There is no game server. The host should keep the page open for the whole match. A few strict networks block direct connections; if a friend can't join, try another network.

## Controls

| Action | Keys |
| --- | --- |
| Run | ← → or A D |
| Aim up / down, drop through ledges | ↑ ↓ or W S |
| Jump, double-jump in mid-air, wall-jump | Z, J or Space |
| Shoot (8 directions) | X or K |
| Dodge (catches arrows) | C, L or Shift |
| Super jump | Jump during a dodge on the ground: a higher jump that keeps the dash speed |
| Pause (host only online) | Esc or P |

**Controller:** any controller the browser recognises works (Xbox, PlayStation, Switch Pro and most others). Stick or d-pad to move and aim, A jump, X or Y shoot, B or any bumper or trigger dodge, Start to begin a match or pause. Press a button once after plugging it in so the browser notices it.

Phones get on-screen buttons.

The whole game is `index.html`, with no build step.
