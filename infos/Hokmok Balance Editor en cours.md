# Hokmok Balance Editor en cours

[Questions à poser à Puthear](Questions%20à%20poser%20à%20Puthear.md)

Concernant les quêts .

⇒ categorie et type de quete.

⇒ quel KPI pour les quêtes 

`'Unlock','Tap','Hero','Support','Tutoriel', 'Defeat','Battle','Progression','Collect'`

SkillsAndPerks

**Il ne faut pas que les quêtes ne servent à rien sur les hauts niveaux.**

Le problème c'est queles quest ont une evolution linéaire.

Il faut que les quests soient ajustées par rapport à un niveau. Par exemple le niveau 50 000

Problème pour les quests de type farming.

Une quête doit donner un équivalent farming :

 - 100 ghost Lvl1, 100 ghost Lvl2 etc... 

 - l'équivalent farming, doit etre déterminer par le niveau à laquel cette quete puisse etre débloquer. 

Exemples:

 - Tuer 10 ghosts Lvl 11 

Tutoriel

Battle 

Level Up

Progression 

  Reachn 

Statistiques Cumulatives

Unlock 

  pet

  support 

LevelUp

  Pet 

  Support

Gameplay :

   matchingStone 

   tap in short time 

   make an action

One Shot 

  Tutorial

  Twitter 

  Facebook

IL faut revoir le cumul des diamands pour s’assurer que c’est ok. = DONE

ensuite il faut appliquer les bonus a l’effet de visualisation. - DONE

=> avec version aussi sur quêtes.

Ce que je veux pouvoir calculer cé st l’effet du pet sur ls attaque du hero.

Donc pour ce faire, il faut calculer  qui peut etre l’actif => ca c’estok.

Ensuite je prends le base dmg => pour avoir la valuer du pet.

Active Pet Effect

La valeur d’ attaque ‘un pet est egale a sa valuer max / nombre de tap

example:

500

20 taps

=> 25 + 500 / 20  => 26.25

DMG

**EN COURS :**

visualisation des pet,

quand un pet monte en niveau, il faut définir les caractéristiques qui le font évolue.

Ecran de detail d’évolution d’un pet

La ligne avec les impact sur le DMG ALL du pet.

=> skills

=> passive

=> pet damage.

=> tap capacity.

Cumulation des pets.

Premiere columne de 1 à 99 :

Active

Tap Capacity

Pet Damage

[skill] active value

**Passive**

Pet Damage

[skill passive value]

Regeneration Time

Total Pet DMG. (en fonction du niveau)

**Pet List**

. on a besoin du détail de la visualition d’un pet comme sur les achievement.

**Taches**

. detailler la progressio d’un pet : en bonus, en dmg.

. Par niveau: les effets passifs: e total dmg passive, le total DMG_ALL,

. Par niveau: l’ effet du pet le plus fort sur le tap dmg.

. L’effet du pet alliance.

**.** Le visu comme dans le jeu de la stats cumulé par niveau de tout le groupe en passif

. Et les effets bonus de chaque effect.

Achievement manquants que sont le cumul d’utilisation des skills,

Achievement manquant liés aux mana, et au temps de jeu + des achievment one-shot

**QUESTION BLOCANTE A REONTER A BORA POUR ACTION**

- level up support : c’est quoi c’est toute l’équipe???
- Rajouter le skill manquant pour les quest
- Rajouter le skill manquant pour les achievement
- Reduce the mana reduction to 10mn
- **** Maintenant j’ai l’utilisation des skills, montée en level Et la problématique des quest. => (rajouter les skills dans les achievmeent et les levels dans les quest)
- bug if you kill a boss with a combo, the combo stay vilisble on the gameplay a little bit after the winning screen.
- question : icon des quest dans le boss?
- quest i can skip with 0 diamond?
- ils ont pas actualisé la version du store, je vais checker pourquoi l'apk a chercher a faire une update alors qu'il était censé etre plus récent que la version du store

