# Guide utilisateur Lumi

Ce guide sert de base simple pour configurer et utiliser Lumi sur un serveur.

## 1. Configuration de base

Utilise `/configuration` pour régler les éléments importants du serveur:

- salons de logs;
- AutoMod et anti-raid;
- rôles de modération;
- rôle automatique d'arrivée;
- rôle vérifié;
- messages de bienvenue et de départ.

Lumi laisse volontairement les permissions Discord faire leur travail. Pour un serveur sécurisé, garde les salons sensibles invisibles au rôle non vérifié, puis ouvre-les au rôle vérifié ou membre.

## 2. Vérification

Le système de vérification fonctionne avec un panneau.

Le membre n'a pas besoin de taper une commande:

1. Le staff publie le panneau avec `/verification`.
2. Le membre clique sur le bouton.
3. Lumi demande le petit captcha.
4. Lumi ajoute le rôle vérifié.
5. Lumi retire le rôle automatique d'arrivée si ce rôle est configuré.

Le reste du parcours dépend du serveur: règlement, rôle membre, salons visibles, ou autre système maison.

## 3. Tickets

Le staff publie un panneau avec `/ticket panel`.

Quand un membre ouvre un ticket:

1. il clique sur le bouton;
2. il choisit le type de demande;
3. il écrit un résumé court;
4. Lumi crée un salon privé;
5. le membre attend que le staff prenne en charge.

Le membre ne peut pas écrire dans le ticket tant qu'un staff n'a pas cliqué sur `Prendre en charge`.

Le staff peut ensuite:

- prendre en charge;
- marquer résolu;
- fermer le ticket.

Le salon de logs ticket affiche une fiche de suivi unique côté staff. Lumi la met à jour au lieu d'empiler plusieurs archives.

À la fermeture, le staff doit indiquer une raison. Lumi passe la fiche de suivi en fermé, puis supprime la donnée temporaire du ticket.

## 4. Rôles à boutons

`/roles panel` permet de créer des panneaux de rôles.

Modes disponibles:

- `add`: le membre reçoit le rôle;
- `toggle`: le membre ajoute ou retire le rôle;
- `remove`: le membre retire uniquement le rôle.

Lumi refuse les rôles trop dangereux, au-dessus d'elle, gérés par une intégration ou contenant des permissions sensibles.

## 5. XP et niveaux

`/level profile` affiche le profil XP d'un membre.

`/level top` affiche le classement du serveur.

Le staff peut régler le système avec:

```text
/level settings enabled:true channel:#level-up
```

Les rangs Lumi sont visuels uniquement. Ils ne donnent pas de rôle Discord.

## 6. Jeux gratuits

Commande réservée au staff/admin serveur.

`/freegames show` affiche un aperçu privé rapide des jeux gratuits détectés sur Steam et Epic.

Le staff peut régler un salon dédié:

```text
/freegames settings enabled:true channel:#jeux-gratuits
```

Lumi utilise un cache pour éviter les appels inutiles et ne pas reposter la même liste.

`/freegames post` publie les annonces complètes dans le salon configuré, avec une carte par jeu quand une image est disponible.

## 7. Vocaux temporaires

Le staff peut activer un salon déclencheur avec:

```text
/voice setup create_channel:#Créer-un-vocal category:Vocaux max_active:5 enabled:true
```

Quand un membre rejoint ce salon, Lumi crée un vocal temporaire, le déplace dedans, puis supprime le vocal quand il devient vide.

Le propriétaire du vocal peut utiliser:

- `/voice rename` pour renommer son vocal;
- `/voice limit` pour régler le nombre de places;
- `/voice lock` pour fermer les nouvelles entrées;
- `/voice unlock` pour rouvrir;
- `/voice transfer` pour donner la gestion à une autre personne présente dans le vocal.

Le staff peut aussi utiliser ces actions si besoin. Lumi garde une limite de vocaux actifs pour éviter les abus.
