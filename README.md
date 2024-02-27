
# BigData project: Leage of legend game analysis using spark

![Logo](https://i0.wp.com/highschool.latimes.com/wp-content/uploads/2021/09/league-of-legends.jpeg?fit=1607%2C895&ssl=1)


The project aim to analysis match data in LOL game using Apache spark. The team start by the project by understanding the domain knowledge. Actully, we have no idea about the game so we go and learn how to play it!

After collecting more details about the game we put some metrics to find which will be descriptive for the path 11.23.

**Win, Pick, and Ban rate** : How much this champion get Picked, baned or win?

**Champion Synergies**: The synergy between each two champions

**Item win and pick rate**: Same as champion win and pick rate

**Item Synergy** : Item-champion synergy









## How the data is collected?

The data is collected using **Riot API**. we have collected a dataset of **120,000** matches of different patches of the game. Then we filtered this dataset and kept the data of only 11.23 patch which were **72,455** matches.

## Methodology
**Win, Pick, and Ban rate**:
It was calculated for each champion on some steps. First, we read the champion’s name of each summoner in each match and read whether the player has won the match or not as pairs in an RDD called champs. Each element in that RDD was a tuple of the champion’s name and an int value of 0 or 1 to represent winning status. Second, another RDD was generated to contain only the tuples of winning champs called **win_champs**. Each of these two RDDs was grouped by key, the champion’s name. The list of matches related to each champion in each of the RDDs was converted to an integer number refer to the length of the list. Third, the two **RDDs** were joined again together. Fourth, for each champion the number of won matches was divided by the number of played matches to calculate the **win rate** for each champion.

Similarly, the pick and ban rates were calculated. Pick rate represents the 
number of matches a champion takes part in divided by the number of all matches in 
the dataset. While ban rate represents the number of times a champion is banned 
divided by double the number of items, because each player can be banned two times 
in a game.




## Documentation
    A full documentation of the project can be found int the pdf attached
[Documentation](https://linktodocumentation)


## 🛠 Skills
Python, Apache Spark
, CoLab...

