#balance-editor 
#last 

[[SMPQuestUpgradeAllHeroReachRankStrategy]]

Compute how many quest has been completed, at a specific level of ennemy.



- On revoit comment le calcul d'une quête est effectué

C'est effectué via:
GameplayQuest -  computeQuestEvolutionSimulation ()

Il y a une initialisation à 100 sur numberOfTimesYouCanPlayTheQuest

La donnée est dans:  ?? je ne sais pas. Il faut pouvoir déterminer combien de fois on va répéter une quest.



- On doit voir où c'est 

GameplayQuest => 
collect -=>
increaseKPIGameplayReference
computeChallengeAndReward

QuestImpl/QUestxxxx => computeChallenge
  

TODO : reprendre le pas à pas du calcul d'une reward d'une quest.
Code in progress:
QuestKPIQuest => 

- the strategy of Bora is inside the mapping file:
questStrategyAdapter.json 

On est en train de convertir une des strategy ca se fait demanière simple, en re/copy pastant le code. 




