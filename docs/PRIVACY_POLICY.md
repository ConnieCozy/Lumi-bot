# Lumi privacy policy

Dernière mise à jour : 2026-08-24

Cette politique explique quelles données Lumi peut utiliser pour fonctionner sur Discord.

Lumi est un bot Discord francophone créé par **ConnieCozy** avec **HexBoon Development**.

## Données utilisées

Lumi peut traiter les données suivantes :

- IDs de serveurs Discord ;
- noms de serveurs, owner ID, nombre approximatif de membres, statut d'accès privé et date d'expiration éventuelle ;
- IDs de salons configurés ;
- IDs de rôles configurés, dont les rôles d'arrivée, de vérification et de panneaux de rôles ;
- IDs d'utilisateurs concernés par une action de modération ;
- IDs de modérateurs ayant effectué une action ;
- raisons, types, durées et dates des cas de modération ;
- réglages AutoMod, logs, bienvenue, départ et configuration serveur ;
- records de pêche : serveur, utilisateur, meilleur score permanent, meilleur score hebdomadaire, résultat de la semaine précédente, score de saison mensuelle, meilleure capture, rareté, poids et compteurs de captures ;
- données XP/Level : serveur, utilisateur, XP total, niveau, nombre de messages comptés et date du dernier gain XP ;
- données temporaires de tickets ouverts : serveur, salon ticket, utilisateur ayant ouvert le ticket, type, résumé court, statut, staff ayant pris en charge, ID du message de suivi staff et date de création ;
- état minimal des jeux gratuits : dernière liste Steam/Epic déjà postée par serveur afin d'éviter les doublons ;
- données temporaires de vocaux privés : serveur, salon vocal temporaire, propriétaire du salon et dates techniques tant que le salon existe ;
- contenu transmis volontairement via une commande de feedback.

Lumi ne stocke pas d'économie, d'inventaire social permanent, de contenu audio ou de dates d'anniversaire.

## Pourquoi ces données sont utilisées

Ces données servent à :

- faire fonctionner la configuration de chaque serveur ;
- gérer l'accès privé, les essais limités et la capacité de Lumi ;
- appliquer les outils de modération ;
- conserver un historique de modération utile au staff ;
- envoyer les logs configurés par le serveur ;
- attribuer un rôle automatique d'arrivée quand un serveur le configure ;
- gérer le parcours de vérification serveur : rôle non vérifié, validation Lumi, rôle vérifié puis rôle membre si le serveur utilise un bouton de règlement ;
- protéger les serveurs contre certains abus comme spam, raid ou messages répétés ;
- afficher le record personnel, le rank saisonnier mensuel et les Top 3 serveur de la commande `/fish` ;
- afficher les profils XP/Level, le classement serveur et les annonces de passage de niveau ;
- créer, suivre et fermer des tickets privés entre un membre et le staff du serveur ;
- afficher ou poster les jeux gratuits Steam/Epic dans un salon configuré ;
- créer et nettoyer des salons vocaux temporaires configurés par le staff ;
- recevoir des retours d'administrateurs via `/feedback`.

## Logs Discord

Les logs envoyés dans les salons Discord configurés restent dans le serveur Discord concerné.

Les administrateurs du serveur sont responsables de la visibilité, des permissions et de la conservation de ces salons.

## Partage des données

Les données ne sont pas vendues.

Elles peuvent être traitées par les services techniques nécessaires au fonctionnement de Lumi, comme Discord, Render, Neon ou GitHub, selon leur rôle respectif.

## Conservation

Les données de configuration sont conservées tant que Lumi est utilisée sur le serveur.

Les cas de modération sont conservés tant que Lumi est présente sur le serveur afin de permettre au staff de vérifier l'historique et les abus.

Une durée de conservation automatique peut être configurée pour les cas de modération si le serveur souhaite limiter l'historique stocké. Par défaut, Lumi ne purge pas automatiquement ces cas.

Les records de pêche ne conservent pas l'historique de chaque pêche. Lumi garde seulement une ligne par joueur et par serveur avec le meilleur score permanent, le meilleur score de la semaine, le résultat de la semaine précédente, le meilleur score de saison mensuelle et des compteurs légers.

Les records de pêche inactifs peuvent être supprimés automatiquement après une courte période de conservation afin de limiter l'espace utilisé sur la base de données. La durée recommandée pendant la phase premium privée est de 14 jours.

Les profils XP/Level gardent une ligne légère par joueur et par serveur. Lumi ne compte que les messages texte éligibles avec un cooldown anti-spam. Les salons tickets temporaires et le vocal ne donnent pas d'XP. Quand un membre quitte un serveur, sa ligne XP/Level et ses records de pêche du serveur sont supprimés automatiquement.

Les panneaux de rôles à boutons ne stockent pas l'état de chaque membre dans la base de données. Lumi applique le rôle au moment du clic et Discord conserve ensuite l'état réel du membre.

Les tickets ne stockent pas les messages dans la base de données. Lumi garde seulement une ligne temporaire pendant que le ticket est ouvert: type, résumé court, statut, prise en charge staff et ID du message de suivi staff. Quand le ticket est fermé, cette ligne est supprimée. Si un salon de suivi ticket est configuré, le message Discord final reste dans le serveur et sa conservation dépend alors des réglages du serveur Discord concerné.

Les jeux gratuits Steam/Epic ne stockent pas d'historique complet. Lumi conserve seulement la dernière signature postée par serveur pour éviter de republier la même liste.

Les vocaux temporaires ne stockent aucun contenu audio. Lumi conserve seulement la ligne technique du vocal actif afin de savoir quel salon supprimer quand il devient vide. Quand le vocal est supprimé, la ligne est supprimée aussi.

Lumi ne stocke pas les dates d'anniversaire des membres. Le module anniversaire est volontairement écarté pour éviter d'ajouter des données personnelles non nécessaires.

Quand Lumi quitte ou est retirée d'un serveur, les données liées à ce serveur sont supprimées automatiquement de la base de données de Lumi. Cela inclut la configuration serveur, les cas de modération associés, les records de pêche du serveur, les profils XP/Level, les tickets encore ouverts, les vocaux temporaires encore suivis et l'état de publication des jeux gratuits.

Une demande de vérification, correction, suppression ou anonymisation peut aussi être faite selon la procédure dédiée.

## Demandes d'accès ou suppression

Les demandes liées aux données doivent suivre la procédure décrite ici :

[DATA_REQUESTS.md](DATA_REQUESTS.md)

Les demandes serveur doivent être faites par un propriétaire ou administrateur vérifié du serveur concerné.

Une demande individuelle liée à des droits légaux sur des données personnelles peut être examinée séparément avec des éléments de vérification raisonnables.

## Sécurité

Les tokens, secrets, variables d'environnement et informations d'infrastructure ne sont jamais publiés volontairement.

Le code public de Lumi sert uniquement de vitrine et ne doit pas contenir de secrets.

## Contact

Pour une question ou une demande, utilisez le serveur support Lumi :

https://discord.gg/wJ8xjWJ2Nd





