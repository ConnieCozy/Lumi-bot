# Changelog


## [0.1.0] - 2026-05-07
### add
- structure du bot + commandes de base


## [0.2.0] - 2026-05-07
### add
- commands and fix


## [0.3.0] - 2026-05-07
### improve
- ergonomics and fix


## [0.3.1] - 2026-05-08
### add
- +Cmd botinfo + fix (help, 8ball)


## [0.3.2] - 2026-05-08
### fix
- config restore


## [0.3.3] - 2026-05-08
### fix
- Deploy-commands + fix git


## [0.3.4] - 2026-05-09
### fix
- Fix cleanUp


## [0.4.0] - 2026-05-10
### improve
- database structure


## [1.0.0] - 2026-05-15
### improve
- Foundation Update: Complete Moderation System, New Database Architecture, Bot Architecture, Embed Visual Rework, New /help System and Smart Staff System


## [1.0.1] - 2026-05-15
### fix
-  fix weather and 8ball commands


## [1.1.0] - 2026-05-16
### improve
- AUTOMOD UPDATE V1: anti-spam, anti duplicate, escalation system, auto mute after warnings, automod logs, message delete logs, message updata logs, anti raid detection v1, automod enable / disable, moderation cases integration, multi-server automod suport
- 

## [1.1.1] - 2026-05-17
### refactor
- refactor logger + hotfix


## [1.2.0] - 2026-05-18
### add
-  improve botinfo, 8ball - add userinfo, serverinfo, avatar, roleinfo, stats, uptime, invite, dice, slap, hack + hotfix 


## [1.2.1] - 2026-05-19
### fix
- organization commands


## [1.3.0] - 2026-05-20
### improve
- Personality Update: /lumi with mood, motivation, lore. /choose, / insultme, rework dice: D6, D20, D100. 


## [2.0.0] - 2026-05-21
### improve
-  replace SQLite3 > Prisma databse + Hosting 24/7


## [2.0.1] - 2026-05-21
### fix
- Database + hotfix


## [1.2.0] - 2026-05-22
### improve
-  Added moderation system with Prisma, Added moderation case system, improve /lumi, /choose + hotfix (Fixed Prisma errors, Fixed guildSettings upsert system, Fixed Render deployment issues, Fixed weather command, Fixed Discord interaction errors, Fixed moderation case logs) + improve Added deploy commands script, Full migration to Prisma, logging system


## [2.2.1] - 2026-05-22
### fix
-  Hotfix interactiion error handlig


## [2.2.2] - 2026-05-22
### fix
-  Hotfix Weather


## [2.2.3] - 2026-05-23
### fix
- Hotfix Weather API, interactCreate


## [2.3.0] - 2026-05-23
### improve
-  starting  automatic slash command deployent


## [2.3.1] - 2026-05-24
### fix
-  Stability & Modernization Update: Replaced deprecated ephemeral: true, Migrated to MessageFlags.Ephemeral, Improved interaction error handling, Better protection against Discord API errors, Prepared internal systems for future updates


## [2.4.0] - 2026-05-25
### improve
- Lumi Bot v2.4.0 — Major Command Rework: Completely redesigned Help Menu, Weather Command Rework, Dice Command Rework, Internal Improvements


## [2.4.1] - 2026-05-26
### fix
- Reworked weather system: Added city selection menu, Added FR → EN aliase,Improved API error handling,  Created weatherEmbed system, Cleaned interactionCreate


## [3.0.0] - 2026-05-28
### refactor
-  Major Update: Logging and Moderation Updat| Complete logging system overhaul (message delete logs, message update logs, join / leave logs, moderation logs, command logs, automod logs) - New independent log toggles (Servers can now enable or disable every log category separately) - New Anti-Raid System (mass join detection, configurable join limit, configurable interval, full enable / disable support) - Moderation system improvement - Improved infractions system - Logging & embeds refactor - New latency command - Massive internal cleanup


## [3.1.0] - 2026-05-28
### add
- Deleted invite command, added community command, deleted toggleMemberLogs, deleted prisma data (MemberLogs), Fixes and cleaned up


## [3.2.0] - 2026-05-30
### imporve
-  Weather System Overhaul: Reworked the entire weather system, Replaced WeatherAPI city search with OpenStreetMap (Nominatim), Improved location accuracy for cities worldwide, Fixed incorrect city matches and unreliable search results, Better support for cities such as Brussels, London, Tokyo, Montreal, and many others, Removed dependency on weather API keys, Simplified weather data handling using Open-Meteo, Improved overall reliability and maintainability


## [3.2.1] - 2026-05-31
### fix
- hotfix Weather System Migration: Fully migrated weather system to OpenWeatherMap, Removed dependency on Open-Meteo, Improved weather command reliability, Reduced API rate-limit issues, Faster and more stable weather responses


