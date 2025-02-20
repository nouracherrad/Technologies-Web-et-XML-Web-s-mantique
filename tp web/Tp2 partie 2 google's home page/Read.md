# Projet : Clone de la page d'accueil de Google

## Description
Ce projet est une reproduction simplifiée de la page d'accueil de Google en utilisant uniquement HTML et CSS. L'objectif est de recréer l'apparence générale de la page tout en pratiquant la mise en page avec Flexbox et d'autres techniques CSS.

## Structure du Code

### 1. **HTML**
Le fichier HTML est structuré comme suit :

- **`<head>`** : Contient les métadonnées, l'encodage des caractères et le titre de la page.
- **`<body>`** : Organisé en plusieurs sections principales :
  
  - **Barre de navigation supérieure (`div1`)** : Contient des liens vers Gmail et Google Images, ainsi qu'un icône de menu et un avatar utilisateur simulé.
  - **Logo Google (`div2`)** : Affiche le logo Google centré en haut de la page.
  - **Barre de recherche (`div3`)** : Inclut un champ de saisie de texte et des icônes représentant la recherche vocale et par image.
  - **Section de personnalisation (`div4`)** : Contient un bouton permettant de personnaliser l'expérience Chrome.

### 2. **CSS**
Le style est appliqué directement dans une balise `<style>` dans le `<head>` du document. Voici les principales règles utilisées :

- **Flexbox** : Utilisé pour aligner les éléments horizontalement et centrer certains blocs.
- **Styles de la barre de navigation (`#div1`)** :
  - Alignement des éléments à droite avec `justify-content: flex-end`.
  - Espacement entre les liens avec `gap: 15px`.
  - Style pour l'icône du compte (`#compte`) avec un fond noir et une bordure arrondie.
- **Positionnement du logo Google (`#div2`)** :
  - Marges pour centrer verticalement et horizontalement l'image du logo.
- **Barre de recherche (`.search-bar`)** :
  - Largeur de 600px, arrondie avec `border-radius: 30px`.
  - Ajout d'une ombre pour un effet visuel similaire à Google.
  - Icônes cliquables de recherche, microphone et caméra positionnées à l'intérieur de la barre.
- **Bouton de personnalisation (`div4 button`)** :
  - Largeur de 200px, arrondie avec une couleur de fond blanche et un effet de survol qui change la couleur d'arrière-plan.

## Résultat Visuel
![image](https://github.com/user-attachments/assets/ef9e727b-56f7-4e1e-a17b-b0ad3158f0e3)



