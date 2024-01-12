# Hex Game

Place tiles to connect your two borders of the board. Play against an AI, implement human vs. human game mode or create your own AI strategy in `strategy.py`.

## Dependencies

`pip install -r requirements`


## Run the program

```
$ python main.py -h

usage: main.py [-h] [--size SIZE] [--games GAMES] [--no-ui] [--player {human,random,minimax}] [--other {human,random,minimax}]

Runs a game of Hex.

options:
  -h, --help            show this help message and exit
  --size SIZE           Size of the board (Default: 7)
  --games GAMES         Number of games to play in tournament. Only if no human (default: 5)
  --no-ui               GUI is not displayed. Only if no human.
  --player {human,random,minimax}
                        Strategy for player1 (default: human)
  --other {human,random,minimax}
                        Strategy for player2 (default: random)
```

## Implementing a new strategie

1. Extend the `Player` class
2. Implement the `start()` function
3. Add your newly created class in `str2strat` at the bottom of the `strategy.py` file
4. Run the program with `python main.py --other my_new_ai_strat` to experiment !

Tip: to debug your AI use a small board (2, 3, 4).

## Comparing AI strategies

Use the `--no-ui` and `--games` options to run a lot of simulation quickly.
For example, `python main.py --player random --other minimax --no-ui -- games 100` will run 100 games between random AI and minimax AI.

7 Mode d’emploi
Pour lancer le projet de jeu de Hex avec des stratégies d'intelligence artificielle, suivez ces étapes simples :
Activer l'environnement virtuel Python Ouvrez un terminal et naviguez jusqu'au répertoire du projet sur votre bureau en utilisant la commande cd. Une fois dans le répertoire du projet, activez l'environnement virtuel en exécutant :
shell
source mon_env_python3.10/bin/activate
Vous remarquerez que le nom de l'environnement virtuel (mon_env_python3.10) apparaît avant le prompt de votre terminal, indiquant que l'environnement est actif.
Lancer le jeu Toujours dans le terminal, lancez le jeu en exécutant la commande suivante :
shell
python3.10 main.py --size 10 --games 10 --player qlearning --other random
Cette commande démarre le jeu avec les paramètres suivants :
--size 10 définit la taille du plateau à 10x10.
--games 10 spécifie que 10 parties seront jouées.
--player qlearning sélectionne la stratégie Q-Learning pour le joueur principal.
--other random définit le joueur adverse pour utiliser la stratégie Random.
Observer les résultats Après le lancement, le jeu va automatiquement jouer 10 parties en utilisant les stratégies spécifiées. Les résultats de chaque partie seront affichés dans le terminal, indiquant lequel des joueurs (White ou Black) a gagné. Il y’aura également une illustration graphique des résultats. 
Une fois que vous avez terminé de jouer ou d'effectuer des tests, vous pouvez désactiver l'environnement virtuel en tapant deactivate dans le terminal.
Assurez-vous que tous les paquets nécessaires sont installés dans votre environnement virtuel et que votre fichier main.py est correctement configuré pour utiliser les options de ligne de commande.

Étudiants : Moustapha Diop, Fall Khadim
Merci pour la lecture 
