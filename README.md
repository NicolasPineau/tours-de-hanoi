# Les Tours de Hanoï

Un TP de JavaScript dans la lignée du [Passeur](https://github.com/NicolasPineau/le-passeur).

Le jeu des Tours de Hanoï est cassé. L'élève le répare mission par mission, directement dans la page : chaque correction débloque une fonctionnalité du jeu, et le moine du temple commente ses progrès.

## Utilisation

- **Élèves** : ouvrir la page publiée sur GitHub Pages. Rien à installer. Le travail est enregistré dans le navigateur, on peut donc finir à la maison sur le même appareil.
- **Rendu** : en bas de la page, l'élève écrit son nom et clique sur « Code pour l'enseignant ». Il envoie ce code (qui commence par `TH1-`) par mail.
- **Enseignant** : ouvrir la page avec `#prof` à la fin de l'adresse, coller les codes reçus (un par ligne) et cliquer sur « Vérifier ». On obtient un tableau avec, pour chaque élève, les points, les missions, les jokers et les dates. Un score modifié à la main est signalé.

## Les missions

| # | Mission | Type | Notion |
|---|---|---|---|
| 1 | Les disques invisibles | 🧩 code à écrire | Classes, constructeur, `this` |
| 2 | Le sommet introuvable | 🧩 | Getter |
| 3 | Le moine distrait | 🐞 bug | `this` dans une méthode |
| 4 | La tour sans fond | 🐞 | Tableaux : `pop` / `shift` |
| 5 | Le sacrilège | 🐞 | Conditions |
| 6 | Le disque volé | 🧩 | `reduce` (somme) |
| 7 | La prophétie | 🧩 | Conditions, `**` (2ⁿ − 1) |
| 8 | Le grand livre | 🐞 | `map` / `forEach` |
| 9 | Les statistiques du moine | 🧩 | `reduce` vers un objet |
| ⭐ | Le moine automatique (bonus) | 🧩 | Récursivité |

**Barème :**
- **+100 points** par mission réussie, mission bonus comprise.
- **Pour chaque mission**, un indice gratuit et un **joker** plus précis qui coûte **40 points**. Il y a 4 jokers pour tout le jeu.
- **La barre de progression** compte les 9 missions ; la mission bonus apparaît en plus (⭐).

**Dernier défi**, une fois le jeu réparé : finir l'énigme avec 4 disques en 15 coups.

## Technique

- **Une seule page** (`index.html`), entièrement statique.
- **L'éditeur** : CodeMirror. Les boucles infinies sont stoppées grâce à l'analyse du code par acorn.
- **Le jeu** tourne dans un cadre isolé. Un second cadre, invisible, vérifie chaque mission avec des tests automatiques.
- **Le moteur** (éditeur, console, tests, indices, jokers, score chiffré, code enseignant) est celui du Passeur. Seuls le jeu, les missions et les tests changent.
