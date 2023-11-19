 <h1 style="text-align:center";>
  Activité d'informatique sans ordinateur : <br>Trier des poids <br>(adaptable à partir du CM2)
</h1>

<p style="text-align:center;" > <b>version classique</b> </p>

Un ordinateur doit souvent ordonner des éléments afin que ceux-ci puissent être accessibles de façon simple et rapide.
En informatique, cette notion est appelé le tri.
Il existe différents types de tri, plus ou moins efficaces selon la situation.

Cette activité a pour but d'initier les élèves à la notion de **tri** (au sens informatique du terme), puis de leur montrer que certaines méthodes sont plus efficaces (= plus rapides) que d'autres.
<br>On pourra également aborder brièvement la notion de **récursivité**.

## Partie 1 - Description de l'activité

### Préparation


**Matériel** :
- 10 pots par groupe avec chacun (chaque pot) une quantité d'eau différente
- Une balance par groupe

**Organisation** :
- Diviser la classe en groupes
- Distribuer le matériel nécessaire et une copie des consignes (cf. partie Déroulement ci-dessous)
- Laisser les élèves en autonomie puis discuter des résultats

**Objectif** :
- Déterminer la méthode de tri la plus efficace pour ordonner des objets selon leur poids.

### Déroulement

#### Approche autonome

1. Trouve le pot le plus léger. *Attention* : tu dois comparer les poids des pots en utilisant **uniquement** la balance. Tu ne peux comparer que deux pots à la fois.
Comment as-tu fait ? As-tu une idée plus simple pour y arriver ?

2. Trie 4 pots du plus léger au plus lourd.
Combien de comparaisons as-tu eues besoin de faire ? Pourrais-tu en faire moins ? Si oui, comment ?

3. Même question, maintenant avec tous les pots. Appelle le ou la professeur pour qu'il vérifie. <br>**Bonus** : Tu peux aussi vérifier
par toi-même, comment faire ?

#### Les différentes méthodes de tri

Nous allons maintenant voir quelques-unes des différentes techniques appelées "**méthodes de tri**" qui permettent de réaliser cet exercice plus facilement (ou pas).
Surtout, n'oubliez pas de compter le nombre de comparaisons que vous effectuez.
*************************
##### Le tri par sélection

Le tri par sélection est l'une des méthodes de tri les plus simples à comprendre, mais n'est *pas très efficace* :

1. Cherche le pot le plus léger et pose-le sur le côté

2. Recommence l'étape 1 avec les pots qui restent. Cette fois, au lieu de le mettre seul sur le côté, pose le juste à droite du dernier pot que tu as sorti

3. Recommence l'étape 2 jusqu'à avoir retiré tous les poids

**Question** : Au total, combien de comparaisons as-tu fait ? Note ce nombre


[Ressource supplémentaire pour le tri par sélection](http://lwh.free.fr/pages/algo/tri/tri_selection.html)

*************************
##### Le tri par insertion

Le tri par insertion est *plus efficace que le tri par sélection*. Il consiste à choisir au hasard un élément parmi ceux qui restent et de l'insérer à la bonne place dans la liste des éléments déjà triés :

1. Choisi deux pots au hasard, compare leurs poids et pose-les sur le côté, dans le bon ordre (le plus léger à gauche, le plus lourd à droite)

**Tant qu'il reste des pots à placer** :

2. Choisi un pot au hasard parmi ceux qui restent à placer

3. Compare ton pot avec celui qui est placé le plus à droite parmi ceux que tu as déjà placés :
<br>**Si ton pot est plus lourd**, place le à droite du pot avec lequel tu viens de faire la comparaison et reviens à l'étape 2
<br>**Si ton pot est plus léger**, recommence l'étape 3 en comparant ton pot avec celui juste à gauche du pot avec lequel tu viens de faire la comparaison. <br>Si tu es arrivé au dernier pot et que le tiens est toujours plus léger, pose ton pot tout à gauche. <br>Enfin, reviens à l'étape 2

**Question** : Au total, combien de comparaisons as-tu fait ? Note ce nombre


[Ressource supplémentaire pour le tri par insertion](http://lwh.free.fr/pages/algo/tri/tri_insertion.html)

*************************
##### Le tri rapide

Le tri rapide est *le tri le plus efficace* :

1. Choisi un pot au hasard

2. Compare ce pot avec tous les autres du groupe, place à sa droite tous ceux qui sont plus légers et à sa gauche tous ceux qui sont plus lourds  

3. Choisi soit le groupe des plus légers, soit le groupe des plus lourds et recommence la procédure à partir de l'étape 1 sur le groupe choisi. <br>*Attention* : laisse toujours au centre le pot que tu avais choisi au tout début

4. Fais la même chose avec les autres groupes jusqu'à ce que tous les groupes ne contiennent qu'un seul pot chacun

**Question** : Au total, combien de comparaisons as-tu fait ? Note ce nombre


[Ressource supplémentaire pour le tri rapide](http://lwh.free.fr/pages/algo/tri/tri_rapide.html)

************************

## Partie 2 - Éclairage scientifique

### Notions abordées

S'intéresser aux différentes méthodes de tri nous a permis d'aborder quelques notions d'informatique, et notamment des notions très courantes dans la programmation :

- **La répétition avec les boucles "tant que"** :<br>
En programmation, la boucle "while", francisée en boucle "tant que", est une structure de contrôle permettant d'exécuter un ensemble d'instructions de façon répétée sur la base d'une condition booléenne (= vrai ou faux). <br>
En d'autres termes, elle permet de **répéter** des instructions **tant que** la condition fixée n'est pas validée (cf. partie tri par insertion)

- **Les instructions conditionnelles** :<br>
Une instruction conditionnelle est une action effectuée sur la base d'une condition booléenne. <br> Autrement dit, cette action est effectuée **si** la condition fixée est validée (cf. partie tri par insertion)

- **La récursivité** :<br>
La récursivité consiste à remplacer les instructions de boucle par des appels de fonctions. Le mécanisme consiste à créer une fonction qui s'appelle elle-même une ou plusieurs fois selon différents critères. Cela permet de résoudre un problème en répétant des instructions sur des instances plus petites à chaque appel de fonction jusqu'à ce qu'une certaine condition appelée "cas terminal" soit atteinte (cf. partie tri rapide). *Définition d'une fonction* : une fonction est un ensemble d'instructions réalisant une certaine tâche ou un calcul.

## Conclusion

Avoir des informations triées permet de trouver ce qu'on cherche plus facilement. Par exemple, les mots d'un dictionnaire sont triés par ordre alphabétique, s'ils ne l'étaient pas il serait bien trop long de trouver les mots recherchés.

Lorsqu'on manipule de grandes quantités d'informations, les trier peut être extrêmement long et coûteux, c'est pour cette raison qu'il est important de trouver le moyen le plus efficace d'effectuer des tris selon la situation, cela fait partie du travail des informaticiens. La plupart du temps, c'est le tri rapide qui est le plus efficace, c'est donc celui-ci qui est le plus souvent utilisé.

<p style="text-align:right;"> Auteur : <b>Rachid Chabane</b> </p>
