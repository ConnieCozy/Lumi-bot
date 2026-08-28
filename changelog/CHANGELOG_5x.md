# Changelog Lumi 5.x

[Retour au changelog actuel](CHANGELOG.md)

## [5.11.0] - 2026-08-24
### improve
- Stability, security and cleanup update: added Discord Gateway disconnect, reconnect, resume and invalid-session diagnostics with safe automatic process recovery after failed startup or a prolonged outage; replaced the basic web probe with a strict cached `/health` check for Discord and Neon plus a Discord-focused `/ready` endpoint that does not keep the free database compute awake; updated Axios and Discord.js and reduced npm audit findings from ten to three Prisma CLI-only findings reserved for the dedicated Prisma 7 migration; redacted Discord interaction/webhook tokens and the private access code from logs; protected the initial `/staff` panel with the configured moderator-role check; added per-server access-code attempt limits with constant-time hash comparison; tightened free-text limits, server ID validation and weather request timeouts; removed the unused Twitch/YouTube creator command, automatic poster, creator database table, environment variables, local creator logos and GIF reaction command/assets; rebalanced Master, Grandmaster and Challenger fishing progression while increasing legendary and mythic chances without removing the location score bonuses; expanded `npm run check` with free-input and secret-redaction regressions; refreshed private maintenance, architecture, privacy and project documentation; and bumped Lumi to 5.11.0.

## [5.10.5] - 2026-08-20
### fix
- Runtime diagnosis patch: expanded the web health response with Discord readiness details and added a `/ready` endpoint that returns `503` when the Discord client is not connected, making Render/UptimeRobot checks able to distinguish a live web server from a truly connected Lumi bot.

## [5.10.4] - 2026-06-28
### fix
- Staff role log cleanup: moved manual role changes into clear role-added/role-removed logs, kept `/staff` role changes in command-origin logs without duplicate member-update posts, kept member-update logs focused on nickname changes, and added the target member avatar thumbnail to role logs.

## [5.10.3] - 2026-06-22
### fix
- Configuration panel hotfix: prevented the anti-spam ignored-channel picker from being rendered twice when opened through the generic settings selector, fixing Discord's duplicated component custom ID error, and extended the local check script to catch duplicated component IDs and invalid slash option ordering before deployment.

## [5.10.2] - 2026-06-20
### fix
- Fish rank hotfix: removed the mythic-only wall from Diamond, Master and Grandmaster progression so strong legendary seasonal records can keep advanced players in the intended high ranks, while Challenger still remains the final mythic-level chase rank.

## [5.10.1] - 2026-06-20
### fix
- Fish balance patch: made high seasonal ranks less frustrating by lowering the Grandmaster and Challenger score/catch walls, increased rare/epic/legendary/mythic catch odds while keeping mythic rare, made high-rarity fishing spots favor the storm cache more often, raised late-rarity score ranges and spot bonuses slightly, made fish weights feel more rewarding, sanitized database-unavailable logs during fish and moderation cleanup tasks, and bumped Lumi to 5.10.1.

## [5.10.0] - 2026-06-18
### add
- Temporary voice, creator logo and fish tuning update: added a lightweight `/voice` staff-category system for temporary voice channels with setup/status controls, owner or staff room actions, rename, limit, lock, unlock, transfer, one active room per owner, a configurable active-room cap, the required `GuildVoiceStates` intent, stricter lock handling that blocks regular members while keeping the configured mod role and administrators able to join, startup cleanup for empty or missing rooms, guild-leave cleanup for temporary voice rows, and temporary voice log suppression to keep server logs clean. Added local logo thumbnail support for creator announcements and Steam/Epic free game posts, applied Twitch/YouTube thumbnails to automatic and manual creator posts, improved free game offer end dates with relative and full Discord timestamps, added clearer channel log title emojis, slightly increased legendary and mythic fish catch odds while keeping them rare, documented temporary voice storage and the decision to avoid birthday data, and bumped Lumi to 5.10.0.


## [5.9.1] - 2026-06-17
### fix
- Ticket staff role hotfix: allowed the configured ticket staff role and Lumi moderation role to claim, update and close tickets without requiring heavy Discord channel-management permissions, added the moderation role to new ticket channel overwrites, synced ticket archive/log channel visibility for configured staff roles when publishing the ticket panel, kept ticket configuration changes restricted to users with channel-management permissions, and bumped Lumi to 5.9.1.


