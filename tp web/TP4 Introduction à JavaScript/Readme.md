---

# Introduction à JavaScript — Évènements

Ce dépôt contient plusieurs projets réalisés en HTML et JavaScript, destinés à résoudre des problèmes variés en lien avec des applications interactives comme la permutation de valeurs, des calculatrices simples, des calculs d'IMC, et une calculatrice scientifique.

## Liste des exercices

1. **Exercice 1 : Permutation de valeurs**
2. **Exercice 2 : Calculatrice Simple**
3. **Exercice 3 : Calculateur d'IMC**
4. **Exercice 4 : Calculatrice Scientifique**

## Exercice 1 : Permutation de valeurs

### Description :
Ce projet consiste à permuter les valeurs de deux champs de texte (`v1` et `v2`) lorsque l'utilisateur clique sur le bouton "Permuter".

### Fonctionnalités :
- Permute les valeurs de deux champs de texte avec un simple bouton.

### Code JavaScript :
```javascript
function permuter() {
    var v1 = document.getElementById("v1");
    var v2 = document.getElementById("v2");

    var temp = v1.value;
    v1.value = v2.value;
    v2.value = temp;
}
```

### Exemple d'utilisation :
Avant de cliquer sur le bouton "Permuter" :
![image](https://github.com/user-attachments/assets/15769233-095c-4848-90ea-3f8a47e77338)

Après avoir cliqué sur le bouton "Permuter" :
![image](https://github.com/user-attachments/assets/8614e8f4-7f38-4702-83b4-10624d7740f1)

## Exercice 2 : Calculatrice Simple

### Description :
Une calculatrice basique qui permet à l'utilisateur d'entrer deux valeurs numériques et de choisir une opération (addition, soustraction, division, multiplication).

### Fonctionnalités :
- Addition
- Soustraction
- Division (avec gestion d'erreur en cas de division par zéro)
- Multiplication

### Code JavaScript :
```javascript
function additionner() {
    var v1 = parseFloat(document.getElementById("v1").value);
    var v2 = parseFloat(document.getElementById("v2").value);
    document.getElementById("resultat").value = v1 + v2;
}

function soustraction() {
    var v1 = parseFloat(document.getElementById("v1").value);
    var v2 = parseFloat(document.getElementById("v2").value);
    document.getElementById("resultat").value = v1 - v2;
}

function division() {
    var v1 = parseFloat(document.getElementById("v1").value);
    var v2 = parseFloat(document.getElementById("v2").value);
    if (v2 === 0) {
        alert("Erreur : Division par zéro !");
        document.getElementById("resultat").value = "";
    } else {
        document.getElementById("resultat").value = v1 / v2;
    }
}

function multiplication() {
    var v1 = parseFloat(document.getElementById("v1").value);
    var v2 = parseFloat(document.getElementById("v2").value);
    document.getElementById("resultat").value = v1 * v2;
}
```

### Exemple d'utilisation :
![image](https://github.com/user-attachments/assets/0c74aa43-c529-409e-92ff-2fb5fede911a)

## Exercice 3 : Calculateur d'IMC

### Description :
Un calculateur d'IMC (Indice de Masse Corporelle) qui permet à l'utilisateur d'entrer son poids (en kg) et sa taille (en m), puis affiche son IMC et une interprétation du résultat.

### Fonctionnalités :
- Calcul de l'IMC en fonction du poids et de la taille.
- Affichage d'un message interprétant le résultat.

### Code JavaScript :
```javascript
function calculerIMC() {
    var poids = parseFloat(document.getElementById("poids").value);
    var taille = parseFloat(document.getElementById("taille").value);
    var imc = (poids / (taille * taille));
    var message = "";

    if (imc < 18.5) {
        message = "Vous êtes en insuffisance pondérale (maigreur).";
    } else if (imc >= 18.5 && imc < 25) {
        message = "Votre IMC est normal.";
    } else if (imc >= 25 && imc < 30) {
        message = "Vous êtes en surpoids.";
    } else if (imc >= 30 && imc < 35) {
        message = "Vous êtes en obésité modérée.";
    } else if (imc >= 35 && imc < 40) {
        message = "Vous êtes en obésité sévère.";
    } else {
        message = "Vous êtes en obésité morbide ou massive.";
    }

    document.getElementById("resultat").innerHTML = `Votre IMC est de <b>${imc}</b>. ${message}`;
}
```

### Exemple d'utilisation :
Avant de remplir les champs :
![image](https://github.com/user-attachments/assets/49967199-519f-4e0a-ad2a-49db967f8fbe)

Après avoir rempli les champs :
![image](https://github.com/user-attachments/assets/6f63f669-5d58-438f-94ef-6a8cf99e106f)

## Exercice 4 : Calculatrice Scientifique

### Description :
Une calculatrice scientifique qui permet de réaliser des calculs plus avancés (fonctions trigonométriques, logarithmes, racines carrées, etc.), avec un affichage de type "grid" pour les boutons et un affichage propre.

### Fonctionnalités :
- Calculs trigonométriques : sin, cos, tan
- Calculs logarithmiques : ln, log
- Calculs mathématiques avancés : π, e, x², exponentielle, etc.

### Code JavaScript :
```<script>
        let inverseMode = false;

        function appendToDisplay(value) {
            document.getElementById('display').value += value;
        }

        function clearDisplay() {
            document.getElementById('display').value = '';
        }

        function calculate() {
            try {
                let expression = document.getElementById('display').value;

                // Remplacer les fonctions trigonométriques et logarithmiques par les versions JavaScript
                expression = expression.replace(/sin\(/g, 'sin(');
                expression = expression.replace(/cos\(/g, 'cos(');
                expression = expression.replace(/tan\(/g, 'tan(');
                expression = expression.replace(/log\(/g, 'log10(');
                expression = expression.replace(/ln\(/g, 'log(');
                expression = expression.replace(/√/g, 'Math.sqrt(');
                
                // Calculer l'expression
                console.log(expression)
                let result = eval(expression);
                document.getElementById('display').value = result;
            } catch (error) {
                document.getElementById('display').value = 'Erreur';
            }
        }

        function toggleInverse() {
            inverseMode = !inverseMode;
            if (inverseMode) {
                document.querySelector('button[onclick="appendToDisplay(\'Math.sin(\')"]').innerText = "sin⁻¹";
                document.querySelector('button[onclick="appendToDisplay(\'Math.cos(\')"]').innerText = "cos⁻¹";
                document.querySelector('button[onclick="appendToDisplay(\'Math.tan(\')"]').innerText = "tan⁻¹";
            } else {
                document.querySelector('button[onclick="appendToDisplay(\'Math.sin(\')"]').innerText = "sin";
                document.querySelector('button[onclick="appendToDisplay(\'Math.cos(\')"]').innerText = "cos";
                document.querySelector('button[onclick="appendToDisplay(\'Math.tan(\')"]').innerText = "tan";
            }
        }
    </script>
```

### Exemple d'utilisation :
Voici un aperçu de la calculatrice :
![image](https://github.com/user-attachments/assets/5e017cc9-b64c-4654-97b9-a8396c49b530)

Exemple de calcul avec ln(5) :
![image](https://github.com/user-attachments/assets/5107f403-8fff-48b5-b4ea-559abd9456d6)
![image](https://github.com/user-attachments/assets/47f0c110-38a1-4316-9111-357174700231)

## Technologies utilisées

- **HTML5** pour la structure de la page.
- **CSS** pour le style et la mise en page.
- **JavaScript** pour la logique de calcul et les interactions.

## Conclusion

Ce dépôt présente une série d'exercices en HTML et JavaScript permettant de réaliser diverses applications interactives et utiles. Chaque projet met en avant une fonctionnalité spécifique, allant des calculatrices simples aux calculs scientifiques plus complexes. Ces exercices sont conçus pour renforcer les compétences en programmation web et à comprendre les bases de la manipulation des événements en JavaScript.

En travaillant sur ces projets, vous avez l'occasion de développer une meilleure compréhension des interactions utilisateur, de la gestion des événements, et de la logique de programmation dynamique pour créer des applications réactives et efficaces. Ces concepts sont essentiels pour toute personne souhaitant approfondir ses connaissances en développement web.

Merci d'avoir exploré ce dépôt et n'hésitez pas à adapter ces exercices à vos besoins ou à les étendre pour de nouveaux défis !

---
