# Quest Design Guidelines (Staff)

> **Staff workspace:** This page is intentionally editable. Use it to establish consistent quest standards before creating quests in the live server. Replace placeholders with the team's decisions.

## 1. Purpose

Quests should give players clear goals, encourage exploration and community participation, and add variety to normal survival gameplay. They should fit BetterTowny's modern Towny identity and support the economy rather than undermine it.

## 2. Quest categories

Choose one primary category for each quest.

- **Onboarding:** teaches new players core systems.
- **Exploration:** encourages visiting locations or discovering landmarks.
- **Gathering:** asks for eligible resources.
- **Crafting:** asks players to create useful items.
- **Town life:** encourages joining, contributing to, or developing a town.
- **Jobs and skills:** highlights jobs or mcMMO progression.
- **Community:** encourages fair trading, cooperation, or events.
- **Story / lore:** builds the server's setting and recurring characters.
- **Repeatable / daily / weekly:** provides recurring goals with carefully balanced rewards.
- **Seasonal / event:** limited-time content with an announced start and end.

## 3. Every quest must define

Before publishing, document:

1. **Quest ID:** stable, unique identifier used by staff.
2. **Title:** short, distinctive, player-facing name.
3. **Summary:** one or two sentences explaining the goal.
4. **Quest giver:** NPC, menu, command, board, or automatic trigger.
5. **Prerequisites:** required rank, earlier quest, level, location, or none.
6. **Objectives:** specific, measurable conditions.
7. **Progress feedback:** how the player knows what remains.
8. **Completion condition:** the exact condition that finishes the quest.
9. **Rewards:** money, items, cosmetics, points, reputation, or unlocks.
10. **Repeat rules:** one-time, repeatable, cooldown, or seasonal.
11. **Failure / cancellation behavior:** what happens if a player abandons it.
12. **Testing notes:** edge cases checked before release.

## 4. Objective writing standards

Good objectives are clear, measurable, and achievable without guesswork.

**Prefer:**
- “Deliver 16 bread to the Quartermaster.”
- “Visit the market district and speak to the Trade Clerk.”
- “Earn $250 from eligible job actions.”
- “Contribute 32 logs to the town supply chest.”

**Avoid:**
- “Help the town.”
- “Get rich.”
- “Explore a lot.”
- “Collect some materials.”

When a task depends on a specific world, region, item variant, or plugin event, state it clearly. Do not require a player to guess which item or location counts.

## 5. Reward balancing

Rewards should feel meaningful without making normal progression irrelevant.

- Compare the reward to the time and difficulty required.
- Check the value of requested items against typical player-shop prices.
- Avoid rewards that create a repeatable money or item duplication loop.
- Treat rare items, permanent cosmetics, and unlocks as higher-impact rewards.
- Give new-player quests useful direction without handing out excessive wealth.
- Ensure repeatable quests have cooldowns or caps where needed.
- Do not make paid perks mandatory for completing standard quests.
- Document whether rewards can be traded, sold, stacked, or claimed more than once.

**Reward budget / guidance:** [EDIT: define target reward ranges by quest tier.]

## 6. Difficulty tiers

| Tier | Intended audience | Design guidance |
|---|---|---|
| Introductory | New players | Teach one system; low risk and low cost |
| Standard | Regular players | A short objective or modest multi-step chain |
| Advanced | Established players | More planning, travel, cooperation, or resource investment |
| Epic / event | Community or endgame | Longer chain, special conditions, and carefully reviewed rewards |

Adjust the labels to match the server's final progression system.

## 7. Fairness and accessibility

- Do not require access to a private town unless the quest explicitly says so.
- Provide alternatives when a rare resource or location may be unavailable.
- Avoid objectives that can be completed only by monopolizing a public resource.
- Clearly disclose PvP, dangerous travel, item-loss, or time-limit risks.
- Avoid quests that require players to break another player's rules or protections.
- Make dialogue and instructions readable, concise, and consistent.

## 8. Technical checklist

Before release, test with a normal player account.

- [ ] Quest can be started by the intended players.
- [ ] Prerequisites work and cannot be bypassed.
- [ ] Every objective increments correctly.
- [ ] Progress survives logout/restart if it is supposed to.
- [ ] Item delivery checks the correct item type and quantity.
- [ ] Rewards are granted exactly once.
- [ ] Repeat and cooldown rules work.
- [ ] Abandoning or failing the quest behaves correctly.
- [ ] NPC, menu, command, and dialogue links work.
- [ ] Quest does not conflict with Towny protections, jobs, mcMMO, or economy rules.
- [ ] Reward values and exploits have been reviewed.
- [ ] Player-facing wording has been proofread.

## 9. Publishing workflow

1. Draft the quest using the template below.
2. Review objectives and reward value with another staff member.
3. Test on a staging server or with a test account.
4. Record the quest ID, config file, author, and date.
5. Publish the quest and add it to the public quest index.
6. Monitor player feedback and economy impact after launch.
7. Update this wiki if the quest rules or rewards change.

## 10. Editable quest template

Copy this block for each new quest.

---

### [QUEST TITLE]

- **Quest ID:** `[unique_id]`
- **Category:** `[onboarding / exploration / gathering / town / jobs / skills / community / story / repeatable / event]`
- **Difficulty:** `[introductory / standard / advanced / epic]`
- **Quest giver:** `[NPC name and location, menu, command, or trigger]`
- **Availability:** `[always available / dates / world / other restrictions]`
- **Prerequisites:** `[none or list]`
- **Repeat rule:** `[one-time / cooldown / daily / weekly / seasonal]`

**Player-facing summary:**  
[Write a concise explanation of the quest.]

**Dialogue / flavour text:**  
[Optional dialogue. Keep instructions understandable even when the player skips flavour text.]

**Objectives:**
1. [Specific measurable objective.]
2. [Specific measurable objective.]
3. [Optional objective.]

**Completion condition:**  
[Exact condition that marks the quest complete.]

**Rewards:**
- Money: `[amount]`
- Items: `[item, quantity, relevant metadata]`
- Cosmetic / points / unlock: `[details]`
- Other: `[details]`

**Failure / cancellation:**  
[What happens to progress and any submitted items.]

**Technical implementation:**
- Plugin / config file: `[name and path]`
- Trigger / objective identifiers: `[details]`
- Commands / permissions: `[details]`

**Test cases:**
- [ ] Normal completion
- [ ] Relog / restart
- [ ] Duplicate reward prevention
- [ ] Invalid item or partial quantity
- [ ] Prerequisite bypass attempt
- [ ] Repeat / cooldown check
- [ ] Towny / economy / jobs / mcMMO interaction

**Review record:**
- Author: `[name]`
- Reviewer: `[name]`
- Last tested: `[date]`
- Status: `[draft / testing / published / retired]`

---