## [3.2.2] - 2026-06-01
### fix
- Stability and security update: fixed moderation permission checks, stabilized AutoMod and anti-raid handling, added GuildSettings cache, improved event error isolation, added Prisma postinstall generation, prevented automatic command deployment on startup, and added safer moderation guards for mute, unmute and warn.


## [3.2.3] - 2026-06-01
### improve
- Stability polish update: added a shared command loader for startup and deployments, added a Render health endpoint, improved graceful shutdown, added `npm run check`, documented maintenance commands, made `/say` safer against unwanted mentions, improved `/clear` permission checks, blocked slash commands in DMs, and improved weather/deploy configuration errors.


## [3.2.5] - 2026-06-02
### improve
- Visual identity polish: added the new Lumi asset pack, removed outdated image assets, introduced the Lumi footer badge for embeds, and documented the optional footer icon URL configuration.


## [3.2.6] - 2026-06-03
### fix
- Patch cleanup and safety update: centralized embed footers without duplicated lightning text, added Lumi assistant v2 assets, removed non-approved legacy visual assets, strengthened release documentation, sanitized/truncated Discord log embeds, protected console logs from obvious secret leaks, and limited moderation reason inputs.


## [3.2.4] - 2026-06-01
### fix
- Maintenance and dependency cleanup: refreshed private architecture docs, marked image assets as binary for Git, and resolved npm audit warnings by overriding vulnerable indirect dependencies.


## [3.2.7] - 2026-06-03
### fix
- Moderation hardening and AutoMod cleanup: added shared target validation for moderation actions, blocked unsafe targets through role hierarchy checks, and cleaned temporary AutoMod tracking maps after inactivity.


## [3.2.8] - 2026-06-03
### fix
- Discord interaction hardening: centralized safe ephemeral replies, ignored expired or already acknowledged interactions cleanly, limited commands to guild contexts by default, and reduced internal error logs to lower sensitive information exposure.


## [3.2.10] - 2026-06-04
### fix
- Ownership and protection update: switched the package license to proprietary/unlicensed, added an all-rights-reserved repository license, and created a Lumi protection dossier with asset references, evidence tracking, official protection sources, and practical cost notes.

## [3.2.9] - 2026-06-04
### fix
- Security and reliability hardening: added safe error logging across runtime handlers, protected staff and dev message sends against unsafe mentions and missing permissions, improved command cooldown cleanup, guarded AutoMod timeout failures, sanitized moderation case reasons, and made shutdown/login failures safer.


## [3.3.0] - 2026-06-04
### improve
- Lumi UX and personality update: removed low-value novelty commands, merged bot statistics into an interactive `/botinfo` menu, moved choosing into `/lumi choose`, expanded Lumi's soft sarcastic futuristic personality, polished help/settings/log messages in French, and added safer settings/log channel checks plus anti-spam and anti-raid value limits.


## [3.3.1] - 2026-06-04
### fix
- Maintenance patch: moved the private update announcement owner check to `OWNER_USER_ID`, documented the new environment variable and polished AutoMod/anti-raid wording.


## [3.4.0] - 2026-06-04
### improve
- Command UX update: modernized moderation command wording and embeds, added a dedicated moderation footer, restored missing moderation logging for `/kick`, normalized visible slash option names such as `/help command`, `/userinfo user` and `/unban user_id`, improved slowmode permission handling, and polished small settings/help inconsistencies.


## [3.5.0] - 2026-06-05
### add
- Fun and personality update: added `/fortune`, plus interactive `/rps` and `/tictactoe` commands with Lumi-flavored responses, button-based gameplay, basic session protection and optional duels against another member, polished `/lumi choose` wording, and removed the duplicate API latency entry from `/botinfo` statistics.


## [3.6.0] - 2026-06-05
### add
- Lumi Assistant update: added `/checklist`, `/pulse`, `/spark` and admin-only `/feedback`, refreshed the Lumi help category wording, clarified Lumi's AI assistant lore in docs and personality text, documented `FEEDBACK_CHANNEL_ID`, and introduced a centralized permission matrix for sensitive slash commands.


## [3.7.0] - 2026-06-06
### add
- Moderation logs visibility update: added `/togglemoderationlogs`, connected moderation logs back into Lumi's assistant checklist, and kept moderation log controls admin-only for safer server configuration.


## [3.8.0] - 2026-06-06
### add
- Welcome and goodbye system: added configurable welcome/goodbye channels, automatic member greeting embeds, admin-only test and clear commands, connected the new server greeting setup to `/checklist` and `/pulse`, added paginated `/help` categories for long command lists, and kept community links centralized in `/community` instead of duplicating them in `/help`.


