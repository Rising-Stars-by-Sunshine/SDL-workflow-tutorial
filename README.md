# # Title [How to Choice a Good Title?](https://www.nature.com/articles/s41562-021-01152-2)
## Project information
- **Author**: [First Name][Last Name], [Major], [Class], Duke Kunshan University
- **Instructor**: Prof. Luyao Zhang, Duke Kunshan University
- **Disclaimer**: Submissions to the Problem Set No. or Final Project for [COMPSCI/ECON 206 Computational Microeconomics, 2023 Spring (Seven Week - Second)](https://ce.pubpub.org/) instructed by Prof. Luyao Zhang at Duke Kunshan University.
- **Acknowledgments**: [How to Acknowledge?](https://www.scribbr.co.uk/thesis-dissertation/acknowledgements/)
[notes: please include all professors, students, and staff who have contributed to your completetion of the project.]
- **Project Summary**: 
  - [Summarize the Background/Motivation]
  - [Research Questions]
  - [Application Scenario]
  - [Methodology]
  - [Results]
  - [Intellectual Merits and Practical impacts of your project.]
  
   
Note: please insert the screenshot of the answers to your research question by ChatGPT. The methodology that you use to address the research questions must be more innovative than both the current literature and ChatGPT. 

## Table of Contents

- model
- code
- spotlight
- more about the author
- references

### Model
* Game environment <br>

	In ancient times, countries were endowed with different wealth and military forces of different intensities. Strong countries are always planning to use their military power to attack weak countries and annex their property. Vulnerable countries are always thinking about how to adopt strategies to address risks and protect their property.<br>

	Against this background, this is a trust game abstract from the ancient war between countries. Anyone with high fighting capacity can seize the wealth of those with low fighting capacity. Players with the same fighting capacity cannot seize wealth from each other. Players can form alliances, and their fighting capacity is the sum of both sides. They all want to get more wealth, or at least not worse off. <br>
	
	In this game, players will first need to decide on forming alliances with whom. Then, to persuade other players to ally with him, player 1 promises he won’t seize his partner’s money and can decide to offer some money to his potential partner to show his loyalty. After this, player 1’s target partner can see the money player 1 offer and redecide whether to cooperate with player 1. If they cooperate with player 1, player 1 will seize the remaining player’s money automatically. Next, player 1 will decide whether to break the cooperation and take his partner’s money.<br>
	
	
* Set of players <br>

	We assume that there are three players in this game. Each player has given the fighting capacity and money. <br>
Player 1 has 10 dollars, and his fighting capacity is 5.<br>
Player 2 has 3 dollars, and his fighting capacity is 2.<br>
Player 3 has 4 dollars, and his fighting capacity is 3.<br>

* Strategies <br>

	1.	No matter how much player 1 chooses to offer, player 2 and player 3 form an alliance and share 5 fighting capacities. <br>
	2.	Player 1 offers x dollars to player 2 and player 2 chooses to form an alliance with player 1. After seizing player 3’s money, player 1 breaks his promise and seizes player 2’s money.<br>
	3.	Player 1 offers x dollars to player 2 and player 2 chooses to form an alliance with player 1. After seizing player 3’s money, player 1 keeps his promise and doesn’t seize player 2’s money.<br>
	4.	Player 1 offers x dollars to player 3 and player 3 chooses to form an alliance with player 1. After seizing player 2’s money, player 1 breaks his promise and seizes player 3’s money.<br>
	5.	Player 1 offers x dollars to player 3 and player 3 chooses to form an alliance with player 1. After seizing player 2’s money, player 1 keeps his promise and doesn’t seize player 3’s money.<br>
	
	
* Payoffs (corresponding to the order of the strategies)<br>
	1.	Player 1 cannot attack player 2 and player 3, and player 2 and player 3 can protect their original wealth. As a result, player 1 will have 10 dollars, player 2 will have 3 dollars and player 3 will have 4 dollars.<br>
	2.	As a result, player 1 can have 17 dollars, player 2 and player 3 have 0 dollars.<br>
	3.	As a result, player 1 has (14-x) dollars, player 2 has (3+x) dollars, and player 3 has no dollars.<br>
	4.	As a result, player 1 can have 17 dollars, player 2 and player 3 have 0 dollars.<br>
	5.	As a result, player 1 has (13-x) dollars, player 2 has 0 dollars, and player 3 has (4+x) dollars.<br>
	



### Code
- Game Environment
- Strategic plays
- Equilibruim Evaluations: e.g. belief, strategy, and payoffs
- oTree Experimental Code 


### Spotlight
- Posters
- Figures
- Slides
- Presentations
- Review articles
- Media appearance

### More about the Author
- headshot
- self-introduction
- Final reflections 
  - intellectual growth
  - professional growth
  - living a purposeful life

### References

- Literature References in [Chicago Author-Date](https://www.chicagomanualofstyle.org/tools_citationguide/citation-guide-2.html) Style and [BibTex](https://scholar.google.com/) 

Levin, Dan, and Luyao Zhang. 2020. “Bridging Level-K to Nash Equilibrium.” *The Review of Economics and Statistics* 104 (6): 1329–40. https://doi.org/10.1162/rest_a_00990.

```
@article{levin2022bridging,
  title={Bridging level-k to nash equilibrium},
  author={Levin, Dan and Zhang, Luyao},
  journal={Review of Economics and Statistics},
  volume={104},
  number={6},
  pages={1329--1340},
  year={2022},
  publisher={MIT Press One Rogers Street, Cambridge, MA 02142-1209, USA journals-info~…}
}
```

