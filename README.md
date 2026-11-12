# Golden Man

A client-side Fabric mod for Hypixel SkyBlock (Minecraft 26.2) that enforces the Golden Man challenge.

## Rules
- **Bazaar:** insta-sell only. No buy orders, no sell offers.
- **Bazaar buys:** only Booster Cookies, instant buy only.
- **Auction House:** completely off-limits.
- **Trading:** only with your co-op members.
- NPC shops and the Dark Auction are fine.

## In-game commands
| Command | What it does |
|---|---|
| `/goldenman` | Status for your current profile |
| `/goldenman start` → `/goldenman start confirm` | Turn Golden Man on for the profile you're on |
| `/goldenman stop` → `/goldenman stop confirm` | Turn it off |
| `/goldenman coop add/remove/list <name>` | Co-op members you're allowed to trade with |
| `/goldenman rules` | Show the rules |
| `/goldenman debug` | Show menu titles and clicked buttons in chat (for fixing detection) |

The mod learns which profile you're on from Hypixel's `Profile ID:` chat message, which appears when you join SkyBlock.
Rules only apply to profiles you've started Golden Man on.

## Building (Windows)
1. Open this folder in IntelliJ IDEA (**File → Open → GoldenMan**). Let it import the Gradle project.
2. If asked for a JDK, pick **corretto-26** or **openjdk-27** (anything 25 or newer).
3. Open the **Gradle** panel (elephant icon on the right) → **GoldenMan → Tasks → build → build**.
4. The mod appears at `build/libs/goldenman-0.1.0.jar`. Copy it into your SkyBlock Enhanced instance's `mods` folder.

## Roadmap
- v2: `/goldenman start` opens a prefilled GitHub issue; a GitHub Action verifies profiles via the Hypixel API and publishes a list.
- v3: verified players get a gold shimmer in the tab list; confirmed cheaters get a strikethrough.