note rapide:

rajouter rapidement un autre achievement, puis voir comment on va tout rajouter, plus définir exactement le next step pour les pets et tirer parti des diamand.

Attention

Kill ennemy => c ést tous les ennemis, donc je peux le faire que a la fin.

~~Kill ghost => c ést bien le farming.~~

Il faut reprendre tous les achievmeent un par un dans l’ordre.

~~kje rajoute une section diamand comme ça je visualise pour un KPI~~

~~=> ensuite il faut le faire pour tous les **achievmeents**~~

**~~Faire la liste de tous les achievment à cosidérer un par un.~~**

~~Et surtout traiter correctement le cumul~~

~~Il faut que j’ai une ligne pour les diamands, et qu ej’ai un détail de composant pour chaque achievment.~~

~~la on doit s’en tenir à tous les achievment d’abord.~~

Règle simple: tous les achievments vont se cumuler.

Les quest vont se renouveller.

**JE SUIS EN TRAIN D’ ESSAYER DE VOIR COMMMENT JE MESURE LE DIAMAOND SPAWN PAR NIVEAU.**

~~=> on fait le test avec 1 achievment lié à la métric kill_ghost.~~

~~. Je fais une fonction stub pour tous les métriques jeux (pour l’instant kill_ghost uniquement)~~

~~. Je rajoute une nouvelle section Metriques Jeux en dessous de General.~~

. J’ai besoin d’une fonction, pour compute =>

