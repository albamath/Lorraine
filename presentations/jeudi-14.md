% Activités de recherche - une présentation pour GAMBLE
% Alba Marina MÁLAGA SABOGAL
% 14 mai 2020

# Systèmes dynamiques

## Le problème général

Ce qu'on connaît:

- l'évolution à court terme
    - par exemple:
        - une fonction qu'on itère (temps discret)
        - un champ de vecteur qu'on suit (temps continu)

Ce qu'on en déduit:

- le comportement à long terme
    - par exemple: partie invariantes

Les outils:

- topologie, géométrie, théorie de la mesure, probabilités,...

Le jargon:

- ergodique, minimal, faiblement ou fortement mélangeant, ensemble invariant, mesure invariante, espace des phases

## Un exemple concret : les rotations du cercle:

Soit $𝕊^1$ le cercle unité.
Soit $α$ un nombre réel quelconque et considérons la rotation $ρ$ par $α$ tours de $𝕊^1$.

Ceci définit un système dynamique:

- l'évolution à court terme est donnée par $ρ$ par qui l'on connaît le futur immédiat de n'importe quel point $z$ sur 
  le cercle: $ρ(z)$
- l'orbite future d'un point $z$ est la suite / l'ensemble $\{ρ^n(z):n∈ℤ\}$

Un résultat classique de Poincaré montre la dichotomie suivante:

- si $α$ est rationnel alors toute orbite est périodique
- si $α$ est irrationnel alors toute orbite est dense (on dit que le système est **minimal**) et les moyennes 
  temporelles convergent à la moyenne spatiale (on dit que le système est ergodique) 

Ν.Β. Une pièce clé de la preuve de se théorème est le développement en fractions continues d'$α$.

En systèmes dynamiques, on regarde souvent le système à conjugaison près. Dans l'exemple qu'on vient de donner, c'est pareil d'étudier la dynamique de $ρ$ sur que d'étudier la translation par $α$ sur $𝕋 = ℝ/ℤ = [0,1]/\{0~1\}$. 

## Exemple le plus simple de surface de translation: le tore

Mes recherches en systèmes dynamiques  portaient concrètement sur des surfaces de translation, principalement des surfaces de translation de mesure infinie. 
Voyons d'abord la surface de translation la plus simple, le tore:

Voir http://albamath.com/snake

Le premier prototype de tore plat est obtenu en identifiant les côtés opposés d'un carré avec la même orientation. On remarquera que les quatre sommets du carré sont identifiés et que l'angle total autour du sommet est de 360 degrés soit quatre quarts de tour.

On va appeler tore tout court n'importe quel espace topologique homéomorphe au résultat de cette construction. 

On peut identifier un tore par sa caractéristique d'Euler, 0, ou de façon équivalente par son genre, 1. 

Par le théorème de Gauss-Bonnet, on sait que si on arrive à mettre une géométrie à courbure constante partout sur 
un tore, alors c'est une courbure constante nulle. Réciproquement, si une surface compacte sans bord est de courbure 
constante nulle, alors cette surface est un tore, qu'on appellera un tore plat.

Ainsi, si dans la construction ci-dessus on prend un rectangle à la place du carré, on obtient aussi un tore. 
De même, si l'on identifie les côtés opposés d'un hexagone régulier, où si l'on identifie les côtés opposés d'un 
parallélogramme quelconque, on obtient un tore plat.

## Un autre exemple simple de surface de translation: le L

Revenons à notre serpent, et imaginons qu'on retire un coin du carré sur lequel on jouait le jeu à la base, tout en continuant la règle que lorsque le serpent disparaît à droite, il reapparaît à gauche etc. 

http://albamath.com/snake-L

Quelle est maintenant la géométrie sous-jacente au jeu ?

Remarquons d'abord que les six sommets de l'hexagone sont identifiés entre eux et avec les points du milieu des côtés longs.

On peut facilement calculer la caractéristique d'Euler de la surface topologique sous-jacente au jeu à partir d'un quadrillage du jeu: $χ = V-E+F = 1 - 6 + 3 = -2$. Or $χ=2-2g$, donc $g=2$.