## [5.9.0] - 2026-06-17
### add
- Ticket v3 and free games update: reworked ticket panels into a member-driven flow where users choose the ticket type and provide a short summary before channel creation, added temporary ticket type, summary, status, claimed-staff and staff tracker message fields, blocked ticket authors from writing until staff claims the ticket, replaced noisy ticket archive spam with one editable staff-side tracker message that turns grey, green or red through the ticket lifecycle, made ticket closure reasons mandatory, added `/freegames` with private quick previews, rich per-game public posts, settings and optional auto-posting for Steam/Epic free game discovery, added a lightweight per-guild duplicate-prevention state table, added a simple user guide document, refreshed private maintenance/project docs, renamed the internal free games utility service for clarity, and bumped Lumi to 5.9.0.


## [5.8.0] - 2026-06-17
### improve
- Level rewards, ticket and role panel update: added visual Lumi rank tiers to XP/Level profiles, leaderboards and level-up embeds without assigning Discord roles or adding database tables; upgraded ticket panels with selectable ticket types, typed ticket channels, richer welcome/log embeds and a staff claim button that stays lightweight in Discord; extended role button panels with a remove-only mode and sanitized custom panel text; simplified channel and role log identities to prefer display names over numeric IDs while keeping user IDs for moderation proof, cleaned message edit/delete logs by removing unnecessary message ID fields, refreshed private maintenance documentation and bumped the public README version badge.


## [5.7.0] - 2026-06-16
### improve
- Duel and stability cleanup: replaced the separate `/rps` and `/tictactoe` slash commands with a unified `/duel` command that launches either rock-paper-scissors or tic-tac-toe against Lumi or another member, switched new duel replies to Discord's `withResponse` flow, improved stale or out-of-order duel button feedback, made BO3 rematches start directly after the first accepted duel, updated rematch guidance to the new command path, allowed message-based settings lookup to reuse a recent cache during short database outages, kept duplicate and volume AutoMod warnings from crashing when a moderation case cannot be stored during a temporary database issue, allowed Lumi's ready flow to keep starting presence and timers when startup metadata sync is skipped during a short database outage, and cleaned up ticket channels automatically if their database record cannot be created.


## [5.6.1] - 2026-06-16
### fix
- Final stability patch: restored XP and level embeds to Lumi's standard blue instead of the Twitch lavender, tightened private-access checks for old component interactions so expired or unauthorized guilds cannot keep using stale panels, made developer update replies ephemeral, and updated the owner cleanup reply to include level and ticket cleanup counts.


## [5.6.0] - 2026-06-16
### add
- XP, level and log clarity update: added a lightweight `/level` system with member profiles, server leaderboard, staff settings, message-based XP gains, a one-minute anti-spam cooldown, optional level-up announcement channels, level profile embeds, a compact `UserLevel` Prisma model, automatic XP cleanup when members leave a guild, and full level cleanup when Lumi leaves a guild. Also improved ticket archives with clearer member/staff/reason/duration/date summaries, removed temporary ticket channel references from archive logs, ignored temporary ticket channels in server and message logs to avoid stale `#unknown` references, simplified channel permission logs to focus on useful allowed or revoked permissions, softened Twitch creator embeds with a shared lavender color, and updated privacy, data request, maintenance and architecture documentation.


## [5.5.2] - 2026-06-16
### fix
- Ticket closure permission hotfix: restricted ticket closing to staff members only, including the close button, while keeping ticket owners able to write inside their private ticket until staff closes it.


## [5.5.1] - 2026-06-16
### fix
- Ticket command deployment hotfix: removed the Discord-level default permission that could hide `/ticket` from staff command lists, kept the Manage Channels safety check inside Lumi, fixed the `/roles panel` option order so Discord accepts command deployment, and moved the creator announcement command file into the dev command folder.


## [5.5.0] - 2026-06-16
### improve
- Staff tools and server log update: added a lightweight private ticket system with panel buttons, private ticket channels, optional ticket archive summaries and temporary Prisma tracking for open tickets only; updated privacy and data request documentation for ticket data transparency; reworked channel create/delete/update logs with a clearer Discord-style presentation; added permission-per-target channel update details with long-list limits; expanded French permission labels; ignored noisy permission-only updates right after channel creation; suppressed duplicate member logs when roles are changed from role panels; required explicit custom titles for role panels; moved creator announcements into the dev-only command area; and allowed longer update/creator announcement text.


