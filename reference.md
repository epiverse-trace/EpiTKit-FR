---
title: Glossaire
editor_options: 
  markdown: 
    wrap: 72
---

# Théorie et modèles des épidémies

## Modèle mathématique des maladies infectieuses

Un modèle mathématique dans la théorie des épidémies de maladies infectieuses est une représentation abstraite qui utilise des équations et des algorithmes mathématiques pour décrire la dynamique de la propagation d'une infection au sein d'une population. Ces modèles permettent de comprendre, de prédire ou de projeter comment une maladie infectieuse peut se propager et affecter une communauté, en tenant compte de divers facteurs tels que le taux de transmission, la période infectieuse, le rétablissement et l'immunité.

Le modèle mathématique classique est le modèle SIR : Susceptible, Infectieux et Rétabli. Celui-ci utilise traditionnellement des équations différentielles ordinaires (EDO).

Il existe plusieurs types de modèles mathématiques, les plus courants étant : [déterministe](#modèle-déterministe) et [stochastique](#modèle-stochastique).

## Équations différentielles ordinaires (EDO)

Les équations différentielles ordinaires (EDO) peuvent être utilisées pour représenter le taux de changement d'une variable (par exemple, le nombre d'individus infectés) par rapport à une autre (par exemple, le temps). Les EDO sont largement utilisées dans la modélisation des maladies infectieuses pour modéliser le flux d'individus entre différents états de la maladie.

Pour plus d'informations, consultez cette introduction aux [EDO](https://mathinsight.org/ordinary_differential_equation_introduction).

## Modèle déterministe

Un modèle déterministe est un type de modèle mathématique dans lequel le comportement du système est entièrement déterminé par ses conditions initiales et les paramètres du modèle, sans impliquer d'éléments de hasard ou d'incertitude. En d'autres termes, étant donné un ensemble de conditions initiales et de paramètres, le modèle produira toujours les mêmes résultats.

## Modèle stochastique

