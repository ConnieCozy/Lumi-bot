# Lumi data requests

Ce document décrit comment traiter une demande liée aux données stockées par Lumi.

Il sert de procédure publique simple pour les administrateurs de serveurs et de note interne pour l'équipe Lumi. Il ne remplace pas un conseil juridique.

## Données concernées

Lumi stocke seulement les données nécessaires au fonctionnement du bot :

- configuration serveur : nom du serveur, owner ID, nombre de membres, statut d'accès privé, salons de logs, salon bienvenue, salon départ, rôle modération, réglages AutoMod ;
- cas de modération : serveur, utilisateur concerné, modérateur, type d'action, raison, durée éventuelle, date ;
- records de pêche : meilleur score permanent, meilleur score hebdomadaire, résultat de la semaine précédente, meilleure capture, rareté, poids et compteurs légers par joueur et par serveur ;
- tickets ouverts : serveur, salon ticket, utilisateur ayant ouvert le ticket, type, résumé court, statut, staff ayant pris en charge, ID du message de suivi staff et date de création. Les tickets fermés sont supprimés de la base de données, avec résumé Discord optionnel si un salon de suivi ticket est configuré ;
- profils XP/Level : serveur, utilisateur, XP total, niveau, messages comptés et dernier gain XP ;
- cache jeux gratuits : dernière signature Steam/Epic postée par serveur pour éviter les doublons ;
- vocaux temporaires actifs : serveur, salon vocal temporaire, propriétaire, message du panneau, mode d'accès, permissions à restaurer, accès individuels et dates techniques tant que le salon existe.
- rappels actifs : serveur, salon d'origine, utilisateur, texte et date prévue, avec cinq rappels maximum par membre et par serveur et trente jours maximum.

Quand Lumi quitte ou est retirée d'un serveur, les données liées à ce serveur sont supprimées automatiquement de la base de données de Lumi.

Quand un membre quitte un serveur, Lumi supprime automatiquement ses données XP/Level, ses records de pêche et ses rappels liés à ce serveur. Les cas de modération restent liés au serveur afin de préserver l'historique staff.

Les profils XP/Level sans activité peuvent également être supprimés automatiquement après 180 jours afin de limiter la conservation de lignes inactives.

Les records de pêche permanents restent conservés tant que le membre reste sur le serveur. Ils ne sont plus supprimés pour simple inactivité.

Les vocaux temporaires ne contiennent pas d'audio ni d'historique de conversation. Les informations de panneau et de permissions sont supprimées de la base avec le salon temporaire.

Les questions adressées à Lumi par `/lumi ask` ou par mention directe ne sont pas enregistrées dans la base de données. Les questions et scores du Trivia restent aussi en mémoire et ne sont pas enregistrés dans Neon.

## Qui peut faire une demande

Pour les données liées à un serveur, la demande doit venir d'un propriétaire ou administrateur du serveur concerné.

Cela évite qu'un utilisateur isolé puisse demander la suppression ou la consultation de données de modération d'un serveur sans contexte, par exemple pour masquer un abus réel.

Une demande individuelle liée à des droits légaux sur des données personnelles peut être examinée séparément. Lumi peut demander des éléments de vérification raisonnables avant de répondre.

## Preuves demandées

Pour une demande serveur, l'administrateur doit fournir :

- l'ID du serveur ;
- une capture de `/serverinfo` montrant le serveur concerné ;
- son ID utilisateur Discord ;
- une capture de son profil Discord ;
- une preuve qu'il possède une permission administrateur ou qu'il est propriétaire du serveur ;
- le type de demande : consultation, correction, suppression, vérification d'un cas.

Pour vérifier un cas de modération précis, ajouter si possible :

- l'ID de l'utilisateur concerné ;
- la date ou période approximative ;
- le type d'action : warn, mute, kick, ban, unban, automod ;
- la raison affichée si elle est connue ;
- tout contexte utile pour repérer le cas.

## Réponses possibles

Selon la demande, l'équipe Lumi peut :

- confirmer qu'aucune donnée liée au serveur n'a été trouvée ;
- fournir un résumé des données serveur pertinentes ;
- vérifier un cas de modération précis ;
- corriger une donnée manifestement incorrecte ;
- supprimer ou anonymiser une donnée qui n'est plus nécessaire ;
- refuser ou limiter une demande abusive, impossible à vérifier, ou qui mettrait en danger la sécurité/modération d'un serveur.

## Données qui ne sont pas fournies

Lumi ne fournit pas :

- les tokens, secrets, variables d'environnement ou informations d'infrastructure ;
- les données d'autres serveurs ;
- les données de modération d'un serveur à une personne qui ne peut pas prouver son autorité sur ce serveur ;
- des exports massifs inutiles quand une vérification ciblée suffit.

## Canal recommandé

Un propriétaire ou administrateur du serveur concerné commence la demande avec `/feedback` en indiquant seulement sa nature. La commande transmet déjà l'identité Discord de l'administrateur et du serveur à l'équipe Lumi.

Les captures, IDs complémentaires et autres preuves sensibles ne doivent pas être placés dans le texte de `/feedback` ni publiés dans un salon public. L'équipe Lumi contacte ensuite l'administrateur de manière privée pour vérifier les éléments et assurer le suivi.
i.