## [5.4.0] - 2026-06-15
### add
- Member onboarding and creator tools update: added `/verification` for the non-verified to verified member flow using the existing arrival autorole, added a lightweight Lumi verification modal, added `/roles panel` for persistent role buttons with add and toggle modes, added safe role permission checks for automatic role assignment systems, added automatic creator posts for Twitch live starts and latest YouTube uploads with a tiny duplicate-prevention state table, kept `/creator announce` as a manual backup, added separate home-server Discord channels for Twitch and YouTube, added new Lumi GIF reactions while removing off-tone duplicate assets, exposed verification state in `/pulse` and assistant checks, documented verification, role buttons, creator env vars and privacy impact, and added the required Prisma fields for verification and creator feed state.


## [5.3.3] - 2026-06-14
### improve
- Fish catch UX cleanup: simplified `/fish catch` result fields so catches stay quick to read, kept detailed season progression inside `/fish profile`, and kept the weekly podium details focused in `/fish top`.


## [5.3.2] - 2026-06-14
### fix
- Fish rank display hotfix: fixed `/fish catch` seasonal progress so the next rank is calculated from the saved seasonal record instead of a reduced response object, preventing the current rank from being shown again as the next rank.


## [5.3.1] - 2026-06-14
### fix
- Maintenance cleanup patch: centralized shared feedback emojis, exposed the common emoji set from config, moved Fish rank embed colors into the shared color config, replaced repeated configuration status markers with common emoji constants, and kept the update behavior-neutral before the next role and verification features.


## [5.3.0] - 2026-06-14
### add
- Fish ranked seasons and autorole update: added lightweight monthly fishing seasons, added seasonal rank progression from Iron to Challenger based on monthly catches, best seasonal rarity and best seasonal score, colored fish catch/profile embeds by rank, added seasonal rank and next-rank hints to `/fish catch`, added a seasonal leaderboard to `/fish top`, kept total catches permanent while monthly ranks reset, reminded users about `/fish profile`, added a secured configurable arrival autorole in `/configuration`, blocked unsafe/high/managed autoroles, logged autorole assignment during member joins, exposed autorole status in `/pulse`, and documented the new seasonal fish storage.


## [5.2.0] - 2026-06-14
### improve
- Server log and Fish optimization update: simplified channel, role, member and user profile logs to avoid repeated identity blocks, removed duplicated channel/role names from log identities, ignored permission-only channel updates emitted immediately after channel creation, added more precise channel permission overwrite details, added optional audit-log responsible fields for channel, role and guild changes when Discord permissions allow it, documented the audit-log permission behavior, reduced `/fish catch` database reads by moving full leaderboard display back to `/fish top`, kept only the player's current weekly rank in catch results, throttled inactive fish cleanup per guild, added safer database-unavailable handling for fish records and rankings, and completed a command UX audit with no active duplicate command names found.


## [5.1.1] - 2026-06-13
### fix
- Database resilience patch: added safe handling for temporary Prisma/Neon connection failures, prevented AutoMod and member events from spamming full database errors, added a throttled database-unavailable logger, allowed log delivery to use cached guild settings when available, returned a clear temporary-unavailable message for commands that need the database, kept public help/community/botinfo commands usable during access checks, and cleaned the `/spark` help wording.


## [5.1.0] - 2026-06-13
### improve
- Pro logs, data retention and UX audit update: improved server/message/member/role/channel log readability with mentions, names and IDs while preventing unwanted log pings, centralized fish and optional moderation case retention cleanup, added periodic data retention checks on startup/runtime, clarified private-assistant help wording, added detailed `/help command` option/subcommand visibility, tightened `/pulse` versus `/spark` command descriptions, simplified configuration checklist status wording, refreshed privacy and maintenance documentation, and kept the command set audit focused on clarity instead of removing useful grouped commands.


## [5.0.0] - 2026-06-13
### add
- Private assistant direction update: repositioned Lumi as a limited private Discord assistant, changed the default capacity to 5 guilds, added a maximum guild member guard, introduced readable guild metadata with guild names, owner IDs, member counts, access status, trial expiration and last-seen timestamps, added code-based `/access` trials, added owner-only `/serveradmin` listing, approval and leave cleanup tools, blocked non-approved guilds from using normal commands during pending or expired access states, added feedback-channel notifications for private access requests, added delayed cleanup for pending guilds without activation, refreshed community, pulse, bot info, README and public data documentation, renamed the internal maintenance README to avoid confusion with the public README, added dynamic presence capacity text, and stored lightweight user/moderator tags on new moderation cases for better readable records.