## [4.0.0] - 2026-06-06
### add
- Internal configuration dashboard update: replaced duplicated toggle/set/test/diagnostic commands with a unified `/configuration` menu for general server settings, log status, welcome/goodbye testing and AutoMod status, added in-menu ON/OFF buttons, channel and role selectors, in-menu log delivery tests, reduced visible slash command clutter, connected member log status to `/pulse`, centralized embed delivery permission checks for log and greeting channels, and hardened log delivery with channel fetch and permission checks before sending embeds.


## [4.1.0] - 2026-06-06
### improve
- Moderation dashboard and data cleanup update: added a unified `/moderation` menu for sanctions, sanction removals, moderation records and slowmode, moved anti-spam and anti-raid limit/interval tuning into `/configuration`, made `/help` and `/botinfo` ephemeral without close buttons, fixed custom moderation-role access by relying on Lumi's internal guard instead of native Discord command permissions, removed obsolete duplicated moderation/settings commands, dropped the unused `UserLevels` XP/level model and migration target, and clarified command logs as an advanced audit option to avoid noisy log channels.


## [4.2.0] - 2026-06-07
### add
- Staff, Lumi and game UX update: replaced standalone staff utilities with a unified `/staff` panel for status, messages, uploaded-file embed drafts, multi-section embed fields and cleanup, kept `/lumi` as lightweight public subcommands while improving its help/usage visibility, added a short `guildCreate` onboarding guide when Lumi joins a server, logged staff cleanup through message delete logs, added shared emoji constants for repeated status/action markers, removed the obsolete settings category from help, simplified `/configuration` status labels with colored dots, and added safer RPS/TicTacToe duel flows with accept/decline buttons, visible inactivity expiry and rematch buttons.


## [4.3.0] - 2026-06-07
### add
- Server visibility and free-plan cleanup update: added a `/configuration` server logs toggle for role, channel, category, guild profile and cached user profile changes using the existing main log channel, added temporary BO3 score tracking for RPS and TicTacToe rematches without storing game scores in Neon, removed unused ticket settings and the legacy member log column from Prisma, added read-only Neon helper views for channel, log and AutoMod settings, and refreshed the public README with Lumi's invite link and clearer roadmap wording.


## [4.4.0] - 2026-06-07
### add
- Staff role management update: added a secured `/staff` members panel with member and role selectors, hierarchy checks, managed-role and administrator-role safeguards, add/remove role actions, private staff feedback, server log entries for role changes made through the panel, clearer staff help wording, and more readable server log emojis for role, channel, permission, guild and profile events.


## [4.5.0] - 2026-06-11
### add
- Server visibility and public documentation update: added more precise role, channel, guild, member and message update logs with safer long-message previews, routed AutoMod logs to the dedicated AutoMod log channel when configured, added an anti-spam ignored channel setting in `/configuration`, clarified AutoMod protection versus AutoMod log toggles for Neon and UX readability, added automatic guild data cleanup when Lumi leaves a server, added periodic presence refresh for long-running hosting, introduced the `/fish` command with fishing spots, rarity tiers, capture scores, lightweight personal records and a server Top 3, updated `/dice` critical result rules for D20 and D100, improved `/roleinfo` and detailed `/help` output, added mobile emoji guidance for staff messages, linked public documents from `/community`, added privacy, terms and data request documentation, and refreshed the public README protection wording.


## [4.6.0] - 2026-06-12
### add
- Free-plan and Fish v2 update: added a configurable guild capacity guard with a default 25-server limit, polite over-capacity onboarding refusal and automatic cleanup, exposed live capacity in `/botinfo`, `/community` and `/pulse`, reworked `/fish` into `catch`, `top` and `profile` subcommands with harder rarity odds, weighted catches, weekly and permanent server rankings plus previous-week winner display without storing full catch history, added automatic cleanup for inactive fish records, added local Lumi GIF reactions through `/lumi react`, updated Prisma fish records for lightweight weekly stats, refreshed free-plan documentation and kept the public README aligned with v4.6.0.


## [4.6.1] - 2026-06-12
### fix
- Fish data cleanup patch: removed stored fish spot columns now that fishing spots are narrative-only, cleaned fish profile output to avoid displaying unused spot data, removed non-approved Lumi reaction GIF assets from the release set, and aligned public data documentation with the lighter Fish v2 storage model.


## [5.0.0] - 2026-06-13
### add
- Premium private assistant direction update: repositioned Lumi as a limited premium private AI assistant, changed the default capacity to 5 guilds, added a maximum guild member guard, introduced readable guild metadata with guild names, owner IDs, member counts, access status, trial expiration and last-seen timestamps, added code-based `/access` trials, added owner-only `/serveradmin` listing, approval and leave cleanup tools, blocked non-approved guilds from using normal commands during pending or expired access states, added feedback-channel notifications for private access requests, added delayed cleanup for pending guilds without activation, refreshed community, pulse, bot info, README and public data documentation, renamed the internal maintenance README to avoid confusion with the public README, added dynamic presence capacity text, and stored lightweight user/moderator tags on new moderation cases for better readable records.


