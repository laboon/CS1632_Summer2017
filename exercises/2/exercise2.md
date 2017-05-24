## Exploratory Testing Exercise

For this exercise, you and a partner will perform exploratory testing on the simple game Professor Wumpus, based on the requirements listed.  There are several known defects in the software; you will need to find and report on three defects.  There should be two and only two members of a group.

For full credit, all three defects should follow the defect reporting template discussed in class:

	 SUMMARY:
	 DESCRIPTION:
	 REPRODUCTION STEPS:
	 EXPECTED BEHAVIOR:
	 OBSERVED BEHAVIOR:

Other attributes of a defect (e.g., SEVERITY or IMPACT) are not necessary.  The test case which found the defect should be listed as part of the DESCRIPTION.

## Professor Wumpus
Professor Wumpus is an action-packed game of turning in your CS homework.  There are three characters:

1. *Student* - This is the player.  The player can move North, South, East or West.  The goal of the player is to find the Assignment (hidden in a random room) and then turn it in to Professor Wumpus, thus winning the game.  If you encounter Professor Wumpus before you find the paper, you lose the game.
2. *TA* - The TA wanders around the rooms randomly.  If you encounter her, you will flee in terror to a random room.  The TA carries a stack of graded papers, whose rustling you can hear from one room away.  The TA moves one room every time the student moves.
3. *Professor Wumpus* - Professor Wumpus stays in one room and mumbles on Computer Science topics (allowing you to hear him from one room away).

The studen is able to smell the assignment from one room away in any direction.

You can run it downloading the profwumpus.jar file and running:
```bash
java -jar profwumpus.jar
```

You may optionally include a random number seed (any 32-bit signed integer value) as the sole argument to the program.  Without a seed, the numbers will be pseudorandom based on the default Java Random class.  Otherwise, the integer will act as the seed and allow true reproduction (since the "random" numbers will be the same for each run).

The requirements are listed in the file requirements.txt.

The defects must be shown to me in class OR emailed to me before the next class in order to receive credit.

```
Grading:
Three defects, reported correctly: 2 points
Two defects, reported correctly: 1 point
One defect, reported correctly: 0.5 point
```

 
