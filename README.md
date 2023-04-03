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
o	Game environment
	In ancient times, countries were endowed with different wealth and military forces of different intensities. Strong countries are always planning to use their military power to attack weak countries and annex their property. Vulnerable countries are always thinking about how to adopt strategies to address risks and protect their property.
	Against this background, this is a trust game abstract from the ancient war between countries. Anyone with high fighting capacity can seize the wealth of those with low fighting capacity. Players with the same fighting capacity cannot seize wealth from each other. Players can form alliances, and their fighting capacity is the sum of both sides. They all want to get more wealth, or at least not worse off. 
	Each round can be divided into two sessions. One is the decision session: players need to make the decision on whether or not to form alliances and with whom. Then comes the seizing session: players need to decide whether and whom they want to seize based on their fighting capacity. The next round will repeat the same process. The game will end when no one wants to seize other’s wealth.
	
	

o	Set of players
We assume that there are three players in this game. Each player has given fighting capacity and wealth.
Player 1 has 10 billion dollars, and his fighting capacity is 5.
Player 2 has 3 billion dollars, and his fighting capacity is 2.
Player 3 has 4 billion dollars, and his fighting capacity is 3.

o	Strategies & payoffs
1.	Player 2 and player 3 form an alliance, sharing 5 attack power. In this way, player 1 cannot attack player 2 and player 3, and player 2 and player 3 can protect their original wealth.
2.	Player 1, player 2, and player 3 are not aligned, and Player 1 can attack Player 2 and Player 3 respectively. In the end, Player 1 can have 17 billion dollars, while Player 2 and Player 3 can only have 0 billion dollars.
3.	Player 1 and player 2 align, then player 1 and player 2 can seize player 3's wealth. After looting, Player 1 can loot player 2's wealth again. In this case, player 3 has no interest conflict (he has no money in his pocket), so he has no motivation to help player 2. Finally, Player 1 can have 17 billion dollars, while player 2 and player 3 can only have 0 billion dollars.
4.	Player 1 and player 3 align, then player 1 and player 3 can seize player 2's wealth. After looting, Player 1 can loot player 3's wealth again. In this case, player 2 has no interest conflict (he has no money in his pocket), so he has no motivation to help player 3. Finally, Player 1 can have 17 billion dollars, while player 2 and player 3 can only have 0 billion dollars.

o	Solution based on backward induction
If we assume every player is rational, player 2 and Player 3 will choose to form an alliance, sharing 5 fighting capacities. In this way, player 1 cannot seize their wealth. The situation remains stable, and no one's wealth will increase or lose.

o	Efficiency and fairness
Efficiency: this is not applicable in this game. The total wealth among the three players is given and will not change according to how they behave.
Fairness: Under this solution, although the three players’ wealth is different, the fairness is pretty high since the wealth gap has not widened further (staying at the original level).



o	Evaluation
The solution is an unstable equilibrium. 
For Player 1, this is not the best outcome. He has an absolute advantage in combat effectiveness, but he has not been able to benefit from it. Thus, he has a strong motivation to change this equilibrium.
 Moreover, based on the fact that player 2 and player 3 are both motivated by a partnership of interests, their cooperation is not strong as we expected. If Player 1 can promise more benefits to Player 2 or Player 3 and make them believe that player 1 will only rob another player if they cooperate with player 1, the alliance between Player 2 and Player 3 can easily collapse.



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

