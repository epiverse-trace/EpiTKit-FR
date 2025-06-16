---
title: Banque de questions fréquemment posées et d'erreurs
date: '2025-06-16'
output:
  html_document:
    self_contained: true
  pdf_document: default
  word_document: default
image: ~
licenses: CC-BY
topics:
- R
- Rstudio
- français
categories: practicals
always_allow_html: true
teaching: 80
exercises: 8
---

::: questions

- Avez-vous des difficultés avec le code dans R ?

:::

::: objectives

- Dans ce document, vous trouverez quelques-unes des questions fréquemment posées et des erreurs dans l'exécution du code R.
:::

## Banque de questions

### RTools est-il nécessaire ?

Il existe plusieurs problèmes courants dans R qui peuvent nécessiter l'installation de Rtools.

1. Installation de paquets nécessitant une compilation : certains paquets R doivent être compilés à partir du code source, ce qui nécessite des outils de compilation fournis par Rtools.

2. Dépendances C, C++ ou Fortran : Si vous souhaitez installer des paquets qui dépendent d'un code écrit en C, C++ ou Fortran, vous aurez besoin de Rtools pour compiler ces composants.

3. Erreurs de compilation : Si vous rencontrez des erreurs lors de l'installation de paquets mentionnant des problèmes de compilation, Rtools peut résoudre ces problèmes en fournissant les outils nécessaires.

4. Développement de paquets personnalisés : si vous développez votre propre paquetage R et que vous devez compiler le code source, Rtools est essentiel pour ce processus.

### Comment installer RTools ?

*Avant de commencer, vérifiez que vous disposez des droits d'administrateur sur l'ordinateur ou le portable.*

Installation de Rtools

L'installation de Rtools dépend du système d'exploitation que vous utilisez.

### Windows

1. Vérifiez la version de R dont vous disposez :

Dans la console R, tapez et exécutez cette commande :


``` r
sessionInfo()
```

``` output
R version 4.5.0 (2025-04-11)
Platform: x86_64-pc-linux-gnu
Running under: Ubuntu 22.04.5 LTS

Matrix products: default
BLAS:   /usr/lib/x86_64-linux-gnu/blas/libblas.so.3.10.0 
LAPACK: /usr/lib/x86_64-linux-gnu/lapack/liblapack.so.3.10.0  LAPACK version 3.10.0

locale:
 [1] LC_CTYPE=C.UTF-8       LC_NUMERIC=C           LC_TIME=C.UTF-8       
 [4] LC_COLLATE=C.UTF-8     LC_MONETARY=C.UTF-8    LC_MESSAGES=C.UTF-8   
 [7] LC_PAPER=C.UTF-8       LC_NAME=C              LC_ADDRESS=C          
[10] LC_TELEPHONE=C         LC_MEASUREMENT=C.UTF-8 LC_IDENTIFICATION=C   

time zone: UTC
tzcode source: system (glibc)

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

loaded via a namespace (and not attached):
[1] compiler_4.5.0 tools_4.5.0    yaml_2.3.10    knitr_1.49     xfun_0.51     
[6] renv_1.1.4     evaluate_1.0.3
```

**Vous obtiendrez des informations similaires à celles-ci. Dans ce cas, la version est 4.5.0.**

2. Visitez la page RTools sur le CRAN dans le navigateur de votre choix :
  <https://cran.r-project.org/bin/windows/Rtools/>et sélectionnez la version de Rtools qui correspond à la version actuelle de R que vous avez sur votre machine et à l'architecture de votre ordinateur.
  Vous pouvez également cliquer sur l'un des liens suivants pour télécharger le programme d'installation :

\\

