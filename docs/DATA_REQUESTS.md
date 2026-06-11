# Lumi data requests

Ce document décrit comment traiter une demande liée aux données stockées par Lumi.

Il sert de procédure publique simple pour les administrateurs de serveurs et de note interne pour l'équipe Lumi. Il ne remplace pas un conseil juridique.

## Données concernées

Lumi stocke seulement les données nécessaires au fonctionnement du bot :

- configuration serveur : salons de logs, salon bienvenue, salon départ, rôle modération, réglages AutoMod ;
- cas de modération : serveur, utilisateur concerné, modérateur, type d'action, raison, durée éventuelle, date ;
- records de pêche : meilleur score par joueur et par serveur, meilleure capture, rareté, spot et compteur total de captures ;
- aucune donnée XP, économie ou profil social permanent n'est prévue dans la version actuelle.

Quand Lumi quitte ou est retirée d'un serveur, les données liées à ce serveur sont supprimées automatiquement de la base de données de Lumi.

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

Les demandes liées aux données doivent être faites sur le serveur support Lumi afin que l'équipe puisse vérifier les preuves, poser des questions si nécessaire et répondre correctement.

La commande `/feedback` sert uniquement à transmettre une suggestion, un bug ou un retour court. Elle ne permet pas d'assurer un suivi ni de répondre directement à une demande de données.

Pour une demande sensible, éviter de publier des IDs et captures dans un salon public.