~~Il me faut une fonction qui va me retourner la liste des achievements collectés en fonction de l’achievement value à un niveau précis => c’est la fonction getDiamondMatchingLevelForAchievment(~~

~~simulateUnlockForLevel(level,achievmeentId)~~

~~et l’autre, ou je passe la valeur du KPI, docn c e’st pas simulateUnlockForLevel,~~

~~c’est simulateUnlockForChallenge(challengeValue)~~

~~=> j’ai besoin d’une fonction pour pouvoir charger les achievments dans les tests~~

~~Mais par contre il faut que je puisse charger les achievements correttement dans la fonction~~

~~getDiamondMatchingLevelForAchievment~~

~~Mettre les achievmeents dans une constante.~~

~~getDiamondUnlockForAllAchievementAtLevel() => all achievment~~

~~. je recupère l'achievmeent~~

~~, je boucle en fonction du niveau, car je peux boucler en fonction du niveau~~

~~. pour chaque niveau, je recupere le KPI, (qui me donne un chiffre), je passe ce chiffre => a la liste detail d’un achievmeent, et je r’ecupère la colonne challenge, et je cumul la reward.~~

Example: niveau 10, 100 =>

~~. Je rajoute une nouvelle section Diamand~~

~~. Je rajoute une ligne pour l’achievment metric kill_ghost~~

~~. Je rajoute d’autres KPI pour cumuler les achievments.~~

. Je reviens au fichier xls pour l’enchainement de la logique.

~~Comment je vais savoir combien un achievement me rapport de diamand en fonctio du niveau.~~

~~On prends un exemple en particulier~~

~~Et ensuite on généralise.~~

**VOIR ICI**

Kill Enemies = > 7800

Il faut que en fonction d’un niveau je puise calcler **le nombre d’enemi tué  => métrique gameplay.**

Et ensuite, je cumule la reward de l’achievement.

En fonction du niveau il faut que je puisse récupérer ma : métrique gameplay.

Exemple:

nombre minimum d’ennemis tués en fonction du niveau. example: niveau 10 c’est level * min-wave.

D’efini la liste des métriques gameplay.

---

Notes

Les quest ne sont pas liés aux diamands, les quests, sont juste liés à l’argent.

Cumulate/Not cumulate.

On a besoin d’un diamand pour booster les pets

Plus le pet est fort, plus il dort

On a besoin de diamand pour réveiller les pets

On a beaucoup de pet, ce qui permet de switcher lorsqu’un pet est fatigué.

Actualiser la rentrée d’argent pour l’éditeur.

Liste tous les points e tpour chaque point je rentre dans le detail des taches qu’il y a à faire.

exporter les données des support

exporter les données des pets

exporter les données des achievements

visualiser les formules

exporter les données des quests

exporter les données des héros

exporter la configuration du Master Mind

exporter la formule du farming offline

exporter la configuration des perks

Golden Walelt Formula

Give me cash (against diamond)

Flying support

Shield

300 taps / minutes.

**~~Il faut ajouter dans la partie des achievements, l’unité de référence.~~**

~~Il faut ajouter une nouvelle propri’eté qui va permettre de visualiser correctement si on cumule ou pas.~~

Il faut visualiser ceux qui sont terminés ou pas encore. ???

Et il faut surtout visualiser et décomposer l’extrapolation des pets.

=> les pets ont des effets sur les domages et l’or,

=> par rapprot en input : les diamands => je vais gonfler les effets.

=> pour les achievements il faut pouvoir les traduire en niveau ou en cout d'argent

=> il faut pouvoir calculer le cout d’argent pour faire booster un hero a un certain niveau

=> il faut pouvoir transformer le cout en argent en temps de jeu ??? , ca va pas etre facile.

**=> il faut une fonction, estimatedDiamond**

POur un niveaux:

- Le cumul des diamands dépendent du spawn des boss

- Le cumul des diamands dépendent des achievement.

- team pet débloqué par niveau minimum, (on utilise l’ exponent pour chiffrer, et on représente le label avec SMPNUm)

Y a deux choses, non il faut que j’ai mon truc en local. pour que je sois pas bloqué et que je le re-d’eploie:

- regarder ce qu’on a sur le serveur
- redeployer en local ce que j’ai sur le servur
- basculer en mongodb => pas nécessaire.
- ~~je recupere en local les fichiers csv~~
- ~~installer strapi en local, je fais une setup avec mongodb~~
- ~~je démarre l’appli en local~~
- ~~je créé juste les meme collections qu’en ligne~~
- ~~et j’inject les données dans le modèle à partir du csv.~~
- ~~j’import les csv dans les collections~~

**=> il faut que ça marche avec l’appli en local**

- achievmeent créér le modèle
- créer une api-put
- sauvegarder le achievementModel Gameplay
- exporter le json
- ~~et avec l’appli vue, je change pour attaquer l’appli en local~~
- je fais un dump => et on est bon.
- je créé un repository sur bitbucket pour l’ éditeur.
- il faut récup’erer lequel est bon ou pas, mais pour l’instant par rapport a ce que je dois faire, je m’en bas les couilles j’ai suiffsament pour avancer les achievements.

**Action en cours:**

~~Afficher ls achievement non pas dans une popup mais dans leur propre fenetre, et en cliquant, on affiche dans la popup, le résultat de la progression,~~ et on autorise pour chaque achievement à changer les valeurs.

- ~~il faut que je bind lorsqu’on arrive dans les achievement, la liste des achievement model par rapport au json.~~

Il faut faire la liste pour chaque achievmeent de la formule à employer.

Je rajoute une section achivement

Je rajoute pour l’ahcievment collecter l’argent le total estimé de diamand perçu pour le niveau en cours

ensuite je créé un autre composant pour afficher ça dans le détail achievement.

~~je vois comment modifeir le ratio pour modifier ça directement.~~

~~=> progression linéaire.~~

Le problème c’est que l’éditeur ne me permet pas de visualiserles différentes progression, je dois le visualiser comme le test unitaire,

pour chaque achievement.

Petite note rapide sur la notion de quete petite/moyenne/grande

Une petite quete est une quete qui va pouvoir etre terminé en 5mn par exemple

Donc le référentiel est un réf’erentiel de temps.

Ce réferentiel de temps doit pouvoir se traduire par :

le nombre de tap

=> Je dois pouvoir calculer le nombre de temps

**Il faut pouvoir visualiser la progression des dimaands.**

Il faut que je puisse activer/désactiver les effets d’un élément de gameplay.

Ce que je dois pouvoir visualiser:

- je dois pouvoir visualiser, combien d’achievement est complété à un niveau donné.
- exemple: collecter de l’or.
- par rappor au niveau :

**note**: doom of god => should cost more than the boss can loot : => boss diamand loot * 3

Comment on la visualise :

Le cumul total possible par niveau.

Kill n ennemies => n can be calculated based on the

je dois pouvoir voir les effets des pets.

=> ligne du DMG Pet => la plus simple

=> comment visualiser les effets des pets car on en a plusieurs.

Le problème des pets:

- c’est qu’ils sont débloqués par les diamands.

- le problème des dimanads c’est qu’ils sont ;débloqués par les achievement et par le drop des boss.

- une ligne : drop boss diamond

- une ligne : drop achievement

~~Il faut voir les effets de toute lea team~~ et ensuite refaire une passe sur la liste des effets.

Et d’abord les pets.

je dois pouvoir modifier les skills des support et que ca soit raffraichis automatiquement

**Le probl`mee est que le watch sur la props ne marche pas**

maintenant il faut que je sois sur que ce qu’il y a dans le balanceVue. soit raffraichi correctement.

Example: si je vais trop vite.

Il faut probablement faire un watch sur le store, car le init est appelé uniquement dans le init.

- il faut réflkéchir à comment on va visualiser le cout des diamands.

. rajouter la liste des achievements pour pouvoir totaliser le nombre de diamand spawner.

- l`a il faut pouvoir afficher le nombre de déclinaison

- pouvoir modifier le nombre de déclinaioson de l’achievement.

- et avoir une compute property qui permet d’afficher le nombre total de diamands gagner.

- et il faut aussi vérifier comment on fait pour récuperer et modifier la valeur des goals.

. tous les support on le meme DMG dps de base. donc ok.

. ensuite là je dois vérifier comment je vais prendre en compte les impacts des skills.

. rajouter un effet sur le skill des support sur le tap damage

**~~relire la fonction utilisé dans le fichier xls**, et en extraire l’algorithme et le ré-appliquer.~~

~~Skill Impacting Hero DMG~~

~~Sjupport Skill Tap DMg~~

**A DETERMINER**

**On défini tout ce qui reste à faire:**

- le ratio de progression des HP des fantomes -

-  le ratio de progression du HP des boss

- ratio de cout du hero

- ratio de progression des héros.

- ratio de progression des supports.

- ratio de cout des supports

- l’ordre d’enchainement des quêtes

- la valeur de récompense des quêtes

- cout de skip des quetes

**Support Skill**

- pourcentage de progression

**Hero Skills**

- ratio de progression

- cout en mana

- cout en argent

**Perks**

- cout en diamand

**Deblocage Global du jeu**

- règle de deblocage des heros
- règle de déblocage des pets
- règle de déblocage des supports

**Règle de l'or**

- spawn du ghost

- spawn des boss

- spawn des boss revenge

**Règles des diamands**

- recompenses des achievements

- rèlge de spawn des diamands

- cout des skills (diamands)

- cout des upgrade de pets ( diamands)

BUG à leur donner:

- PETS alignement des upgrade /

- Quest:

la façon de générer les quetes dynamiques. => un bouton pour les générer automatiquement sur la meme base que les autres.

un module pour avoir les icones sur le coté, et assigner des noms pour chaque icones.

ensuite, une popup pour assigner les icones, et ensuite récupérer les noms qui correspondent pour les assigner à la quête.

ce qu’il faut cé st que je me le remette en tete ce qu’il y a:

iconGridSelection

skillList

iconList (iconSkill) , on aurait du renommer ça icon. => usedBy, name : {kh:, en: fr: }

questList

Algorithme d’application :