Ainsi, la surface sous-jacente est de genre 2, mais on voit bien que sa géométrie est plate, comment c'est possible ? Est-ce une contradiction au théorème de Gauss-Bonnet ? En fait, la courbure est en quelque sorte concentré sur un seul point, le coin de la figure L. Si on regarde de près, le serpent est obligé de faire huit quarts de tour pour en faire le tour, c'est à dire que l'angle total autour de ce point est de deux tours.

On voit peut-être mieux cet angle sur une autre vue de cette surface de translation, la vue "en croix".

http://albamath.com/snake-X

## Définition de surface de translation "finie".

Une surface de translation est une surface compacte sans bord qui, privée d'un nombre fini de points,  possède un atlas tel que que les changements de cartes dans cet atlas sont des translations. Supposons que l'atlas est maximal - les points non couverts par l'atlas sont des singularités coniques de la géométrie de la surface avec un angle qui est un multiple entier de 360 degrés.

## Dynamique sur une surface de translation

La dynamique sur une surface de translation est le flot par droites. Une particule à une position données et dans une direction donnée sur la surface ira tout droit devant soi tant qu'elle ne bute pas sur un point conique de la surface. 

Ainsi, cette dynamique possède des singularités - par convention, on considère que le futur des points coniques n'est pas défini.

On appelle connexion de selle toute trajectoire reliant deux points coniques entre eux.

Les trajectoires du serpent lorsqu'on arrête de le manipuler dans les jeux montrés tout à l'heure sont des exemples de trajectoires de cette dynamique. Ce sont pourtant des exemples assez particuliers car le serpent ne prend qu'une direction verticale ou une direction horizontale. 

## Billards: un contexte où les surfaces de translation apparaissent naturellement

Considérons une figure polygonale dans le plan et jouons au billard mathématique dedans. C'est comme le billard mais avec des balles qui n'ont pas de masse, de volume/aire, sans frictions et dont tous les rebonds sont parfaitement élastiques. Si on veut, un modèle physique plus exact pour le billard mathématique, c'est un rayon laser dans une pièce aux murs couvers de miroirs; plutôt qu'une balle sur une table de billard polygonale.

Une construction classique, due à Katok et Zemljakov, permet de déplier les trajectoires de billards: moralement, à chaque fois qu'une trajectoire devrait rebondir sur le bord de la table, on la prolonge dans la même direction. 

Par exemple, le dépliage d'un billard carré donne un tore.

De façon générale, à chaque fois qu'une table de billard polygonale n'a que des angles qui sont des fractions de tour, le résultat du dépliage est une surface de translation finie. On appelle de telles tables, des tables rationnelles.

## Questions ouvertes sur des billards polygonaux:

Même pour les billards triangulaires, on ne sait pas si:

- il existe toujours des trajectoires périodiques ?
- toutes les trajectoires sont denses ? (**minimalité**)
- il y a ou pas des partitions non triviales (en mesure) en sous-ensembles invariants ? (**ergodicité**) 

Grâce à la construction de dépliage on a des résultats positifs pour le cas de billards rationnels. En effet, pour ces billards,, les problèmes se traduisent dans des questions de dynamique sur des surfaces de translation "finies", où l'on peut s'appuyer sur une théorie déjà très mature. Mais pour des billards irrationnelles, le dépliage donne lieu à des surfaces de translation non compactes, avec possiblement des singularités "sauvages", et la dynamique sur ces surfaces et beaucoup moins bien connue. 

La troisième question de cette liste était le point de départ de ma thèse, effectuée de 2011 à 2014 à Orsay sous la direction de Jean-Christophe Yoccoz. La question est encore ouverte, he he, c'est à dire que finalement dans ma thèse je réponds à d'autres  questions (moralement) en rapport avec celle-ci. 

## Cylindres discrets - motivation

Pour commencer avec un exemple simple de billard triangulaire, considérons un triangle rectangle quelconque. En dépliant autour de l'angle droit, on voit bien que étudier ces billards est équivalent à étudier le billard dans un losange irrationnel dont les angles seraient les doubles des angles non droits du triangle en questions.