| Pour les versions de R...    | Installez : |
| ---------------------------- | ----------- |
| À partir de la version 4.5.0             | [RTools 4.5](https://cran.r-project.org/bin/windows/Rtools/rtools45/rtools.html)         |
| À partir de la version 4.4.0 | [RTools 4.4](https://cran.r-project.org/bin/windows/Rtools/rtools44/rtools.html)            |
| À partir de la version 4.3.0      | [RTools 4.3](https://cran.r-project.org/bin/windows/Rtools/rtools43/rtools.html)            |
| À partir de la version 4.2.  | [RTools 4.2](https://cran.r-project.org/bin/windows/Rtools/rtools42/rtools.html)            |
| Entre 4.0.0 et 4.1.3         | [RTools 4.0](https://cran.r-project.org/bin/windows/Rtools/rtools40.html)            |
| Avant la version 4.0.0       | [anciennes versions de RTools](https://cran.r-project.org/bin/windows/Rtools/history.html)            |

3. Sur la page de téléchargement, recherchez la phrase : "***peut être installé à partir du site***"et cliquez sur **[*Installateur Rtools44*](https://cran.r-project.org/bin/windows/Rtools/rtools44/files/rtools44-6335-6327.exe)** ou dans la version que vous avez sélectionnée **ci-dessus *Installateur RtoolsXX***.

![](fig/rtools.png)

4. Attendez la fin du téléchargement et exécutez le fichier.

5. Cliquez sur "*Suivant*" o "*Suivant*" pour toutes les options affichées à l'écran.

### Mac

Sur Mac, il vous suffit d'installer Xcode Command Line Tools.

1. Cliquez sur Spotlight Search en haut à droite de l'écran, puis recherchez "Terminal".

2. Ouvrez un terminal ou une ligne de commande sur votre machine.

3. Dans le terminal, copiez et collez la commande suivante :
  `xcode-select –install`

4. Vous devrez probablement fournir votre mot de passe pour installer le logiciel.

5. Suivez les instructions du terminal et attendez la fin de l'installation.

Vous pouvez également le faire directement à partir de R comme expliqué dans cette vidéo : [Installation à l'aide de R](https://www.youtube.com/watch?v=_fckF0fefXQ&t=5s)

### [Comment installer un package ou une "bibliothèque" dans R ?]{#instr}

Pour installer un paquetage dans R, vous pouvez le faire via :

- Nous vous recommandons de le faire par le biais de la fonction :


``` r
install.packages("package")
```

Certains paquets qui sont en phase de développement peuvent être installés à partir de la dernière version sur github ou d'autres emplacements en utilisant des remotes ou des paquets pak.

- Une autre option consiste à utiliser la fonction require :


``` r
if (!require("package")) {
  install.packages("package")
}
```

Cette option est utile car elle installe le paquet s'il n'est pas déjà installé.
Elle peut être combinée avec remotes ou pak

- Utilisez l'interface RStudio :

  1. Cliquez sur le bouton `Packages`

  2. Cliquez sur le bouton `Install`

  3. Saisissez le nom du (des) paquet(s) à installer.

  4. Appuyez sur le bouton `Install`.

### [Comment utiliser une fonction ?]{#funcr}

Si la fonction appartient à un paquetage R, vous pouvez procéder de deux manières :

- Appelez le nom du paquetage R et mettez deux fois deux points. `(::)` puis appelez le nom de la fonction. Vous devez maintenant remplir les arguments


``` r
package::nom_de_la_fonction(arguments)
```

- Chargez le paquetage R avec `library`:


``` r
library("package")
```

et une fois chargé.
Appelez le nom de la fonction et remplissez les arguments.


``` r
nom_de_la_fonction(arguments)
```

Il est important que le paquetage ait été installé au préalable.
En cas de doute, rendez-vous sur [Comment installer un paquetage dans R ?](instr)

- Si la fonction a été créée par vous et se trouve dans l'environnement global :

Appelez simplement la fonction par son nom et fournissez les arguments nécessaires :


``` r
nom_de_la_fonction(arguments)
```

### Comment charger un paquet ou une "bibliothèque" ?

Voici quelques options pour télécharger un paquet :

- Il est recommandé d'utiliser la fonction library :


``` r
library("package")
```

- Utiliser l'interface RStudio :

  1. Allez dans la section en bas à droite de l'interface RStudio. `Packages`

  2. Cliquez sur la case devant chaque fonction, ce qui activera la fonction. `library`.

### Si je charge les bibliothèques, dois-je les charger chaque fois que j'utilise la fonction ?

Non, vous ne devez les charger qu'une seule fois par session R.
Cependant, si vous fermez votre RStudio ou ouvrez un nouveau projet, cela compte comme une nouvelle session et vous devez donc les charger à nouveau pour qu'elles fonctionnent.

### Puis-je désactiver une bibliothèque que j'ai déjà chargée sans redémarrer R ?

Oui, c'est possible grâce à deux options :

- Utiliser la fonction `detach`


``` r
detach("package", unload = TRUE)
```

- Utiliser l'interface RStudio :

  1. Allez dans la section en bas à droite de l'interface RStudio. `Packages`

  2. Cliquez sur la case devant chaque fonction (si la case est cochée, le paquet est chargé ; si la case est vide, le paquet n'est pas chargé), ce qui activera la fonction. `detach`. ***Avertissement* En appuyant sur le symbole x à côté du paquet, vous le désinstallez.**

### L'objet ou la fonction n'a pas été créé

Cela peut se produire pour plusieurs raisons :

- **Exécution incomplète du code** La raison la plus fréquente est que le code n'a pas été exécuté partiellement ou complètement. Veillez à exécuter l'intégralité du script afin que toutes les lignes de code soient exécutées dans le bon ordre. Pour créer l'objet, assurez-vous d'avoir effectué l'une de ces deux actions :

1. écrire le code dans la console et l'exécuter (en appuyant sur `Enter`)

2. ou dans le script RMarkdown ou Chunck, appuyez sur `Control` + `Enter` sous Windows ou `Command` + `Enter` sur Mac.

Si l'objet ou la fonction a été créé correctement, il apparaîtra dans l'environnement global (*Environnement*) situé dans la zone supérieure droite.

- Un paquetage requis est manquant : vérifiez que tous les paquetages ou bibliothèques requis sont chargés au début du script.

- Erreurs dans le code : vérifiez qu'aucune erreur n'empêche le code de s'exécuter correctement. Lors de l'exécution du code dans la console, certaines alertes d'erreur apparaîtront.

::: callout

## Recommandation

Regardez toujours la console pour vérifier si :

1. Le code a été exécuté avec succès. S'il ne s'est pas exécuté, vous pouvez le relancer.
2. Si une commande est toujours en cours d'exécution et que vous voyez le symbole rouge **arrêt**. Dans ce cas, attendez que R termine le processus avant d'exécuter d'autres commandes.
3. Si une erreur s'est produite. Examinez les erreurs ou les avertissements, car ils peuvent vous donner des indications sur la manière de résoudre le problème.

:::

### Je ne vois pas le résultat de mon code

Cela peut arriver pour plusieurs raisons :

- Si j'enregistre le résultat en utilisant le symbole d'allocation (c'est-à-dire `nombre <- "Laura"`). Celui-ci apparaîtra dans l'environnement global (zone en haut à droite) et ne sera pas exécuté sur la console à moins que l'objet ne soit appelé, c'est-à-dire

  1. le nom de l'objet est affiché dans la console et exécuté (en appuyant sur la touche `Enter`)

  2. ou que dans le script RMarkdown ou Chunck, vous appuyez sur `Control + Enter` sous Windows ou `Command + Enter` sur Mac.

- Une bibliothèque requise est manquante. Vérifiez que toutes les bibliothèques requises sont chargées au début du script.

- Le code contient des erreurs. Vérifiez qu'il n'y a pas d'erreurs qui empêchent le code de s'exécuter correctement. Lorsque vous exécutez le code dans la console, vous verrez des alertes d'erreur que le code peut avoir.

- Le script ne s'est pas exécuté complètement. Veillez à exécuter l'intégralité du script afin que toutes les lignes de code soient exécutées dans le bon ordre.

### Erreurs courantes lors de l'utilisation de `ggplot`

- Syntaxe incorrecte :

  1. Utilisez `++` au lieu de `+` pour concaténer des fonctions.

  2. Il peut également arriver que la fonction `+` se trouve sur la ligne inférieure, il est important de noter que pour concaténer des fonctions, il doit se trouver à la fin de la ligne précédant celle que vous voulez concaténer.


- Ne spécifiez pas l'esthétique :

  1. Ne pas inclure `aes()`.
  2. Ne pas définir `aes()` correctement, par exemple en n'indiquant pas x ou y.
  3. Bien que l'aes puisse dans certains cas se trouver dans la partie initiale, la géométrie ou être divisée en sections, il est essentiel qu'elle soit toujours présente.

- Données non présentes :

La colonne mentionnée dans aes() n'existe pas dans le jeu de données.
Utilisez le mauvais nom, n'oubliez pas que R est sensible à la casse.`VariableX` est différent de `variableX` ou `variablex`.

- Manque de librairies :

Avant de travailler avec `ggplot` n'oubliez pas de charger la bibliothèque avec `library`:


``` r
library(ggplot2)
```

- Erreurs dans `geom`:

Sélectionner la mauvaise géométrie pour le type de données à représenter.

### `filter` ne fonctionne pas

Cela peut se produire pour plusieurs raisons :

- Le paquet `dplyr` n'est pas chargé. Veillez à inclure `library(dplyr)` o `library(tidyverse)` dans votre script et de l'exécuter à chaque nouvelle session.

- Il existe des conflits de noms de fonctions avec d'autres paquets. Utilisez `dplyr::filter()` pour spécifier la fonction que vous souhaitez utiliser `filter` fonction de `dplyr`.

- Il se peut que les données ne soient pas dans le format attendu. Vérifiez que la colonne que vous filtrez existe et qu'elle possède les valeurs appropriées.

`filter` Acceptez des conditions logiques pour la sélection des lignes.
Voyons quelques exemples :

\- Valeurs spécifiques :


``` r
covid19 %>% filter(eta_du_cas == "deces")
```

- Plages de valeurs :


``` r
covid19 %>% filter(date >= "2020-01-01" & date <= "2020-12-31")
```

\- Conditions multiples :


``` r
covid19 %>% filter(eta_du_cas == "deces" & pays == "Kenya")
```

\- Affections avec fonctions :


``` r
covid19 %>% filter(grepl("Kenya", pays))
```

Pour plus d'informations sur le filtrage, reportez-vous à la section [documentation](https://dplyr.tidyverse.org/reference/filter.html).

### Où se trouve l'objet que vous créez ?

Lorsqu'un objet est créé, il est stocké dans l'environnement global.
Vous pouvez voir l'environnement global dans l'interface R située en haut à droite.

### Le tuyau ne fonctionne pas `%>%`

Rappelez-vous les points suivants :

- Il est important de précharger une bibliothèque contenant le tuyau. Par exemple : `magrittr`, `dplyr`, `tidyr` o `purrr`.
- Le tuyau doit être placé à l'extrémité de la ligne à raccorder. Pas au début de la ligne raccordée :


### Comment éviter les accidents ? {#prevencion}

Lorsque vous allez enregistrer des modifications dans l'objet où est stocké le dataframe, il est conseillé de prendre quelques précautions pour éviter de perdre des informations :

- Créez une sauvegarde des données dans les objets :

o Faites des sauvegardes régulières pendant le processus.
Il est recommandé de faire une première copie pour éviter de recharger la base de données.
Après avoir effectué certains traitements, en particulier ceux qui prennent du temps, il est recommandé de créer des sauvegardes.
Vous pouvez en créer autant que vous le souhaitez.
Il est recommandé de créer des notes pour identifier chaque processus


- Créez une sauvegarde des données dans les fichiers :

o Comme pour l'enregistrement des objets, il est judicieux de sauvegarder sur le disque de l'ordinateur des données qui ont déjà fait l'objet d'un certain nombre de traitements.
Cela permet d'éviter que les données traitées ne soient sauvegardées en cas de plantage de la session ou d'arrêt de l'ordinateur.
La fréquence de stockage dépend de la personne qui effectue le traitement.


- Test avant stockage :

o Effectuez des tests sur les changements souhaités avant le stockage final.

o Exemple : si vous voulez transformer une variable en une variable numérique, avant de la stocker, et que vous obtenez en fin de compte `NAs` des changements non désirés dans les données, il est conseillé d'effectuer un test avant de les stocker, afin de voir si ces changements seront générés. `NAs`


- Créez des variables de sauvegarde :

o Parfois, lorsque nous allons transformer une variable, il est préférable d'en créer une nouvelle qui stocke le contenu de la transformation.
Cela évite le risque de perdre des informations lors de la transformation d'une variable.


- Attention au stockage :

o Ne stockez pas de tableaux ou d'objets transformés accidentellement.

o Par exemple, si nous créons un tableau pour voir si la variable a changé comme souhaité, puis réutilisons le code et ajoutons l'affectation vers l'avant, nous stockons le tableau et perdons l'information que l'objet contenait.


### Mon cadre de données a changé de façon inattendue

Lorsque nous avons des accidents avec nos données, certaines options sont possibles :

- Vérifier les dommages et voir s'ils sont réparables.
  Par exemple, le mauvais caractère a été modifié dans une chaîne de texte.

- Chargez les données à partir d'une sauvegarde.
  Si nous avons créé des sauvegardes du processus, nous pouvons éviter des temps de traitement trop longs.
  Parmi ces sauvegardes, on trouve les variables de sauvegarde ou les objets de sauvegarde (voir [Comment éviter les crashs ?](Banco_errores.Rmd#prevencion)).

### Utilisation de la fonction `rename`

1. Appeler la base de données


``` r
donees
```

2. Utiliser le tuyau`%>%` pour établir un lien avec la fonction de renommage

3. Appelez la fonction`rename` et tapez d'abord le nom de la nouvelle colonne, puis le nom de la colonne préexistante que vous voulez renommer


``` r
donees <- donees %>% rename(nouvelle = préexistante)
```

Sélectionner quelques lignes d'un groupe de données

1. Appeler la base de données


``` r
donees
```

2. Utiliser le tuyau`%>%` pour établir un lien avec la base de données `group_by`


``` r
datos %>% group_by(variable_grupo)
```

La fonction `group_by` crée des groupes de données en fonction d'une variable donnée, dans lesquels vous pouvez effectuer d'autres actions telles que la sélection des données dans l'en-tête de chaque groupe.

4. Utilisez ensuite la fonction comme dans cet exemple, nous pourrions utiliser`head` uniquement pour les données de l'en-tête de chaque groupe.


``` r
donees <- donees %>% group_by(variable) %>% head()
```

### Comment utiliser `summarise`?

1. Appelez la base de données


``` r
donees
```

2. Utiliser le tuyau`%>%`pour établir un lien avec le `summarise`


``` r
donees %>% summarise()
```

La fonction "summarise" ne peut pas être utilisée directement, elle doit donc être utilisée en conjonction avec un argument à l'intérieur, par exemple :

a. Obtenir la moyenne


``` r
donees %>%
  summarise(mean = mean(variable))
```

b. Obtenir l'écart-type


``` r
donees %>%
  summarise(sd = sd(variable))
```

Cette fonction peut être utilisée avec le pré-clustering (`group_by`) pour obtenir ces valeurs pour chaque groupe, par exemple,


``` r
donees %>%  group_by(pays) %>%
  summarise(
    mean = mean(variable),
    sd = sd(variable))
```

### Erreurs liées au groupe (`group_by` y `ungroup`)

- Une erreur très fréquente est que l'objet groupé est stocké (`group_by`), car l'action de dégroupage n'a pas été effectuée à la fin. Cela peut entraîner des erreurs telles que des calculs incorrects, des résumés par groupe au lieu de l'ensemble des données, ainsi que des problèmes lors d'opérations ultérieures sur l'ensemble de données. C'est pourquoi nous vous recommandons de toujours utiliser (`ungroup`) avant de stocker. Pour utiliser `ungroup()` il suffit de le mettre à la fin.


``` r
donnees <- donnees %>%
  group_by(categorie) %>%
  traitement_des_donnees(...) %>%
  ungroup()
```

Examinons un exemple d'erreur qui peut se produire si l'on ne procède pas au dégroupage :


``` r
library("tidyverse")
set.seed(123) # Pour la reproductibilité
# Exemple de dataframe
type_sanguin <- c("A", "B", "O", "AB")
rh <- sample(c("+", "-"), 10, replace = TRUE)
jour <- c(1:5)
f_battements <- sample(60:100, 200, replace = TRUE)
f_respiratoire <- sample(12:20, 200, replace = TRUE)
df <- data.frame(type_sanguin, rh, jour, f_battements, f_respiratoire)

# Résumé par colonnes
par_jour <- df %>%
  group_by(type_sanguin, rh, jour) %>%
  summarize(
    f_b = mean(f_battements),
    f_r = mean(f_respiratoire)
  )
```

Créons une variable contenant des identifiants uniques pour chaque ligne.


``` r
par_jour %>% mutate(id = row_number())
```

``` output
# A tibble: 20 × 6
# Groups:   type_sanguin, rh [8]
   type_sanguin rh     jour   f_b   f_r    id
   <chr>        <chr> <int> <dbl> <dbl> <int>
 1 A            +         1  76.3  15.2     1
 2 A            +         3  81.5  16.6     2
 3 A            +         4  81.2  15.6     3
 4 A            +         5  81    15.9     4
 5 A            -         2  78.3  16.2     1
 6 AB           +         2  79.3  16       1
 7 AB           +         5  73.1  17.4     2
 8 AB           -         1  83    16.6     1
 9 AB           -         3  79.8  15       2
10 AB           -         4  84.8  17.4     3
11 B            +         2  77.8  16.4     1
12 B            +         5  83.8  14.6     2
13 B            -         1  74.5  14.9     1
14 B            -         3  85.1  16.2     2
15 B            -         4  83.3  16.6     3
16 O            +         1  80.3  15       1
17 O            +         3  78.9  14.8     2
18 O            +         4  81.2  14.9     3
19 O            +         5  84.9  15       4
20 O            -         2  80.7  16.1     1
```

Comme vous pouvez le voir dans la colonne id, au lieu d'identifiants uniques, nous avons des identifiants répétitifs.
Pourquoi cela se produit-il si chaque ligne est différente ?

La raison de ce problème réside dans le fait que les données sont toujours regroupées.
Même si nous n'appliquons pas directement la méthode`ungroup` comme expliqué ci-dessus, nous pouvons tout de même le résoudre.

Voyons d'abord comment il ne serait pas résolu.
Une erreur fréquente lors de la résolution de ce problème est d'appliquer la fonction de dégroupement sans enregistrer le résultat.


``` r
# mauvaise application de ungroup
par_jour %>% ungroup()
```

``` output
# A tibble: 20 × 5
   type_sanguin rh     jour   f_b   f_r
   <chr>        <chr> <int> <dbl> <dbl>
 1 A            +         1  76.3  15.2
 2 A            +         3  81.5  16.6
 3 A            +         4  81.2  15.6
 4 A            +         5  81    15.9
 5 A            -         2  78.3  16.2
 6 AB           +         2  79.3  16  
 7 AB           +         5  73.1  17.4
 8 AB           -         1  83    16.6
 9 AB           -         3  79.8  15  
10 AB           -         4  84.8  17.4
11 B            +         2  77.8  16.4
12 B            +         5  83.8  14.6
13 B            -         1  74.5  14.9
14 B            -         3  85.1  16.2
15 B            -         4  83.3  16.6
16 O            +         1  80.3  15  
17 O            +         3  78.9  14.8
18 O            +         4  81.2  14.9
19 O            +         5  84.9  15  
20 O            -         2  80.7  16.1
```

``` r
# bien que cela désagrège l'objet pour l'affichage,
# tant que l'objet n'est pas stocké, il restera groupé
par_jour %>% mutate(id = row_number())
```

``` output
# A tibble: 20 × 6
# Groups:   type_sanguin, rh [8]
   type_sanguin rh     jour   f_b   f_r    id
   <chr>        <chr> <int> <dbl> <dbl> <int>
 1 A            +         1  76.3  15.2     1
 2 A            +         3  81.5  16.6     2
 3 A            +         4  81.2  15.6     3
 4 A            +         5  81    15.9     4
 5 A            -         2  78.3  16.2     1
 6 AB           +         2  79.3  16       1
 7 AB           +         5  73.1  17.4     2
 8 AB           -         1  83    16.6     1
 9 AB           -         3  79.8  15       2
10 AB           -         4  84.8  17.4     3
11 B            +         2  77.8  16.4     1
12 B            +         5  83.8  14.6     2
13 B            -         1  74.5  14.9     1
14 B            -         3  85.1  16.2     2
15 B            -         4  83.3  16.6     3
16 O            +         1  80.3  15       1
17 O            +         3  78.9  14.8     2
18 O            +         4  81.2  14.9     3
19 O            +         5  84.9  15       4
20 O            -         2  80.7  16.1     1
```

Comme vous pouvez le constater, le problème n'a pas été corrigé.

Pour le corriger, nous pouvons soit inclure le `ungroup` dès le début lorsque nous créons l'objet `por_dia` soit appliquer la modification et l'enregistrer dans l'objet :


``` r
# nous stockons maintenant le désagrégement
par_jour_sans_groupe <- par_jour %>% ungroup()

par_jour_sans_groupe %>% mutate(id = row_number())
```

``` output
# A tibble: 20 × 6
   type_sanguin rh     jour   f_b   f_r    id
   <chr>        <chr> <int> <dbl> <dbl> <int>
 1 A            +         1  76.3  15.2     1
 2 A            +         3  81.5  16.6     2
 3 A            +         4  81.2  15.6     3
 4 A            +         5  81    15.9     4
 5 A            -         2  78.3  16.2     5
 6 AB           +         2  79.3  16       6
 7 AB           +         5  73.1  17.4     7
 8 AB           -         1  83    16.6     8
 9 AB           -         3  79.8  15       9
10 AB           -         4  84.8  17.4    10
11 B            +         2  77.8  16.4    11
12 B            +         5  83.8  14.6    12
13 B            -         1  74.5  14.9    13
14 B            -         3  85.1  16.2    14
15 B            -         4  83.3  16.6    15
16 O            +         1  80.3  15      16
17 O            +         3  78.9  14.8    17
18 O            +         4  81.2  14.9    18
19 O            +         5  84.9  15      19
20 O            -         2  80.7  16.1    20
```

Comme vous pouvez le voir maintenant, si nous avons chaque ligne avec son propre identifiant.

Remarque : il est important de préciser que, dans les scénarios précédents, le dégroupage est effectué après l'opération, alors que, dans le cas présent, il est effectué avant l'opération.

### Lorsque j'essaie de créer un pdf dans RMarkdown, j'obtiens l'erreur suivante

Si le fichier sort correctement dans d'autres formats que le pdf.
L'une des situations les plus fréquentes est que l'installation de LaTeX est manquante : RMarkdown a besoin de LaTeX pour générer des PDF.
Assurez-vous que LaTeX est installé sur votre système.

Pour installer LaTeX à partir de RStudio, vous pouvez utiliser le paquetage TinyTeX :


``` r
install.packages("tinytex")

tinytex::install_tinytex()
```

Configurez RStudio :

Allez dans Outils > Options globales > Sweave.

Assurez-vous que l'option "Typeset PDF" est réglée pour utiliser TinyTeX.

### Matériel supplémentaire pouvant contribuer à votre apprentissage :

**Traitement des données avec Tidyverse et R :**

<https://www.youtube.com/watch?v=6STcQVX8Hk0>

::: keypoints


:::

## Contributions

- José M. Velasco-España : Version initiale
- Andree Valle-Campos : Éditions mineures
- Laura Gómez-Bermeo : Éditions mineures
- Geraldine Gomez : Éditions mineures
- Hugo Gruson: Traduction en français

