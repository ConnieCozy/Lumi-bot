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

Le panneau est divisé en trois onglets simples: **Général**, **Logs** et **AutoMod**. Choisis le réglage à modifier, puis recherche directement le rôle ou le salon dans la liste Discord. La valeur actuelle reste visible et peut être retirée avec le bouton prévu.

Lumi laisse volontairement les permissions Discord faire leur travail. Pour un serveur sécurisé, garde les salons sensibles invisibles au rôle non vérifié, puis ouvre-les au rôle vérifié ou membre.

## 2. Panneaux de modération et staff

`/moderation` rassemble les sanctions, les retraits, le casier et le slowmode. Le membre ciblé peut être recherché directement dans le panneau, sans relancer la commande.

`/staff` rassemble le statut, la communication, la gestion des membres et le nettoyage. Les sélections de salon, membre et rôle restent affichées pendant la session.

## 3. Vérification

Le système de vérification fonctionne avec un panneau.

Le membre n'a pas besoin de taper une commande:

1. Le staff publie le panneau avec `/verification`.
2. Le membre clique sur le bouton.
3. Lumi demande le petit captcha.
4. Lumi ajoute le rôle vérifié.
5. Lumi retire le rôle automatique d'arrivée si ce rôle est configuré.

Le reste du parcours dépend du serveur: règlement, rôle membre, salons visibles, ou autre système maison.

## 4. Tickets

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

## 5. Rôles à boutons

`/roles panel title:Mon panneau` ouvre un constructeur privé pendant dix minutes. Recherche jusqu'à dix rôles, utilise l'aperçu, puis publie. Cette préparation temporaire ne stocke rien dans la base de données.

Modes disponibles:

- `add`: le membre reçoit le rôle;
- `toggle`: le membre ajoute ou retire le rôle;
- `remove`: le membre retire uniquement le rôle.

Lumi refuse les rôles trop dangereux, au-dessus d'elle, gérés par une intégration ou contenant des permissions sensibles.

## 6. XP et niveaux

`/level profile` affiche le profil XP d'un membre.

`/level top` affiche le classement du serveur.

Le staff peut régler le système avec:

```text
/level settings enabled:true channel:#level-up
```

Les rangs Lumi sont visuels uniquement. Ils ne donnent pas de rôle Discord.

Un profil sans activité peut être supprimé automatiquement après la durée de conservation configurée, fixée à 180 jours par défaut.

## 7. Pêche numérique

`/fish catch` lance une pêche et affiche une carte courte : prise, rareté, poids, score, niveau du lieu et position hebdomadaire.

Les informations détaillées sont séparées pour garder les captures rapides à lire :

- `/fish profile` affiche la carte pêcheur et la progression de saison ;
- `/fish top` affiche les classements du serveur.

## 8. Jeux gratuits

Commande réservée au staff/admin serveur.

`/freegames show` affiche un aperçu privé rapide des jeux gratuits détectés sur Steam et Epic.

Le staff peut régler un salon dédié:

```text
/freegames settings enabled:true channel:#jeux-gratuits
```

Lumi utilise un cache pour éviter les appels inutiles et ne pas reposter la même liste.

`/freegames post` publie les annonces complètes dans le salon configuré, avec une carte par jeu quand une image est disponible.

## 9. Vocaux temporaires

Le staff peut activer un salon déclencheur avec:

```text
/voice setup create_channel:#Créer-un-vocal category:Vocaux max_active:5 enabled:true
```

Quand un membre rejoint ce salon, Lumi crée un vocal temporaire, le déplace dedans, puis supprime le vocal quand il devient vide.

Lumi publie automatiquement un panneau dans le chat du vocal. Le propriétaire et le staff peuvent y :

- renommer le vocal et régler le nombre de places ;
- choisir un mode ouvert, verrouillé ou privé ;
- autoriser une personne ou lui retirer l'accès ;
- transférer la propriété à une personne présente ;
- actualiser le panneau.

Les commandes restent disponibles comme solution de secours :

- `/voice rename` pour renommer son vocal;
- `/voice limit` pour régler le nombre de places;
- `/voice lock` pour fermer les nouvelles entrées;
- `/voice unlock` pour rouvrir;
- `/voice private` pour cacher le vocal aux personnes non autorisées;
- `/voice transfer` pour donner la gestion à une autre personne présente dans le vocal.
- `/voice panel` pour vérifier ou republier le panneau.

Le staff peut aussi utiliser ces actions si besoin. Lumi garde une limite de vocaux actifs pour éviter les abus et récupère les modes d'accès après un redémarrage.

## 10. Assistant local de Lumi

`/lumi ask question:comment ouvrir un ticket ?` aide à retrouver la commande adaptée avec une question simple.

Lumi cherche uniquement dans son catalogue local de commandes. La question n'est envoyée à aucun service externe et n'est pas enregistrée dans Neon. Elle propose jusqu'à trois chemins utiles avec leur utilisation et leur niveau d'accès, sans afficher les commandes réservées au développement.

Il est aussi possible de mentionner directement Lumi dans un message, par exemple `@Lumi comment ouvrir un ticket ?`. Elle répond aux salutations, aux remerciements et aux questions simples sur ses commandes. Ces messages ne sont pas stockés et un délai anti-spam limite les réponses répétées.

Le staff peut activer ou désactiver les réponses aux mentions depuis `/configuration` > **Général**.

## 11. Jeux légers

`/game game:LUMOT` lance **LUMOT**, le jeu de mots du flux. La première lettre est révélée et les couleurs indiquent les lettres bien placées, présentes ou absentes. Le mode peut être solo ou coopératif. Lumi choisit au hasard un mot de 5 à 8 lettres : il n'y a plus de difficulté à régler.

`/game game:Memory` lance une grille Memory personnelle équilibrée de 8 paires, sans difficulté à choisir.

`/game game:Trivia` lance cinq questions francophones auxquelles chaque membre peut répondre une fois. Les questions viennent de QuizzAPI.fr ; Lumi ne lui transmet aucun identifiant Discord, message personnel ou score.

Les parties et leurs scores restent uniquement en mémoire. Elles ne créent aucune ligne dans Neon et une seule partie peut être active par salon afin d'éviter le spam.

## 12. Rappels

`/reminder create` programme un rappel entre une minute et trente jours. Lumi accepte au maximum cinq rappels actifs par membre et par serveur.

`/reminder list` affiche uniquement tes rappels actifs et `/reminder cancel` en annule un grâce à son numéro.

Le rappel est envoyé dans le salon d'origine. Si ce salon n'est plus accessible, Lumi tente un message privé. Le texte, les IDs techniques et la date sont conservés temporairement dans Neon, puis supprimés dès le déclenchement ou l'annulation.

## 13. Sondages

`/poll` ouvre un formulaire réservé au staff ou aux membres qui peuvent gérer les messages. Il accepte entre deux et dix réponses, une durée de 1 heure à 32 jours et un choix simple ou multiple.

Le sondage utilise le système natif de Discord. Lumi ne stocke ni les réponses ni les votes dans Neon.

## 14. État de Lumi

La commande `/community` rassemble dans un seul message les liens officiels, l'invitation privée, la vitrine GitHub, les documents publics et l'état des systèmes. Un administrateur peut transmettre une question, un bug ou une demande d'accès avec `/feedback`.

La page publique [État de Lumi](https://lumi-bot-r4in.onrender.com/status) permet de vérifier séparément :

- le processus Render ;
- la connexion Discord Gateway ;
- la disponibilité de Neon.

Cette page n'affiche aucun identifiant de serveur, d'utilisateur ou secret.