Regardons donc des billards dans des parallélogrammes. On a vu tout à l'heure que le billard dans un rectangle est déjà bien compris car il se déplie sur le tore. Regardons donc des billards dans un parallelogramme proche du rectangle, possiblement irrationnel.

Dans le début de ma thèse je calcule explicitement l'application de premier retour sur le bord d'un dépliage partiel de tels parallélogrammes, des calculs que je ne vais pas détailler ici, et je remarque la similarité avec des familles d'applications sur le cylindre discret $ℤ×𝕋$. L'étude de la dynamique de ces applications sera finalement l'objet de ma thèse. 

## Une famille de transformations du cylindre discret $ℤ×𝕋$

Considérons une suite bi-infinie de paramètres de rotation $α_n∈𝕋 = [0,1]/\{0~1\}$. Pour chaque suite de la sorte, appliquons la rotation par $α_n$ au cercle $\{n\}×𝕋$. Puis, coupons tous les cercles en deux intervalles de même longueur, independants des paramètres de rotation, et considérons leur intérieur, qu'on appelera la partie descendante, et la partie montante, puis déplaçons la partie de droite de un niveau vers le haut et la partie de gauche d'un niveau vers le bàs. 

Ainsi, à chaque suite bi-infinie $(α_n)_{n∈ℤ}$ correspond une transformation du cylindre discret $ℤ×𝕋$, définie partout sauf sur un ensemble discret de points singuliers ( ceux qui après rotation arriveraient sur les bords des parties montantes et descendants). C'est cette famille de transformations que j'ai étudié dans ma thèse.

## Dynamique générique d'une famille de transformations de $ℤ×𝕋$




# Les illustrations des mathématiques

## Impression 3D de surfaces algébriques
## Impression 3D d'autres objets mathématiques
## Analyse d'anciens objets en plâtre
# Intégration dans Gamble
## En tant que mathématicienne
Compétences poussées en:

- géométries 2D et 3D (y compris non-euclidiennes)
- systèmes dynamiques

Compétences raisonnables en:

- géométrie algébrique "à l'ancienne" (c-à-dire sans schemas)
- géométrie riemannienne
- analyse numérique
- théorie des probabilités

## En tant que dynamiste
- analyse d'algorithmes\
Beaucoup d'algorithmes ont comme pièce clé une boucle itérative.
Mais qu'est-ce qu'une itération si non l'évolution à court terme d'un système dynamique ? 
Les questions de convergence et de vitesse de convergence d'un algo sont finalement des questions de systèmes dynamiques.
- relation entre géométrie plate et géométrie hyperbolique\
Les surfaces de translation, que j'ai beaucoup étudié, sont des cas particuliers de surfaces de demi-translation. Il existe une correspondance standard entre la métrique plate d'une surface de demi-translation et une métrique hyperbolique. Je me demande si les algorithmes que vous étudiez pour des géométries hyperboliques ne pourraient pas bénéficier de ce dictionnaire.
- apport de problèmes
Dans le domaine de la géométrie computationnelle, j'ai plus de questions que de réponses. Des questions, j'en ai plein:
    - mieux detecter les lieux singuliers d'une surface algébrique
    - compléter les descriptions partielles d'objets historiques
    - trancher les surfaces pour l'impression 3D directement à partir de leur équations

## En tant qu'informaticienne

- un petit peu d'expérience
- beaucoup d'envies d'apprendre

## En tant que médiatrice scientifique

- une facilité à parler de sciences avec... tout le monde 
Cela permet de trouver plus facilement non seulement un public mais aussi des collaborateurs un peu atypiques. Je finis par exemple en ce moment un article sur des pliages en papier avec un architecte (et un autre avec des mathématiciens).
- un réseau de contacts en mathématiques qui va bien au-délà de mon domaine
Le réseau AudiMath réuni des mathématiciens universitaires qui font de la diffusion scientifique. Avec Imaginary, j'y participe depuis 2015. 
- un savoir-faire de "maker"
Au fur et à mesure, je suis devenue familière du découpage laser et de l'impression 3D ce qui me permet de prototyper très rapidement toutes sortes d'illustrations - on pourrait utiliser ce savoir-faire pour vos algos.
  