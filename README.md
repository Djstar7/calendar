# DJSTAR Calendar

Un calendrier léger en JavaScript vanilla qui affiche les mois de manière dynamique sans utiliser aucune fonction du JavaScript comme `Date()`.

## Aperçu

Ce calendrier est entièrement construit from scratch en utilisant uniquement :
- **CSS natif** pour le style (aucun framework)
- **JavaScript vanilla** avec manipulation du DOM
- **Structures de contrôle** (boucles, conditions)
- **Aucune fonction de date native** (`Date()` n'est pas utilisé)

## Comment ça marche

Le calendrier calcule tout manuellement :

- **Années bissextiles** déterminées avec l'algorithme standard : `(year % 4 === 0 && year % 100 !== 0) || (year % 400 === 0)`
- **Jours par mois** définis selon l'index du mois
- **Positionnement des jours** calculé de manière itérative pour déterminer le jour de la semaine où chaque mois commence

## Fonctionnalités

- Sélectionnez un **mois de départ** via un menu déroulant (Janvier à Décembre)
- Entrez le **nombre de mois** à afficher consécutivement
- Spécifiez une **année** pour afficher les calendriers jusqu'à cette année
- **Gestion du passage d'année** - gère automatiquement la transition d'une année à l'autre lors de l'affichage de plusieurs mois
- Interface utilisateur moderne avec thème sombre

## Utilisation

1. Ouvrez `calendar.html` dans un navigateur
2. Sélectionnez un mois de départ dans le menu déroulant
3. Entrez le nombre de mois que vous souhaitez afficher
4. Entrez l'année cible
5. Cliquez sur **Afficher** pour générer le calendrier

## Points techniques

| Aspect | Implémentation |
|--------|----------------|
| Gestion des dates | Calcul manuel (pas de `Date()`) |
| Style | CSS |
| DOM | Manipulation directe via `document.getElementById`, `createElement`, `appendChild` |
| Logique | Boucles itératives et structures conditionnelles |

## Passage d'année

Le calendrier gère correctement les transitions d'année. Lors de l'affichage de plusieurs mois qui s'étendent au-delà de décembre :
- Incrémente le compteur d'année
- Réinitialise l'index du mois à Janvier (0)
- Recalcule le statut bissextile pour la nouvelle année
- Continue l'affichage des mois de manière transparente

---

Créé par **DJSTAR**
