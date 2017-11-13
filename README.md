# TP5
## Introduction
Vous le savez peut-être, un programme Java est composé de classes qui sont chargées dynamiquement lorsqu'elles sont nécessaires. Certaines classes proviennent de votre disque local, d'autres proviennent peut-être du réseau (applet, etc...), certaines sont chargées automatiquement, d'autres peuvent l'être "à la demande".
Attention, les questions sur le chargement des classes sont à réaliser :
soit hors d'Eclipse (ligne de commandes)
soit dans Eclipse mais en désactivant le "build automatique"
pour mieux maitriser la compilation des classes et le déplacement des fichiers .class nécessaires aux expérimentations.


## Les classes ne sont pas toutes chargées en même temps : vérifions !
Avant tout, testons quelques exemples qui prouvent que toutes les classes utilisées par une appli Java ne sont pas chargées en mémoire avant que l'appli ne démarre.
• Récupèrez donc les exemples de chargement dans cette archive.
• Etudiez les classes A.java, B.java, C.java, D.java. Elles comportent toutes un bloc static qui affiche un message dès que la classe est chargée en mémoire. Compilez toutes les classes. Exécutez Exemple1.
• Observez bien les chargements de chaque classe, et ce qui provoque ces chargements.
• Remarquez (ClasseB n'est jamais chargée) que déclarer une variable d'un certain type ne suffit pas pour déclencher le chargement de ce type (classe ou interface). Les classes ne sont chargées qu'au moment où on en a vraiment besoin (chargement de ClasseD après les 5 secondes d'attentes). On appelle ça le "lazy loading" (chargement paresseux).
• Remarque : pour des classes quelconques (sans bloc static comme celui de des classes A, B, C et D) on peut s'aider de l'option -verbose de la commande java pour observer les classes qui sont chargées.