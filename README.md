# Squeek Wheel Run — MVP (Direct route, no IMD)

Single-page browser game. Open `index.html` directly in a browser, or serve this
folder with any static server. No build step, no wallet, no token, no backend.

## What it does
- Canvas runner: hamster (drawn in code, original art — not the official logo asset),
  jump over tall obstacles, duck under low ones, collect seeds.
- Strategies before a round: Sprint / Jog / Rest, affecting speed and stamina.
- 60-second MVP round: distance + seeds = score, minus collision penalties.
  Local top-5 board only (browser localStorage on the player's device).
- Live panel: fetches https://api.squeekchain.com/v1/status every 15 seconds and
  shows Squeek block height, settled-through round, cumulative work and core status.
  A newly detected block gives a short in-game speed boost.
  If the API is unreachable, the panel says "offline" and the game still plays
  locally — no live number is invented.

## Honest limits (important for the Direct submission)
- The 60-second round is an MVP test round. It is NOT a SqueekCore 10-minute round.
  SqueekCore rounds are only shown as live reference data in the panel.
  Before submitting to Squeekchain, either (a) state this clearly on the page, or
  (b) change the game round to follow a real SqueekCore round.
- No global leaderboard, no token rewards, no staking, no betting in this MVP.
- This folder is NOT yet the submitted project. Direct submission still needs:
  1. a domain owned by the user,
  2. a public GitHub repo for this project,
  3. the site live on that domain,
  4. the DNS record given by squeekchain.com added to the domain,
  5. the page tag given by squeekchain.com added to the live site,
  6. the repository line given by squeekchain.com added to the repo README,
  7. pressing Verify in the user's Genesis account, then automatic check + team review.
- Verification records are rechecked daily by Squeekchain: do not remove the DNS
  record, page tag, or repo line after approval, or the project (and, if it is the
  only approved project, the Buildooooor badge) can be lost.