## [5.1.0] - 2026-06-13
### improve
- Pro logs, data retention and UX audit update: improved server/message/member/role/channel log readability with mentions, names and IDs while preventing unwanted log pings, centralized fish and optional moderation case retention cleanup, added periodic data retention checks on startup/runtime, clarified private-assistant help wording, added detailed `/help command` option/subcommand visibility, tightened `/pulse` versus `/spark` command descriptions, simplified configuration checklist status wording, refreshed privacy and maintenance documentation, and kept the command set audit focused on clarity instead of removing useful grouped commands.


## [5.1.1] - 2026-06-13
### fix
- Database resilience patch: added safe handling for temporary Prisma/Neon connection failures, prevented AutoMod and member events from spamming full database errors, added a throttled database-unavailable logger, allowed log delivery to use cached guild settings when available, returned a clear temporary-unavailable message for commands that need the database, kept public help/community/botinfo commands usable during access checks, and cleaned the `/spark` help wording.


## [5.2.0] - 2026-06-14
### improve
- Server log and Fish optimization update: simplified channel, role, member and user profile logs to avoid repeated identity blocks, removed duplicated channel/role names from log identities, ignored permission-only channel updates emitted immediately after channel creation, added more precise channel permission overwrite details, added optional audit-log responsible fields for channel, role and guild changes when Discord permissions allow it, documented the audit-log permission behavior, reduced `/fish catch` database reads by moving full leaderboard display back to `/fish top`, kept only the player's current weekly rank in catch results, throttled inactive fish cleanup per guild, added safer database-unavailable handling for fish records and rankings, and completed a command UX audit with no active duplicate command names found.


## [5.3.0] - 2026-06-14
### add
- Fish ranked seasons and autorole update: added lightweight monthly fishing seasons, added seasonal rank progression from Iron to Challenger based on monthly catches, best seasonal rarity and best seasonal score, colored fish catch/profile embeds by rank, added seasonal rank and next-rank hints to `/fish catch`, added a seasonal leaderboard to `/fish top`, kept total catches permanent while monthly ranks reset, reminded users about `/fish profile`, added a secured configurable arrival autorole in `/configuration`, blocked unsafe/high/managed autoroles, logged autorole assignment during member joins, exposed autorole status in `/pulse`, and documented the new seasonal fish storage.


## [5.3.2] - 2026-06-14
### fix
- Fish rank display hotfix: fixed `/fish catch` seasonal progress so the next rank is calculated from the saved seasonal record instead of a reduced response object, preventing the current rank from being shown again as the next rank.
## [5.3.1] - 2026-06-14
### fix
- Maintenance cleanup patch: centralized shared feedback emojis, exposed the common emoji set from config, moved Fish rank embed colors into the shared color config, replaced repeated configuration status markers with common emoji constants, and kept the update behavior-neutral before the next role and verification features.


## [5.3.3] - 2026-06-14
### improve
- Fish catch UX cleanup: simplified `/fish catch` result fields so catches stay quick to read, kept detailed season progression inside `/fish profile`, and kept the weekly podium details focused in `/fish top`.


## [5.4.0] - 2026-06-15
### add
- Member onboarding and creator tools update: added `/verification` for the non-verified to verified member flow using the existing arrival autorole, added a lightweight Lumi verification modal, added `/roles panel` for persistent role buttons with add and toggle modes, added safe role permission checks for automatic role assignment systems, added automatic creator posts for Twitch live starts and latest YouTube uploads with a tiny duplicate-prevention state table, kept `/creator announce` as a manual backup, added separate home-server Discord channels for Twitch and YouTube, added new Lumi GIF reactions while removing off-tone duplicate assets, exposed verification state in `/pulse` and assistant checks, documented verification, role buttons, creator env vars and privacy impact, and added the required Prisma fields for verification and creator feed state.


## [5.5.0] - 2026-06-16
### improve
- Staff tools and server log update: added a lightweight private ticket system with panel buttons, private ticket channels, optional ticket archive summaries and temporary Prisma tracking for open tickets only; updated privacy and data request documentation for ticket data transparency; reworked channel create/delete/update logs with a clearer Discord-style presentation; added permission-per-target channel update details with long-list limits; expanded French permission labels; ignored noisy permission-only updates right after channel creation; suppressed duplicate member logs when roles are changed from role panels; required explicit custom titles for role panels; moved creator announcements into the dev help category; and allowed longer update/creator announcement text.


## [5.5.1] - 2026-06-16
### fix
- Ticket command deployment hotfix: removed the Discord-level default permission that could hide `/ticket` from staff command lists, kept the Manage Channels safety check inside Lumi, fixed the `/roles panel` option order so Discord accepts command deployment, and moved the creator announcement command file into the dev command folder.
