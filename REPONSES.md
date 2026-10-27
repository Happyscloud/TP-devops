# TP 1 - Réponses aux questions de réflexion

## Exercice 1.1 : Différence entre `git diff` et `git diff --staged`
`git diff` montre les modifications qui ne sont pas encore ajoutées avec `git add`.
`git diff --staged` montre les modifications qui ont déjà été ajoutées avec `git add` mais qui ne sont pas encore commitées.

## Exercice 1.2 : Différence entre `merge` et `rebase`
Avec `git merge`, l'historique garde une trace des deux branches et crée un commit de fusion.
Avec `git rebase`, l'historique devient linéaire (une ligne droite), comme si tout avait été fait à la suite.
On utilise `merge` pour des branches partagées, et `rebase` pour nettoyer une branche locale avant de la publier.

## Exercice 1.3 : Pourquoi utiliser une Pull Request ?
La PR permet de demander l'avis des autres avant de valider. On isole le code sur une branche, les autres peuvent le relire et commenter, puis on fusionne une fois que tout le monde est d'accord. Cela évite de casser la branche `main`.

## Exercice 1.4 : Pourquoi `git reset --hard` est-il dangereux ?
Parce qu'il efface définitivement les commits récents et les modifications non sauvegardées. Si on l'utilise sur un commit déjà poussé, on crée un historique divergent pour les autres membres de l'équipe. En équipe, on utilise plutôt `git revert` qui annule sans effacer.

## Exercice 1.5 : Pourquoi des dossiers séparés réduisent les conflits ?
Parce que Git gère les conflits fichier par fichier. Si chaque étudiant travaille dans son propre dossier, deux personnes ne modifient jamais le même fichier en même temps. Les fichiers s'ajoutent côte à côte sans se marcher sur les pieds.
