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