Un modèle stochastique aborde la variation aléatoire des paramètres dans les simulations du modèle pour les mêmes conditions initiales. Cela signifie que les résultats exacts ne seront pas toujours obtenus dans toutes les simulations. Les exemples incluent les équations différentielles stochastiques et les modèles de processus de branchement. Pour plus de détails, consultez [Allen (2017)](https://www.sciencedirect.com/science/article/pii/S2468042716300495?via%3Dihub).

## Conditions initiales

Dans les équations différentielles ordinaires (EDO), les conditions initiales sont les valeurs de chaque compartiment au temps initial du modèle (temps zéro). Ces conditions sont nécessaires pour démarrer la simulation de l'épidémie dans le modèle et peuvent affecter de manière significative les résultats ultérieurs.

Exemple : S'il y a un individu infectieux dans une population de 1000 personnes dans un modèle Susceptible-Infectieux-Rétabli, les conditions initiales seraient :
* $S_0=999$
* $I_0=1$
* $R_0=0$

## Paramètres du modèle de transmission

Les paramètres du modèle sont des valeurs qui permettent le mouvement des individus entre les différents compartiments ; ils décrivent le flux entre les états de la maladie. Ceux-ci incluent, par exemple : le taux de récupération qui est un paramètre du modèle qui peut être utilisé pour décrire le flux entre les états infectieux et rétabli.

## Variables d'état

Les variables d'état dans un modèle représenté par des équations différentielles ordinaires sont les états de la maladie dans lesquels les individus peuvent se trouver. Par exemple, si les individus peuvent être susceptibles, infectieux ou rétablis, les variables d'état sont S, I et R. Il existe une équation différentielle ordinaire pour chaque variable d'état.

## Susceptible

Population n'ayant eu aucune exposition antérieure ou actuelle à l'agent pathogène, ou sans vaccination, et n'ayant donc ni infection ni protection immunitaire humorale (anticorps neutralisants) contre l'agent pathogène. (Lié aux variables d'état)

Exemples :
* En 2020, au début de la pandémie de COVID-19, l'ensemble de la population mondiale était considérée comme susceptible.
* Enfants non vaccinés contre la rougeole et qui n'ont pas été infectés ou n'ont pas développé d'anticorps post-infection.

## Infectieux

Population avec présence active de l'agent pathogène capable de le transmettre à des individus susceptibles dans la population. Cet état a une durée équivalente à la période infectieuse.

Exemple :
* Patient vivant avec le VIH ne recevant pas de traitement antirétroviral avec une charge virale élevée qui a des relations sexuelles non protégées.

## Rétabli

Population avec des anticorps neutralisants contre l'agent pathogène. Cette immunité pourrait avoir été acquise par infection naturelle ou par vaccination. Cet état a une durée équivalente à la durée de l'immunité neutralisante. (Lié aux variables d'état)

Exemple :
* Personne vaccinée contre la fièvre jaune. Ce vaccin offre une protection élevée et durable contre l'infection.

## Exposé

Population qui a été infectée par un agent pathogène mais n'est pas encore capable de transmettre l'infection (infectée, mais non infectieuse). Cet état a une durée équivalente à la période de latence.

Exemple :
* La transmission du bacille de la tuberculose se produit à partir de sujets bacillifères positifs qui libèrent des bacilles dans l'environnement, et les individus exposés sont facilement infectés. Cependant, pendant de nombreuses années, les individus peuvent rester infectés mais contrôler la maladie, sans la transmettre ; ces individus sont considérés comme exposés dans les modèles de transmission dynamique.

## Débordement (Spillover)

En épidémiologie, le terme débordement (spillover) fait référence au processus par lequel un agent pathogène (micro-organisme, qu'il s'agisse d'un virus, d'une bactérie, d'un parasite ou autre), qui affecte normalement une espèce animale spécifique, est transmis à un autre réservoir. En d'autres termes, il s'agit du saut évolutif d'un agent pathogène entre espèces, ce qui inclut la transmission d'un animal à un humain.

## Zoonose

L'OPS définit la zoonose comme "des maladies infectieuses naturellement transmissibles des animaux vertébrés aux humains".

## Paramètres de transmission

## Nombre de reproduction de base, $R_0$

Il est défini comme le nombre moyen de cas secondaires produits à partir d'un cas primaire dans une population totalement susceptible, c'est-à-dire au temps 0. Ce nombre est spécifique à chaque agent infectieux, bien qu'il puisse également être affecté par des variables climatiques et sociales, et représente le potentiel de transmission de l'agent pathogène. Cette valeur est théorique et détermine également le seuil d'immunité collective. C'est une mesure de la transmissibilité d'une infection. Il est calculé comme suit :

$R_0 = p * c * D$

Où,
$p$ = probabilité d'infection après contact
$c$ = taux de contact
$D$ = durée de la période infectieuse

Exemple :
* Le diagramme suivant compare le $R_0$ de la grippe saisonnière, d'Ebola, de la diphtérie, de la variole et du syndrome respiratoire de la rougeole.

## Nombre de reproduction effectif, $R_t$

Il est défini comme le nombre moyen de cas secondaires à partir d'un cas infectieux dans la population composée d'hôtes susceptibles et non susceptibles par unité de temps (t). Il est calculé comme suit :

$R_t = R_0 * S$

Où :
$R_0$ = Nombre de reproduction de base
$S$ = proportion de susceptibles dans la population

Caractéristiques du nombre de reproduction effectif, $R_t$ :
* **Temporel** : $R_t$ reflète la situation actuelle de la transmission de la maladie et change au fil du temps.
* **Contextuel** : Contrairement à $R_0$, qui suppose une population complètement susceptible, $R_t$ tient compte de l'impact de l'immunité acquise (par infection ou vaccination) et des interventions de santé publique (telles que la distanciation sociale, les quarantaines et l'utilisation de masques).

Interprétation :
* $R_t > 1$ : L'infection se propage dans la population.
* $R_t = 1$ : L'infection reste stable dans la population.
* $R_t < 1$ : L'infection diminue et peut éventuellement disparaître.

$R_t$ peut être influencé par deux grands groupes de facteurs :
* Mesures de contrôle : médicaments antimicrobiens, mesures barrières (préservatifs, masques) et mesures de réduction des contacts (isolement, distanciation, utilisation de moustiquaires, fumigation, etc.).
* Acquisition de l'immunité par des anticorps neutralisants (réduction des susceptibles à mesure qu'une épidémie progresse ou par vaccination).

## Taux de contact

Le **taux de contact** est une mesure épidémiologique qui décrit la fréquence à laquelle les individus d'une population entrent en contact les uns avec les autres, sur une période de temps spécifique, de manière à permettre la possibilité de transmission d'une maladie infectieuse. Ce taux est fondamental pour comprendre et modéliser la dynamique de la propagation de la maladie au sein d'une communauté.

Caractéristiques du taux de contact :
* **Fréquence** : Reflète le nombre de contacts potentiellement infectieux par individu sur une période donnée.
* **Homogène vs hétérogène** : Le taux de contact peut être homogène, si les contacts sont répartis uniformément entre tous les individus, ou hétérogène, si certains individus ont plus de contacts que d'autres, ce qui est courant dans la réalité.
* **Influence des facteurs** : Le taux peut varier en fonction de facteurs tels que l'âge, le comportement, l'environnement et les mesures de contrôle (par exemple, la distanciation sociale).

Calcul du taux de contact : Le taux de contact peut être estimé à partir de données empiriques recueillies par des enquêtes, des études observationnelles ou des inférences à partir de modèles mathématiques.

## Matrice de contact

Une **matrice de contact** est un outil épidémiologique qui représente les taux de contact entre différents groupes d'une population, normalement organisés par catégories telles que l'âge, le sexe ou le lieu géographique. Chaque élément de la matrice indique la fréquence à laquelle les individus d'un groupe spécifique ont des contacts avec des individus d'un autre groupe.

Caractéristiques de la matrice de contact :
* **Structure** : C'est une matrice carrée, où les lignes et les colonnes représentent les différents groupes de population.
* **Éléments** : Chaque cellule de la matrice indique le nombre moyen de contacts entre les individus des groupes correspondants.
* **Données** : Les données peuvent être collectées par le biais d'enquêtes, d'études observationnelles ou inférées à partir de modèles mathématiques.

## Période de latence

Intervalle de temps entre l'exposition à un agent infectieux avec transmission réussie et l'apparition de la période infectieuse. Pendant la période de latence, les individus infectés ne transmettent pas l'infection.

Exemples :
* Pour la tuberculose, la période de latence est généralement prolongée, et après la contagion, les individus restent sans transmettre la maladie pendant de nombreuses années.
* Pour l'infection par le SARS-CoV-2, la période de latence était courte (2-4 jours) et également plus courte que la période d'incubation, de sorte que les individus pouvaient transmettre l'infection avant l'apparition des symptômes.

## Période d'incubation

Intervalle de temps entre l'exposition à un agent infectieux avec transmission réussie et l'apparition de la maladie clinique (signes et symptômes). Pour les maladies où l'apparition de la période infectieuse coïncide avec l'apparition des signes et des symptômes, les périodes de latence et d'incubation sont les mêmes.

Exemple :
* Dans l'étude de Wu et al. 2022, une revue systématique des périodes d'incubation du SARS-CoV2 a été réalisée. Il a été constaté que : la période d'incubation moyenne de la COVID-19 était de 5,00 jours (IC à 95 %, 4,94-5,06 jours) pour les cas causés par le variant Alpha, 4,50 jours (IC à 95 %, 1,83-7,17 jours) pour le variant Beta, 4,41 jours (IC à 95 %, 3,76-5,05 jours) pour le variant Delta, et 3,42 jours (IC à 95 %, 2,88-3,96 jours) pour le variant Omicron. Les résultats de cette étude suggèrent que le SARS-CoV-2 a continuellement évolué et muté tout au long de la pandémie de COVID-19, produisant des variants avec différents niveaux de transmission et de virulence. L'identification de la période d'incubation des différents variants est un facteur clé pour déterminer la période d'isolement.

## Période infectieuse

Intervalle de temps pendant lequel l'individu infecté présente une réplication active de l'agent pathogène et peut le transmettre à d'autres individus. Comme cette période peut chevaucher la période d'incubation, il peut être difficile d'obtenir des estimations précises de la période infectieuse. La charge virale et la détection du virus infectieux sont les deux paramètres clés pour estimer l'infectiosité ([Puhach et al., 2022](https://www.nature.com/articles/s41579-022-00822-w) et [Hakki et al, 2022](https://www.thelancet.com/journals/lanres/article/PIIS2213-2600(22)00226-0/fulltext)).

Exemple :
* Dans les cas de virus respiratoires (par exemple, la grippe, le SARS-CoV-2), cette période peut durer des jours, tandis que pour des maladies comme le VIH ou la tuberculose, elle peut durer des années.

## Temps de récupération

Intervalle de temps entre l'apparition de la période infectieuse et le moment où un individu cesse de transmettre l'agent pathogène.

Exemple :
* Dans les cas de varicelle, les sujets cessent de transmettre l'agent pathogène lorsque toutes les lésions se sont croûtées. Par conséquent, la période de récupération apparaît avant la disparition des lésions. Après cette période, les sujets sont considérés comme rétablis.

## Temps de génération

Intervalle de temps entre le début de la période infectieuse d'un cas primaire et le début de la période infectieuse d'un cas secondaire, infecté par le cas primaire. Il est normalement inconnu et est approximé par l'intervalle sériel. Il ne peut pas être mesuré, seulement estimé.

Exemple :
* L'étude de Hart et al. 2022 au Royaume-Uni entre février et août 2021 a recruté 227 ménages avec 559 participants. Il a été constaté que le variant Delta se transmettait plus rapidement que le variant Alpha dans les ménages, avec un temps de génération moyen plus court : 4,7 jours pour Delta contre 5,5 jours pour Alpha. Cela suggère que Delta se propage plus rapidement dans les ménages en raison d'une diminution rapide des individus susceptibles, ce qui pourrait rendre les interventions telles que la recherche des contacts et l'isolement moins efficaces.

## Intervalle sériel

Période de temps entre le **début des symptômes** d'un cas primaire et le début des symptômes d'un cas secondaire infecté par le cas primaire. Il est mesurable étant donné que des données telles que les dates d'apparition des symptômes peuvent être obtenues. Cette valeur peut être négative en cas d'infection présymptomatique. La distribution de l'intervalle sériel d'une infection est couramment utilisée pour estimer la distribution du temps de génération ([Cori et al., 2017](https://royalsocietypublishing.org/doi/10.1098/rstb.2016.0371)). La relation entre l'intervalle sériel et la période d'incubation aide à définir le type de transmission de l'infection (symptomatique ou présymptomatique) ([Nishiura et al., 2020](https://www.ijidonline.com/article/S1201-9712(20)30119-3/fulltext#gr2)).

Exemple : Dans l'étude de Nishiura et al. 2020, l'intervalle sériel de la COVID-19 a été estimé à partir de 28 paires infecteur-infecté. Les dates d'apparition de la maladie pour les cas primaires et secondaires ont été analysées, en ajustant pour la troncature à droite car l'épidémie était toujours en croissance. Les résultats ont montré que l'intervalle sériel médian était de 4,0 jours dans l'ensemble des données et de 4,6 jours dans le sous-ensemble de paires avec une plus grande certitude. Il est conclu que l'intervalle sériel de la COVID-19 est proche ou plus court que sa période d'incubation, suggérant une transmission significative avant l'apparition des symptômes, et est plus court que l'intervalle sériel du SRAS, ce qui pourrait introduire un biais dans les calculs basés sur le SRAS.

## Taux d'attaque

Le **taux d'attaque** est une mesure épidémiologique qui décrit la proportion de personnes dans une population spécifique qui développent une maladie ou une infection pendant une période définie, généralement dans le contexte d'une épidémie. Ce taux inclut à la fois les cas de maladie et les infections asymptomatiques, et peut nécessiter des études de séroprévalence ou des modèles mathématiques pour un calcul précis.

Caractéristiques :
* **Objectif** : Évalue la proportion de personnes qui tombent malades ou sont infectées parmi celles initialement exposées.
* **Contexte** : Utilisé pour mesurer l'impact immédiat de l'exposition à un agent infectieux.

## Taux d'attaque secondaire symptomatique

Le **taux d'attaque symptomatique** mesure la proportion de personnes exposées qui développent des symptômes cliniques de la maladie. Il se concentre exclusivement sur les individus qui présentent des symptômes, se différenciant ainsi du taux d'attaque général qui peut inclure des cas asymptomatiques.

Caractéristiques :
* **Objectif** : Évalue la proportion de personnes exposées qui développent des symptômes cliniques, fournissant une mesure de la manifestation clinique de la maladie.
* **Contexte** : Utilisé pour comprendre la gravité et l'impact clinique de la maladie dans une population spécifique.

## Taux d'attaque secondaire (TAS)

Le **taux d'attaque secondaire** mesure la proportion de cas qui surviennent parmi les contacts étroits des cas primaires. Il se concentre sur la transmission secondaire de la maladie, c'est-à-dire la propagation de la maladie des cas initiaux à d'autres individus en contact étroit.

Caractéristiques :
* **Objectif** : Mesure la transmission de la maladie parmi les contacts étroits des cas primaires.
* **Contexte** : Utilisé pour évaluer l'efficacité des mesures de contrôle et pour mieux comprendre la dynamique de transmission de la maladie.

## Seuil d'immunité collective

Le **seuil d'immunité collective** est la proportion de la population qui doit être immunisée contre une maladie infectieuse, soit par vaccination, soit par infection antérieure, pour que la propagation de la maladie diminue et finisse par s'arrêter. Lorsque ce seuil est atteint, même les individus non immunisés sont indirectement protégés en raison de la probabilité réduite de transmission de l'agent pathogène.

Caractéristiques du seuil d'immunité collective :
* **Proportion critique** : Représente la fraction de la population qui doit être immunisée pour interrompre la transmission soutenue de l'infection.
* **Dépendance au R₀** : Le seuil est directement lié au nombre de reproduction de base ($R_0$) de l'infection, qui est le nombre moyen de cas secondaires produits par un cas primaire dans une population totalement susceptible.

Calcul : Le seuil d'immunité collective dépend du nombre de reproduction de base $R_0$ et est défini comme $1 - \frac{1}{R_0}$. Plus un agent pathogène est contagieux, plus son $R_0$ est élevé et plus la proportion de la population qui doit être immunisée pour bloquer la transmission soutenue est grande.

Exemple :
* Dans le cas de la rougeole, pour un $R_0$ de 18, l'immunité collective est d'environ 95 %.

## "Dépassement" (Overshoot)

Le terme **dépassement** (overshoot) fait référence au phénomène par lequel le nombre de cas d'une maladie infectieuse dépasse le seuil d'immunité collective lors d'une épidémie, avant que la transmission de la maladie ne diminue et ne se stabilise. Cet excès de cas se produit malgré le fait qu'une proportion suffisante de la population ait atteint l'immunité nécessaire pour ralentir la propagation de la maladie.

Caractéristiques du dépassement :
* **Excès de cas** : Se produit lorsque le nombre de cas est supérieur à celui attendu, même après avoir atteint le seuil d'immunité collective.
* **Temporel** : C'est un phénomène transitoire observé avant que la maladie ne se stabilise ou ne disparaisse.
* **Immunité collective** : Indique que le seuil d'immunité collective a été atteint, mais que la transmission se poursuit initialement en raison de la dynamique épidémique.

Causes du dépassement :
* **Inertie épidémique** : La maladie continue de se propager en raison du nombre d'individus susceptibles encore exposés à l'agent infectieux avant que la transmission ne soit réduite.
* **Distribution hétérogène de l'immunité** : L'immunité n'est pas uniformément répartie dans la population, ce qui permet l'apparition d'épidémies localisées.

## Taille critique de la communauté (CCS)

C'est la taille minimale d'une population fermée requise pour qu'un agent infectieux persiste dans cette population. Si le nombre de la population est trop faible, après une épidémie, l'agent pathogène ne peut pas persister et disparaît. Cette masse critique de susceptibles est déterminée par les caractéristiques de l'agent, la structure démographique et les conditions hygiéniques de la population hôte.

Exemple : Pour la rougeole, qui a un $R_0$ élevé, la CCS est relativement grande. Des études ont montré que la rougeole a besoin d'une population d'au moins 250 000 à 500 000 individus pour rester endémique. En revanche, les maladies avec un $R_0$ plus faible peuvent avoir une CCS beaucoup plus petite.

## Superspreading (Super-propagation)

Le **superspreading** est un phénomène en épidémiologie des maladies infectieuses où un petit nombre d'individus infectés est responsable d'une grande proportion de nouvelles infections. Ces individus, appelés "superspreaders" (super-propagateurs), infectent un nombre beaucoup plus important de personnes que la moyenne attendue, accélérant ainsi la propagation de la maladie.

Caractéristiques du superspreading :
* **Variabilité de la transmission** : Il existe une grande hétérogénéité dans la capacité des individus à transmettre la maladie, quelques individus causant de nombreuses infections tandis que la plupart en causent peu ou pas.
* **Facteur de dispersion (k)** : Le degré de superspreading peut être quantifié à l'aide du paramètre k. Des valeurs faibles de k indiquent un superspreading élevé, tandis que des valeurs proches de 1 indiquent une dispersion plus uniforme.
* **Contexte spécifique** : Les événements de superspreading se produisent généralement dans des contextes spécifiques tels que les rassemblements de masse, les espaces confinés et les activités où il y a un contact étroit prolongé.

Exemple : Pendant la pandémie de COVID-19, plusieurs événements de superspreading ont été observés, comme une seule personne infectée infectant des dizaines de personnes lors d'un rassemblement religieux en Corée du Sud. Dans un autre cas, un événement choral aux États-Unis a entraîné de nombreuses infections à partir d'un seul individu infecté.

Exemple :
* En Corée du Sud, pendant la pandémie de COVID-19, des événements de super-propagation se sont produits dans le cadre de chorales religieuses, avec 11 grappes de transmission associées à 641 cas de COVID-19.

## Taux de croissance exponentiel

Le **taux de croissance exponentiel** est une mesure épidémiologique qui décrit la vitesse à laquelle le nombre de cas d'une maladie infectieuse augmente dans une population au début d'une épidémie, lorsque les mesures de contrôle n'ont pas été mises en œuvre ou sont minimes. Ce taux est fondamental pour comprendre la dynamique de la propagation de la maladie à ses premiers stades et pour planifier les interventions de santé publique.

Calcul du taux de croissance exponentiel : Le taux de croissance exponentiel peut être calculé à l'aide de la formule :

$$r = \frac{\ln(C_t) - \ln(C_0)}{t}$$

Où :
* $r$ est le taux de croissance exponentiel.
* $C_t$ est le nombre de cas au temps t.
* $C_0$ est le nombre initial de cas.
* $t$ est le temps écoulé.

## Paramètres de gravité

## Létalité

Désigne la gravité de la maladie par rapport au décès. Cela peut être classé comme IFR ou CFR.

## Taux de létalité de l'infection (IFR)

Probabilité de décès après infection (symptomatique ou asymptomatique).

Exemple :
* Pour le SARS-CoV-2, l'âge est de loin le principal facteur de risque de décès. Par conséquent, l'IFR moyen d'une population dépend de sa structure démographique.

## Taux de létalité des cas (CFR)

Probabilité de décès parmi les cas signalés. Il n'inclut généralement que les cas symptomatiques confirmés en laboratoire ou cliniquement. Par conséquent, le CFR sera toujours plus élevé que l'IFR.

Exemple :
* Le CFR rapporté pour Ebola a été estimé dans différentes épidémies entre 30 et 70 %.

## Taux de létalité hospitalière (HFR)

Le **Taux de Létalité Hospitalière (TLH)** est un paramètre épidémiologique qui mesure la proportion d'individus hospitalisés atteints d'une maladie spécifique qui décèdent de cette maladie. Ce ratio est une mesure de la gravité de la maladie chez ceux qui nécessitent une hospitalisation et fournit des informations cruciales sur l'efficacité du traitement hospitalier et la gravité de la maladie dans les cas les plus graves.

## Biais dans la déclaration des paramètres

## Biais de phase (Dynamique ou Épidémique)

Considère la susceptibilité de la population au moment où les paires de transmission (cas et contacts) sont observées. C'est un type de biais d'échantillonnage. Il affecte les données rétrospectives et est lié à la phase de l'épidémie : pendant la phase de croissance exponentielle, les cas récemment symptomatiques sont surreprésentés dans les données observées, tandis que pendant la phase de déclin, ces cas sont sous-représentés, conduisant à l'estimation d'intervalles de délai plus courts et plus longs, respectivement ([Park et al., en cours](https://github.com/parksw3/epidist-paper)).

## Retard de déclaration

Délai ou décalage entre le moment où un événement se produit (par exemple, l'apparition des symptômes) et le moment où il est signalé ([Lawless, 1994](https://www.jstor.org/stable/3315820)). Nous pouvons le quantifier en comparant la liste des cas avec des versions successives des mêmes ou avec des dénombrements de cas agrégés mis à jour ([Cori et al., 2017](https://royalsocietypublishing.org/doi/10.1098/rstb.2016.0371)).

## Biais de troncature à droite

Un type de biais d'échantillonnage lié au processus de collecte de données. Il survient parce que seuls les cas qui ont été signalés peuvent être observés. Le fait de ne pas tenir compte de la troncature à droite pendant la phase de croissance d'une épidémie peut entraîner une sous-estimation du délai moyen ([Park et al., en cours](https://github.com/parksw3/epidist-paper)).

## Censure

Signifie que nous savons qu'un événement s'est produit, mais nous ne savons pas exactement quand il s'est produit. La plupart des données épidémiologiques sont "doublement censurées" car il existe une incertitude sur les heures des événements primaires et secondaires. Le fait de ne pas tenir compte de la censure peut entraîner des estimations biaisées de l'écart-type du délai ([Park et al., en cours](https://github.com/parksw3/epidist-paper)). Différentes approches d'échantillonnage peuvent générer des biais dus à la censure à gauche et à droite dans l'estimation de l'intervalle sériel, ce qui peut propager le biais à l'estimation de la période d'incubation et du temps de génération ([Chen et al., 2022](https://www.nature.com/articles/s41467-022-35496-8/figures/2)).

## Risques relatifs

## Rapport de risque (RR)

Le Rapport de Risque (RR), également appelé Risque Relatif, compare le risque de développer un événement de santé (maladie, décès) entre deux groupes. Il le fait en divisant le risque (proportion d'incidence, taux d'attaque) dans le groupe 1 par le risque (proportion d'incidence, taux d'attaque) dans le groupe 2. Les deux groupes sont généralement différenciés par des facteurs démographiques tels que le sexe ou par l'exposition à un facteur de risque suspecté, par exemple, la consommation alimentaire ou le contact avec des cas suspects.

La formule du Rapport de Risque (RR) est la suivante :

Risque de maladie (proportion d'incidence, taux d'attaque) dans le groupe d'intérêt primaire / Risque de maladie (proportion d'incidence, taux d'attaque) dans le groupe de comparaison

De cela, on peut conclure que :
* Si le RR est égal à 1, cela indique un risque identique entre les deux groupes.
* Si le RR est supérieur à 1, cela indique un risque plus élevé pour le groupe numérateur, généralement le groupe exposé.
* Si le RR est inférieur à 1, cela indique un risque diminué pour le groupe exposé, ce qui suggère que l'exposition peut en fait protéger contre l'apparition de la maladie.

Exemple :
* Lors d'une épidémie de virus respiratoire chez des écoliers, 28 élèves de l'école primaire sur 157 ont développé la tuberculose, contre 4 élèves du lycée sur 137. En définissant l'exposition comme le fait d'être un élève de l'école primaire, et la non-exposition comme le fait d'être un élève du lycée, nous avons :

| | Malade | Sain | Total |
|---|---|---|---|
| **Élèves du primaire** | 30 | 120 | 150 |
| **Élèves du secondaire** | 5 | 135 | 140 |
| Total | 35 | 265 | 290 |

Pour calculer le RR, calculez d'abord le taux d'attaque pour chaque groupe :
Taux d'attaque pour les exposés (Tuberculose École Primaire) = $\frac{30}{150} = 0.2 = 20\%$
Taux d'attaque pour les non-exposés (Tuberculose École Secondaire) = $\frac{5}{140} = 0.036 = 3.6\%$

Ainsi, le RR est simplement le rapport de ces deux risques :
$RR = \frac{20}{3.6} = 5.5$

Par conséquent, les élèves du primaire étaient 5,5 fois plus susceptibles de développer la tuberculose que les élèves du secondaire.

## Odds Ratio (OR)

Dans les études cas-témoins, l'**Odds Ratio (OR)** est utilisé pour comparer les chances d'exposition à un facteur de risque entre les cas (individus atteints de la maladie) et les témoins (individus sans la maladie). Cette mesure permet d'évaluer l'association entre l'exposition et la maladie.

Chances d'exposition chez les cas / Chances d'exposition chez les témoins

Il est important de noter que le résultat n'est pas une probabilité.

De plus, si ce nombre est :
* Égal à 1, cela signifie que la fréquence de l'événement est égale chez les exposés et les non-exposés, ce qui signifie qu'il n'y a pas d'association entre l'exposition et l'événement.
* Supérieur à 1, cela signifie que la fréquence de l'événement est plus élevée chez les exposés que chez les non-exposés, ce qui signifie que l'exposition est un facteur de risque.
* Inférieur à 1, cela signifie que la fréquence de l'événement est plus faible chez les exposés que chez les non-exposés, et dans ce cas, cela est interprété comme l'exposition étant un facteur protecteur.

Exemple :
Après une conférence académique, une épidémie de vomissements et de diarrhée a été signalée après le déjeuner. Le déjeuner comprenait des sandwichs. L'affluence totale était de 100 personnes ; dont 50 participants sont tombés malades. Lors de l'enquête initiale, il a été constaté qu'un total de 60 personnes ont déclaré avoir mangé le sandwich du déjeuner. Parmi ces 60, 35 sont tombées malades, et sur les 40 qui n'ont pas mangé le sandwich, 15 ont signalé des symptômes de maladie. En résumé :

| | Malade (Cas) | Sain (Témoins) | Total |
|---|---|---|---|
| **Exposé (A mangé le sandwich)** | 35 | 25 | 60 |
| **Non exposé (N'a pas mangé le sandwich)** | 15 | 25 | 40 |
| Total | 50 | 50 | 100 |

En calculant, nous avons que :
Chances d'exposition chez les cas : $\frac{35}{15} = 2.33$
Chances d'exposition chez les témoins : $\frac{25}{25} = 1$
Odds Ratio d'exposition (OR) $= \frac{2.33}{1} = 2.33$

Cela signifie que les chances de présenter les symptômes de maladie signalés en raison de la consommation de sandwich sont 2,33 fois plus élevées que les chances de développer ces symptômes sans avoir consommé le sandwich. Cela peut être interprété comme le fait d'avoir mangé le sandwich étant un facteur de risque.

## Enquête sur les épidémies

## Courbe épidémique

La **courbe épidémique** est une représentation graphique qui montre la distribution des cas de maladie au fil du temps lors d'une épidémie. C'est un outil fondamental en épidémiologie pour comprendre la dynamique d'une épidémie, identifier son origine, évaluer l'efficacité des interventions et prédire son évolution.

Caractéristiques de la courbe épidémique :
* **Axe des X (horizontal)** : Représente le temps (jours, semaines, mois, etc.).
* **Axe des Y (vertical)** : Représente le nombre de nouveaux cas de maladie dans chaque unité de temps.
* **Motifs** : La forme de la courbe peut varier en fonction de la manière dont la maladie est transmise et des caractéristiques de l'épidémie.

Types de courbes épidémiques :
1.  **Courbe à source ponctuelle (ou exposition à une source commune)** :
    * **Caractéristiques** : Présente un pic prononcé suivi d'un déclin rapide. Elle se produit généralement lorsque tous les cas sont exposés à une source commune d'infection à un seul moment ou dans une courte période de temps.
    * **Exemple** : Une épidémie d'intoxication alimentaire lors d'un événement social où tous les cas sont exposés à des aliments contaminés en même temps.
2.  **Courbe à source commune persistante** :
    * **Caractéristiques** : La courbe montre un plateau prolongé suivi d'une baisse, indiquant une exposition continue ou intermittente à une source commune d'infection.
    * **Exemple** : Une épidémie de choléra dans une communauté due à une contamination de l'approvisionnement en eau qui n'est pas immédiatement corrigée.
3.  **Courbe de transmission de personne à personne** :
    * **Caractéristiques** : Montre plusieurs pics successifs, reflétant la transmission de la maladie d'une personne à une autre. Chaque pic représente une nouvelle génération de cas.
    * **Exemple** : Une épidémie de grippe saisonnière, où le premier cas infecte d'autres personnes, qui à leur tour en infectent davantage, créant plusieurs pics au fil du temps.

## Endémicité

Implique des niveaux de transmission relativement stables reflétés par une incidence de cas plus ou moins constante. Cela ne signifie pas qu'il n'y a pas de changements soudains d'incidence, avec des périodes de transmission élevée, dues, par exemple, à des phénomènes saisonniers ou à des changements soudains du nombre de susceptibles (immigrants, par exemple). La frontière entre endémicité et épidémie est très difficile à établir, à l'exception des maladies importées, où le niveau endémique précédent était nul. Les endémies peuvent connaître des changements temporaires dans leur manifestation, qui peuvent être décrits comme des cycles.

## Épidémicité

Implique une instabilité dans la transmission, des niveaux changeants qui peuvent varier de zéro à des millions de cas.

## Épidémie (Outbreak)

Terme couramment utilisé pour décrire l'apparition soudaine et inattendue de cas d'une maladie.

## Cycles saisonniers

Se produisent liés aux saisons (hiver et virus respiratoires dans les pays tempérés) ou aux cycles climatiques (saison des pluies et paludisme sous les tropiques).

## Pandémie

Désigne les épidémies de grande ampleur en termes d'étendue géographique et de durée prolongée, comme la grippe, le choléra ou le SIDA à notre époque.

## Concepts de base

## Infection vs Maladie

L'infection est le processus par lequel un agent infectieux pénètre, se développe et se multiplie dans l'organisme d'une personne ou d'un animal. Pendant l'infection, un individu peut être infectieux, c'est-à-dire capable de transmettre l'agent à d'autres, même s'il ne présente pas de symptômes.

La maladie, quant à elle, est l'état dans lequel une infection entraîne le développement de symptômes cliniques. Un individu atteint de la maladie est généralement infectieux, mais il peut y avoir des périodes où il est infectieux avant de montrer des symptômes.

Exemple : Une personne peut être infectée par le virus du VIH et être infectieuse sans présenter de symptômes pendant des années. Cependant, lorsqu'elle développe le SIDA, elle présente des symptômes graves. Il est crucial de comprendre que l'agent infectieux (comme le VIH) est transmis, pas les symptômes de la maladie (comme le SIDA).

Cette distinction est très importante en épidémiologie des maladies infectieuses.

## Agent pathogène

Un **agent pathogène** est un micro-organisme qui peut causer des maladies chez un organisme hôte. Ceux-ci peuvent être subdivisés en vivants et non-vivants. Les vivants comprennent les bactéries, comme *Mycobacterium tuberculosis* qui cause la tuberculose ; les parasites, comme *Plasmodium falciparum* qui cause le paludisme ; et les champignons, comme *Candida albicans* qui cause la candidose. Bien que les virus, comme le SARS-CoV-2 qui cause la COVID-19, soient également des agents pathogènes, ils ne sont pas considérés comme vivants car ils ne peuvent pas effectuer de processus métaboliques par eux-mêmes et nécessitent une cellule hôte pour se répliquer. Tous ces agents pathogènes envahissent, se répliquent et endommagent les tissus de l'hôte, provoquant des maladies. Leur étude est fondamentale en épidémiologie pour développer des stratégies efficaces de prévention, de contrôle et de traitement des maladies infectieuses.

## Cas

Un **cas** est une personne identifiée comme souffrant d'une maladie ou d'un événement d'intérêt épidémiologique, soit par diagnostic clinique, tests de laboratoire ou critères épidémiologiques. Les cas peuvent être classés comme suit :
* **Cas suspect** : Individu qui présente des symptômes compatibles avec une maladie mais qui n'a pas encore été confirmé par des tests de laboratoire.
* **Cas probable** : Individu qui présente des signes et des symptômes d'une maladie et qui répond à des critères épidémiologiques spécifiques, mais qui manque de confirmation en laboratoire.
* **Cas confirmé** : Individu diagnostiqué avec une maladie par des tests de laboratoire spécifiques.
* **Cas index (cas primaire)** : Le premier cas détecté ou signalé lors d'une épidémie.
* **Cas secondaire** : Un cas qui se produit à la suite de la transmission du cas index ou primaire.

## Hôte

Une personne ou un animal vivant (mammifère, reptile, oiseau, etc.), qui, dans des circonstances naturelles, permet la subsistance ou l'hébergement d'un agent infectieux. Les insectes arthropodes ne sont pas considérés comme des hôtes.

## Vecteur

Un vecteur peut être défini comme un organisme vivant capable de transmettre un agent infectieux entre d'autres organismes vivants ([OMS, 2020](https://www.who.int/news-room/fact-sheets/detail/vector-borne-diseases)). Cependant, cette définition peut varier selon les critères utilisés. Certains des critères utilisés incluent l'approche anthropocentrique (maladies transmises à l'homme), l'approche micropredator (qui met l'accent sur l'ingestion de fluides de l'hôte par contact direct), l'approche des arthropodes hématophages (arthropodes qui se nourrissent de sang), l'approche basée sur la morbidité (transmission de maladies à l'hôte), l'approche basée sur la mobilité (vecteur à haute mobilité) et l'approche de la transmission séquentielle de l'infection (transmission mutuelle de l'infection entre le vecteur et l'hôte) ([Wilson et al., 2017](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5352812/#RSTB20160085C19)). Selon les points sélectionnés, la définition peut varier et englober des êtres vivants divers. De plus, la transmission peut être une simple fonction de transport mécanique (Transmission Mécanique), ou l'agent infectieux peut se multiplier ou se développer à l'intérieur du vecteur (Transmission Biologique).

Exemple : Le moustique *Aedes aegypti* est un vecteur du virus de la Dengue.

## Porteur

Une personne (ou un animal) qui héberge un agent infectieux spécifique sans en présenter de symptômes cliniques ou de signes, et qui constitue une source potentielle d'infection pour les humains.

## Réservoir

Tout être humain, animal, arthropode, plante, sol, ou matière inanimée, ou combinaison de ceux-ci, où un agent infectieux vit et se multiplie normalement et dont il dépend pour sa survie, se reproduisant de telle manière qu'il peut être transmis à un hôte susceptible.

## Taille minimale de la communauté (TMC)

Elle est définie comme la taille minimale d'une population fermée au sein de laquelle un agent pathogène non zoonotique de personne à personne peut persister indéfiniment. En d'autres termes, c'est la taille totale de la population (d'individus susceptibles et infectés, ou autres) nécessaire pour maintenir une épidémie une fois qu'elle est apparue.

## Super-propagation

Un événement au cours duquel une maladie infectieuse se propage beaucoup plus que d'habitude. De même, un individu qui infecte de manière disproportionnée un grand nombre d'individus et qui est susceptible de déterminer la vitesse et la gravité d'une épidémie est appelé un super-propagateur.

## Transmission vectorielle

La transmission vectorielle signifie qu'une infection peut être transmise d'un vecteur (par exemple, les moustiques) à l'homme. Des exemples de maladies à transmission vectorielle incluent le paludisme et la dengue. L'Organisation mondiale de la Santé dispose d'une [fiche d'information](https://www.who.int/news-room/fact-sheets/detail/vector-borne-diseases) sur les maladies à transmission vectorielle avec des informations clés et une liste de celles-ci en fonction de leur vecteur.

## Excrétion virale

L'**excrétion virale** est le processus par lequel un virus est libéré de l'organisme infecté dans l'environnement, où il peut potentiellement infecter d'autres individus. Ce phénomène est fondamental dans la transmission des maladies virales, car il détermine quand et comment une personne infectée peut être contagieuse.

## Pathogénicité

La **pathogénicité** est la capacité d'un agent infectieux, tel qu'un virus, une bactérie, un champignon ou un parasite, à provoquer une maladie chez un hôte. Cette capacité dépend de plusieurs facteurs inhérents à l'agent infectieux et à son interaction avec l'hôte. La pathogénicité est évaluée qualitativement, c'est-à-dire si un micro-organisme est capable ou non de causer une maladie.

Caractéristiques de la pathogénicité :
* **Capacité à causer des maladies** : Tous les micro-organismes ne sont pas pathogènes ; la pathogénicité indique si un organisme peut causer une maladie dans des conditions normales.
* **Mécanismes de pathogénicité** : Inclut divers processus biologiques qui permettent à l'agent infectieux d'envahir et de nuire à l'hôte, tels que l'adhésion aux cellules hôtes, l'invasion tissulaire, l'évasion du système immunitaire et la production de toxines.

## Virulence

La **virulence** est une mesure quantitative de la gravité de la maladie causée par un agent infectieux. Elle représente l'intensité de la pathogénicité d'un micro-organisme, c'est-à-dire sa capacité non seulement à infecter mais aussi à causer des dommages significatifs à l'hôte. Souvent, la virulence est évaluée en termes de taux de mortalité, de gravité des symptômes et d'impact sur la santé de l'hôte.

Caractéristiques de la virulence :
* **Gravité de la maladie** : Quantifie les dommages qu'un agent pathogène peut causer à l'hôte, y compris la gravité des symptômes et le taux de mortalité.
* **Facteurs de virulence** : Molécules et mécanismes qui permettent à l'agent pathogène d'envahir l'hôte, d'échapper à son système immunitaire et de causer des dommages. Ceux-ci incluent les toxines, les enzymes, les protéines d'adhésion et les mécanismes d'évasion immunitaire.

## Résistance naturelle

La **résistance naturelle** à un agent pathogène fait référence à la capacité inhérente d'un organisme à éviter l'infection ou à combattre un agent infectieux sans avoir besoin d'une exposition préalable, d'une vaccination ou d'un traitement. Cette résistance peut être le résultat de diverses caractéristiques biologiques et génétiques de l'hôte qui empêchent l'entrée, la réplication ou la propagation de l'agent pathogène.

Caractéristiques de la résistance naturelle :
* **Inhérente** : C'est une caractéristique innée de l'organisme, présente sans avoir besoin d'une exposition préalable à l'agent pathogène.
* **Génétique** : Souvent, la résistance naturelle est déterminée par des facteurs génétiques qui peuvent varier d'un individu à l'autre et d'une population à l'autre.
* **Spécifique à l'agent pathogène** : La résistance naturelle peut être spécifique à certains agents pathogènes tandis que d'autres peuvent ne pas être affectés.

Exemple : Dans des études menées en Afrique subsaharienne, il a été observé que les populations avec un pourcentage élevé d'individus Duffy-négatifs ont une très faible incidence d'infections par *Plasmodium vivax*. En revanche, dans les régions d'Asie et d'Amérique du Sud, où la plupart des gens sont Duffy-positifs, le paludisme à *Plasmodium vivax* est plus courant.

## Infestation

Terme utilisé pour un hôte affecté par des ectoparasites, les puces par exemple. Également pour désigner l'infestation par des insectes ou des réservoirs dans les maisons ou les lieux (la maison est infestée de punaises de lit, la ville est infestée de rats, le taux d'infestation est de 10 %).

## Infection patente

Est la période pendant laquelle l'agent infectieux n'a pas encore produit de signes ou de symptômes, mais est déjà détectable par certains moyens chez l'hôte.

## Infection latente ou subclinique

L'agent infectieux est présent chez l'hôte, mais il n'y a aucune indication de sa présence. Cet état est très difficile à différencier de l'incubation chez l'hôte.

## Malade

L'hôte présente des signes ou des symptômes pathologiques.

## Porteur

Est un état infectieux prolongé, avec élimination persistante de l'agent infectieux. Il peut être un porteur malade, un porteur convalescent ou un porteur sain.

## Immunisé

Possède une protection active ou passive, à médiation cellulaire et/ou humorale contre l'infection.

## Immunité active

Immunité due à une exposition antérieure aux antigènes de l'agent ou similaires.

## Immunité passive

Immunité due au transfert d'anticorps, maternels ou d'autre origine.

## Gamme d'hôtes

Les espèces d'organismes naturellement susceptibles à un certain agent infectieux.

## Réservoir

Espèces ou populations capables de maintenir un certain agent infectieux dans la nature.

## Hôte définitif

Celui chez lequel se déroule la reproduction sexuelle de l'agent, lorsqu'il a une phase sexuelle obligatoire dans son cycle de vie. Cela se produit chez de nombreux helminthes et protozoaires.

## Hôte intermédiaire

Lorsque le cycle de vie implique deux espèces d'hôtes différentes, ce terme décrit l'hôte chez lequel se déroule la phase de reproduction asexuée.

## Hôte amplificateur

Une espèce hôte qui développe des épidémies périodiques par un certain agent, et qui génère une augmentation de la taille de la population de l'agent suffisamment importante pour se propager à d'autres espèces non habituellement exposées à cet agent.

## Hôte cul-de-sac

Ces espèces ou espèces dont les individus sont infectés mais ne sont pas fonctionnellement infectieux, et ne transmettent donc pas l'infection.

## Durée de l'infectiosité

Est directement liée au temps pendant lequel l'hôte infecté excrète des quantités considérables de l'agent infectieux.

## Rechute ou recrudescence

Implique la réapparition de signes cliniques après une période de maladie inapparente ou subclinique.

## Transmission verticale

Implique le transfert direct d'un agent infectieux d'un parent à la progéniture, soit transplacentaire, soit transovarien.

## Transmission horizontale

Désigne le transfert direct de l'agent pathogène par une personne autre que les parents.


# RÉFÉRENCES

-   Alzate, A. (1996). Conceptos básicos de enfermedades infecciosas.
    Boletín SIEI, 2(2), 2-5

-   Cambridge English Dictionary. (n.d.). Shedding. En Cambridge English
    Dictionary. Récupéré de <https://dictionary.cambridge.org>

-   Epiverse-Trace. (n.d.). Glossary. Récupéré de
    <https://epiverse-trace.github.io/tutorials-late/reference.html#glossary>

-   Glosario epidemiológico. Gobierno de
    Mexico. <https://www.insp.mx/nuevo-coronavirus-2019/glosario-epidemiologico.html> 

-   [Hart, William S., Elizabeth Miller, Nick J. Andrews, Pauline
    Waight, Philip K. Maini, Sebastian Funk, and Robin N.
    Thompson. 2022. "Generation Time of the Alpha and Delta SARS-CoV-2
    Variants: An Epidemiological Analysis." The Lancet Infectious
    Diseases 22 (5): 603--10.](http://paperpile.com/b/uKZiEn/PspE)

-   Holmdahl, I., & Buckee, C. (2020). COVID-19 epidemic prediction and
    the impact of public health interventions: A review of COVID-19
    epidemic models. ScienceDirect. Récupéré de
    <https://www.sciencedirect.com>

-   Keeling, M. J., & Rohani, P. (2008). A primer on stochastic epidemic
    models: Formulation, numerical simulation, and analysis.
    ScienceDirect. Récupéré de <https://www.sciencedirect.com>

-   Kucharski, A. J., & Edmunds, W. J. (2018). Key data for outbreak
    evaluation: Building on the Ebola experience. Philosophical
    Transactions of the Royal Society B: Biological Sciences. Récupéré
    de <https://royalsocietypublishing.org>

-   Lloyd-Smith, J. O., Schreiber, S. J., Kopp, P. E., & Getz, W. M.
    (2005). Superspreading and the effect of individual variation on
    disease emergence. Nature. Récupéré de <https://www.nature.com>

-   Math Insight. (n.d.). An introduction to ordinary differential
    equations. Récupéré de <https://mathinsight.org>

-   Milwid, R. (2016, 28 septembre). Toward Standardizing a Lexicon of
    Infectious Disease Modeling Terms.
    Frontiers. <https://www.frontiersin.org/articles/10.3389/fpubh.2016.00213/full> 

-   Nishiura, H., Linton, N. M., & Akhmetzhanov, A. R. (2020). Serial
    interval of novel coronavirus (COVID-19) infections. International
    Journal of Infectious Diseases. Récupéré de
    <https://www.ijidonline.com>

-   Organización Panamericana de la Salud. COVID-19, GLOSARIO SOBRE
    BROTES Y EPIDEMIAS. PAHO.
    <https://www.paho.org/es/documentos/covid-19-glosario-sobre-brotes-epidemias-recurso-para-periodistas-comunicadores> 

-   Organización Panamericana de la Salud. Módulo de Principios de
    Epidemiología para el Control de Enfermedades (MOPECE) Segunda
    Edición Revisada. Unidad 5. Investigación epidemiológica de campo:
    aplicación al estudio de brotes.
    <https://www3.paho.org/hq/index.php?option=com_content&view=article&id=9161:2013-mopece-training-modules-epidemiology&Itemid=0&lang=es#gsc.tab=0> 

-   Park, S. (n.d.). Epidist-paper. GitHub. Récupéré de
    <https://github.com>

-   Wellcome Open Research. (n.d.). Estimating the overdispersion in
    COVID-19. Récupéré de <https://wellcomeopenresearch.org>

-   World Health Organization. (n.d.). Vector-borne diseases. Récupéré
    de <https://www.who.int>

-   [Wu, Yu, Liangyu Kang, Zirui Guo, Jue Liu, Min Liu, and Wannian
    Liang. 2022. "Incubation Period of COVID-19 Caused by Unique
    SARS-CoV-2 Strains: A Systematic Review and Meta-Analysis." JAMA
    Network Open 5 (8): e2228008.](http://paperpile.com/b/uKZiEn/yGCE)
