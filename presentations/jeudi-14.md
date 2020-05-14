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

En systèmes dynamiques, on regarde souvent le système à conjugaison près. Dans l'exemple qu'on vient de donner, c'est pareil d'étudier la dynamique de $ρ$ sur $𝕊^1$ que d'étudier la translation par $α$ sur $𝕋 = ℝ/ℤ = [0,1]/\{0~1\}$. 

## Les rotations comme échanges d'intervalles

Revenons à la rotations vue comme un déplacement par $α ∈ [0,1[$ sur $𝕋 = ℝ/ℤ = [0,1]/\{0~1\}$. Si on veut pour chaque élement de $𝕋$ utiliser aussi un représentant dans $[0,1[$, la définition de $ρ$ pourrait s'écrire comme l'union des deux applications suivantes:

$$\begin{array}{rcrcll} ρ_- & : & [0,1-α[ & \to & [α,1[\\
                            &   &    x \mapsto x + α $$

et 

$$\begin{array}{rcrcll} ρ_+ & : & [1-α,1[ & \to & [0,α[\\
                            &   &    x \mapsto x + α - 1 $$

De sorte que $ρ$ agit en échangeant deux intervalles - on dit que c'est un échange d'intervalles.

De façon générale, un échange d'intervalles est une transformation d'un intervalle muni d'une partition finie en intervalles plus petits qui rearrange ces intervalles par des translations, de sorte que le résultat est encore une partition du plus grand intervalle (à ceci près que les bords des petits intervalles peuvent être couvers $0$, $1$ ou $2$ fois). Mon directeur de thèse, Jean-Christophe Yoccoz, avait beaucoup étudié la dynamique de ces systèmes.

Ainsi, la rotation du cercle est un exemple d'échange d'intervalles avec deux intervalles.


## Un exemple fondamental: le tore

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

Ainsi, à chaque suite bi-infinie $(α_n)_{n∈ℤ}$ correspond une transformation du cylindre discret $ℤ×𝕋$, définie partout sauf sur un ensemble discret de points singuliers ( ceux qui après rotation arriveraient sur les bords des parties montantes et descendants). C'est cette famille de transformations $T_{α_}$ que j'ai étudié dans ma thèse.

## Dynamique générique d'une famille de transformations de $ℤ×𝕋$

La famille de transformations ainsi définie a comme espace de paramètres $𝕋^n$, qui dispose d'une mesure de probabilité et d'une topologie produit. C'est en particulier un espace de Baire. Un ensemble $G_δ$-dense est défini comme une intersection dénombrable d'ensembles ouverts denses, et un espace de Baire est un espace topologique où tout ensemble $G_δ$-dense est dense. 

On dit qu'une propriété dynamique est presque sûre dans la famille si et seulement si elle est satisfaite sur un ensemble de mesure totale de paramètres. On dit que la propriété est (Baire) générique si elle est satisfaite sur un ensemble $G_\delta$-dense de paramètres.

Pour simplifier les notations, on va écrire $α$ pour la suite $(α_n)_{n\in ℤ}$. Dans ma thèse j'ai demontré que:

- presque sùrement, $T_α$ n'a pas d'ensemble errant de mesure positive
- génériquement:
      - $T_α$ est conservative
      - toute demi-orbite $T_α$ définie pour une infinité d'itérations est dense (c-à-d $T_α$ est **minimal**)
      - tout sous-ensemble invariant par $T_α$ est de mesure nulle ou bien a un complement de mesure nulle (c-à-d $T_α$ est **ergodique**)

## Techniques developpées dans la thèse

Pour montrer ces résultats, je me suis appuyé sur des résultats bien connus pour des échanges d'intervalles, pour lesquelles les propriétés dynamiques que j'étudiais était déjà bien connues:

**Thm (Poincaré)** Tout système dynamique de mesure finie est conservatif.

**Thm (Keane)** Tout échange d'intervalles "irréductible" est minimal.  

**Thm (Masur-Tabachnikov)** Tout échange d'intervalle minimal est aussi ergodique.

Ensuite, j'ai procédé par perturbations: des valeurs spéciales de $α_n=±½$, (c-à-d les rotations par un demi-tour), permettent d'obtenir des sous-ensembles dans l'espace des phases qui sont invariants et qui sont des échanges d'intervalles classiques. Ensuite, en traduit la propriété dynamique qu'on veut montrer dans une formule quantitative et puis on construit des ouverts denses autour de ces paramètres spéciaux en prenant garde à ne pertuber qu'un petit peu cette formule. 

## Les surfaces en escalier.

Les résultats obtenus dans ma thèse se traduisent sur des surfaces de translation d'un type particulier, les surfaces en escalier.

En effet, considérons un collection dénombrable de rectangles de même largeur mais de hauteur variable, superposées comme un escalier qui monterait de gauche à droite, recollé sur la moitié de la largeur entre chaque marche et la suivante. Identifions les "côtés opposés" comme on avait fait pour le tore où la surface en L.

On obtient ainsi une famille de surfaces de translations, avec une surface en escalier pour chaque suite bi-infinie de hauteurs. 

Fixons une direction ni verticale, ni horizontale, l'application de premier retour sur les sections circulaires à mi-hauteur de chaque marche devient alors la transformation étudiée dans ma thèse. 

## Le modèle wind-tree des Ehrenfest: 

Tout de suite après ma thèse, j'ai effectué un postdoctorat à l'université de Marseille. J'y ai initié une collaboration avec Serge Troubetzkoy qui a donné lieu à cinq articles (quatre déjà parus), concernant principalement la dynamique générique du modèle du wind-tree des Ehrenfest.

Le wind-tree est un billard mathématique qu'on joue dans le complement d'un ensemble d'obstacles carrés, parallèles les uns aux autres. 

https://rantonse.no/demos/MirrorRoom/

Avec Serge, on a montré que génériquement, la dynamique du wind-tree est minimale (2015), ergodique (2016), de puissances cartésiennes ergodiques (2016-2017) et uniquement ergodique (2017-2019) dans presque toute direction. Les techniques de demonstration restent similaires à ce que j'avais fait dans ma thèse, mais la maîtrise technique et calculatoire nécessaire pour mener les preuves à bout est plus poussée pour pouvoir couvrir simultanément un ensemble large de directions - et car on s'occupe aussi de propriétés dynamiques plus subtiles. 

## Retour aux surfaces en escalier:

Les résultats que je viens d'énoncer pour le wind-tree, sont aussi valides pour des familles de surfaces en escaliers où l'on varie une seule sorte de paramètres de construction: la hauteur des marches, la largeur des marches ou la taille de recollement entre une marche et la suivante. 

Pourtant, sauf dans notre dernier pre-print, avec Serge on a rédigé les preuves pour le wind-tree et non pas pour des surfaces en escalier. Je prépare un article de survol qui contiendra les preuves pour le cas des surfaces en escaliers, et j'ose esperer qu'il sera plus accessible et plus lisible maintenant que le sujet a bien mûri pour moi. 

# Illustrations des mathématiques et intégration dans Gamble

## Impression 3D de surfaces algébriques
## Impression 3D d'autres objets mathématiques
## Analyse d'anciens objets en plâtre

# Ce que (je pense que) je peut apporter dans Gamble
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
  