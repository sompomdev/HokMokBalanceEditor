



KPIDashboard.

SUPPORT DPS 
  On est en train d'afficher le SUPPORT DPS.

Ensuite on affiche les impacts du support DPS sur le reste.


x
Il faut afficher ce que je vois dans le jeu :
- le Tap DMG du Héro 
- le Support DPS
- PET DPS
- Average DPS 

Comment on calcule les effets des éléments des support sur le DPS>


- Et ensuite ses effets sur le DSPS et les autres KPI du héro.




Et on enchainera sur la meme chose pour les pets.

Il faut avoir un modelUtils sur les achievements.



Afficher :
 ~~- les infos sous forme de tableaux 

SupportSettings component =>

~~=> il faut un combo avec la liste des supports. ~~
~~=> vérifier où on va récupérer la liste des données ( avec le model utils) ~~

Il faut un formulaire pour les données du support.
=> quand on a choisi, on affiche le détail des support dans le form.

Il faut afficher les données que j'ai dans le fichier, et mettre en form uniquement celle qui sont utilisés => et faire un debrief avec Bora sur ce point.

=> et ensuite on le save dans le store.

=>4h.


Et j'ai encore une problématique su rles achievements, il faut avancer sur la partie données.



Il me faut la possibilité de modifier le paramétrage des supports dans le parameters.
  => button support to access support component 
  => support componetn : list de support 
  => formulaire avec les différentes valeurs
  => pouvoir sauvegarder le modèle et ensuite l'exporter.



Fixer l'affichage des supports.


Il faut revoir le modèle du support.

Il me faut un modèle Util, permettant de manipuler facilement toutes les supports et les implémenter en unit-test
- support par id
- support par nom
- calculer les skills effect d'un DPS en fonction d'un niveau

Je peux organiser tout ça juste par model utils en fait Et je vais aller beaucoup plus vite.
=> J'ai le niveau du support, donc j'ai le evolve counter. et j'ai le unlock.

Meme hcose pourles pets ensuite.


POssible level-up à l'air d'etre bloqué à 1.00K

=> c'était vraiment à cause de l'argent alloué au support.
Intéressant en fait, ca ma peut etre fait corriger des soucis du coup.






- Trouver un algorithme pour calculer le skill d'un seul support, et surtout pouvoir le re-exploiter ou calculer ensuite.



et ensutie faire l'addition de tout ces skills benefits sur la team.
BalanceBuilder => buildListBonusSupportTapDamage


=> revoir comment est initiaoliser le supportDetail Selected,
et ensuite appeler la méthode que je viens de creér 
buildListBonusSupportTapDamage2

buildBonusSupportTapDamageForSupportID


Correction rapide : 
. Visualisation => il faut revoir les min/max des sliders, le hero et le monstre ne sont plus alignés.

Surpport : 
~~. dans cette popup : on voit le nom et l'image du support 
. on voit aussi l'argent à cumuler pour atteindre le niveau affiché.


Cette popup servira à afficher le détail des effets (par support)

Il faudra aussi une popup pour afficher le total des effets pour avoir le DPS.

=>innerFunctionBuildPossibleLevelUpForSupport
Il faut que je revoit cette fonction, et que je définisse clairement comment va être calculer le DPS de la team.

Je veux vérifier les formules de progression des supports.
Comment je vais faire?
=> Il faut que je puisse visualiser : les couts.
=> Il faut que je puisse visualiser en fontion de l'argent disponible le niveau où je peux l'emmener.
=> juste un composant de 'veirification pur vérifie que les calculs sont logiques.
 - min: niveau avant utilisation de l'argent
 - max : niveau possible en fonciton de l'argent tuilisé .
 - calcul du cout cumulé à dépenser. 

=> faire le schéma de la vue que j'ai besoin d'afficher pour vérifier. (il faut une autre popup)



Je suis en train d'essayer d'afficher les DPS des supports.
bonus passif DPS, bonus actif, DPS team , => ensuite facile d'appliquer sur le TTKG et le TTKB

Et il faut le listPossibleLevelUp =>

buildSupportDPSWithSkillSupportAllDamageAndSupportDamage
 => il y a une sous fonction à extrairer pour pouvoir ré-utiliser la logique de calcul.



Implémentation:

Il faut intégrer l'effet des supports sur le TTG. Ce qui est en cours donc c'est de faire remonter sur l'UI les effets du support. [[TTKG Support]] [[TTKBoss Support]]


[[FTT]], le FTT est juste pour le ratio, 1:1, mais la disposition de l'UI n'est pas claire. Il faut la clarifier pour rendre évident ce que l'on regarde et ne pas confondre, le levelup, et le nombre.

J'étais en train de travailler sur [[Balance Verification Criteria - List]] 

Le but est de déterminer par des propositions en texte normal comment on veut que le jeu soit équilibré => et les traduires en KPIs.

Une fois que tous les KPIs auront été exprimés, on pourra en faire des dépendances => ce qui facilitera l'implémentation.

La problématique est celle d'intégré les items dans cette phase.
 
 [[Balance Verification Criteria]]
 
 