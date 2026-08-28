# Changelog Lumi 4.x

[Retour au changelog actuel](CHANGELOG.md)

## [4.6.1] - 2026-06-12
### fix
- Fish data cleanup patch: removed stored fish spot columns now that fishing spots are narrative-only, cleaned fish profile output to avoid displaying unused spot data, removed non-approved Lumi reaction GIF assets from the release set, and aligned public data documentation with the lighter Fish v2 storage model.


## [4.6.0] - 2026-06-12
### add
- Free-plan and Fish v2 update: added a configurable guild capacity guard with a default 25-server limit, polite over-capacity onboarding refusal and automatic cleanup, exposed live capacity in `/botinfo`, `/community` and `/pulse`, reworked `/fish` into `catch`, `top` and `profile` subcommands with harder rarity odds, weighted catches, weekly and permanent server rankings plus previous-week winner display without storing full catch history, added automatic cleanup for inactive fish records, added local Lumi GIF reactions through `/lumi react`, updated Prisma fish records for lightweight weekly stats, refreshed free-plan documentation and kept the public README aligned with v4.6.0.


## [4.5.0] - 2026-06-11
### add
- Server visibility and public documentation update: added more precise role, channel, guild, member and message update logs with safer long-message previews, routed AutoMod logs to the dedicated AutoMod log channel when configured, added an anti-spam ignored channel setting in `/configuration`, clarified AutoMod protection versus AutoMod log toggles for Neon and UX readability, added automatic guild data cleanup when Lumi leaves a server, added periodic presence refresh for long-running hosting, introduced the `/fish` command with fishing spots, rarity tiers, capture scores, lightweight personal records and a server Top 3, updated `/dice` critical result rules for D20 and D100, improved `/roleinfo` and detailed `/help` output, added mobile emoji guidance for staff messages, linked public documents from `/community`, added privacy, terms and data request documentation, and refreshed the public README protection wording.


## [4.4.0] - 2026-06-07
### add
- Staff role management update: added a secured `/staff` members panel with member and role selectors, hierarchy checks, managed-role and administrator-role safeguards, add/remove role actions, private staff feedback, server log entries for role changes made through the panel, clearer staff help wording, and more readable server log emojis for role, channel, permission, guild and profile events.


## [4.3.0] - 2026-06-07
### add
- Server visibility and free-plan cleanup update: added a `/configuration` server logs toggle for role, channel, category, guild profile and cached user profile changes using the existing main log channel, added temporary BO3 score tracking for RPS and TicTacToe rematches without storing game scores in Neon, removed unused ticket settings and the legacy member log column from Prisma, added read-only Neon helper views for channel, log and AutoMod settings, and refreshed the public README with Lumi's invite link and clearer roadmap wording.


## [4.2.0] - 2026-06-07
### add
- Staff, Lumi and game UX update: replaced standalone staff utilities with a unified `/staff` panel for status, messages, uploaded-file embed drafts, multi-section embed fields and cleanup, kept `/lumi` as lightweight public subcommands while improving its help/usage visibility, added a short `guildCreate` onboarding guide when Lumi joins a server, logged staff cleanup through message delete logs, added shared emoji constants for repeated status/action markers, removed the obsolete settings category from help, simplified `/configuration` status labels with colored dots, and added safer RPS/TicTacToe duel flows with accept/decline buttons, visible inactivity expiry and rematch buttons.


## [4.1.0] - 2026-06-06
### improve
- Moderation dashboard and data cleanup update: added a unified `/moderation` menu for sanctions, sanction removals, moderation records and slowmode, moved anti-spam and anti-raid limit/interval tuning into `/configuration`, made `/help` and `/botinfo` ephemeral without close buttons, fixed custom moderation-role access by relying on Lumi's internal guard instead of native Discord command permissions, removed obsolete duplicated moderation/settings commands, dropped the unused `UserLevels` XP/level model and migration target, and clarified command logs as an advanced audit option to avoid noisy log channels.


## [4.0.0] - 2026-06-06
### add
- Internal configuration dashboard update: replaced duplicated toggle/set/test/diagnostic commands with a unified `/configuration` menu for general server settings, log status, welcome/goodbye testing and AutoMod status, added in-menu ON/OFF buttons, channel and role selectors, in-menu log delivery tests, reduced visible slash command clutter, connected member log status to `/pulse`, centralized embed delivery permission checks for log and greeting channels, and hardened log delivery with channel fetch and permission checks before sending embeds.
