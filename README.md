# Révision AM11 · MEF en mouvement

Outil de révision interactif pour AM11 (méthode des éléments finis) : barre 1D, treillis 2D/3D, poutre 2D, formulaire, et entraînement sur les TD et médians avec corrections.

Ouvrir `index.html` dans un navigateur, ou utiliser la version en ligne (GitHub Pages) : <https://phi1ow.github.io/revision/>. Le pendant AM08 (fluides) est ici : <https://phi1ow.github.io/revision-am08/>.

## Ce que la page sait faire

- **Labos animés** : chaque étape de la recette (mailler, approcher, élément, tourner, assembler, bloquer, résoudre, exploiter) a une animation dont tu changes les paramètres. Les solveurs retrouvent les valeurs des diapos.
- **Entraînement** : les 4 TD et les médians A24 et A25, avec figure, déformée recalculée et correction à dévoiler question par question.
- **Progression** : sous chaque correction, marque la question *Acquis* ou *À revoir*. Le panneau en tête de la partie E montre la barre d'avancement, filtre ce qui reste, et retrouve le dernier exercice travaillé.
- **Cartes mémoire** (fin du formulaire) : formules, pièges et gestes de la méthode deviennent des cartes à répétition espacée (4 boîtes : une carte ratée revient tout de suite, une carte sue revient dans 1, 3 puis 7 jours). Le paquet *Exercices* ajoute toutes les questions des TD et médians.
- **Chrono d'examen** (icône ⏱ dans la barre) : médian de 2 h, ou une durée au choix ; le temps restant s'affiche dans la barre et dans l'onglet, la page sonne à la fin, et le chrono survit à un rechargement.
- **Recherche** (loupe, `/` ou `Ctrl+K`) : chapitres, labos, formules, pièges, exercices et questions ; la cible s'ouvre et se surligne.
- **Thème** clair / sombre (icône lune / soleil, ou touche `t`), mémorisé.
- **Impression** : le bouton *Imprimer le formulaire* sort formules et pièges seuls sur une à deux pages A4 ; `Ctrl+P` imprime toute la page avec les corrections dépliées.
- **Liens profonds** : chaque question a une ancre (`#ex-td2-q3` par exemple), utile pour retrouver un point précis.

## Raccourcis clavier

| Touche | Action |
| --- | --- |
| `/` ou `Ctrl+K` | Rechercher |
| `t` | Changer de thème |
| `Espace` | Retourner la carte affichée |
| `→` / `←` | Carte sue / carte à revoir |
| `Échap` | Fermer la fenêtre ouverte |

## Données

Progression, cartes, thème et chrono sont enregistrés dans le `localStorage` du navigateur (clés préfixées `am11:`). Rien ne quitte ta machine ; un autre navigateur ou une fenêtre privée repart de zéro. Les boutons *Réinitialiser* du panneau de progression et des cartes effacent ces données.

## Structure

Un seul fichier, `index.html` : styles, contenu, solveurs et animations. Le « kit de révision » (progression, cartes, chrono, recherche, impression) est un bloc CSS et un script indépendants ajoutés à la fin du fichier ; il lit la page telle qu'elle est, donc ajouter un exercice ou un piège suffit pour qu'il apparaisse dans la recherche, la progression et les cartes.
