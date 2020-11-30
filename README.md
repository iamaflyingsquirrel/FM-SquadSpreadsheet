# FM-Squad Spreadsheet
A spreadsheet to help manage new squads, and to get a quick feel (with consent) for who is who.

It was tested on FM19, 20, and 21, but I make no promises that it works perfectly.


**Overview**

As a firm believer in starting at the bottom, my backroom staff are generally awful, and so a while back I searched around for a spreadsheet that I could export my squad into, in order to get a better understanding of just what I'd let myself in for.  Unfortunately, all of the spreadsheet tools I could find were either overly simplistic or out of date, and so I created this...lunacy.

<a href="https://drive.google.com/uc?export=view&id=1_Fbf1kTX6fY7ki8wiBoimFdXIMZ5HYuu"><img src="https://drive.google.com/uc?export=view&id=1_Fbf1kTX6fY7ki8wiBoimFdXIMZ5HYuu" style="width: 500px; max-width: 100%; height: auto" title="Click for the larger version." /></a>

There is a readme tab in the spreadsheet which should be read but essentially the steps are:

    1. Import the custom view to FM

    2. Export your squad to a html output (CTRL+P in squad view)

    3. Delete the example data in the spreadsheet (SquadExport tab) and import your export using XML import
    
Once you've imported your squad once, you can just keep overwriting the output from step 2 and refresh the data in Excel. There are some weird Excel quirks to wrestle with, though, namely when you refresh the data it sometimes screws up the formulas in the WeightedParse tab. Simply select all row 2 cells and drag down to reapply them properly.  This will work on all sheets come to think of it, if it ever breaks then just unhide all columns, and drag all row 2 cells down.

Anyway, enough words. There's a list of concerns/issues on the readme tab, if anyone finds this sort of thing useful then maybe I'll fix them in the future.



**[Weighted Summary]**

- The main tab to view once you've imported your squad

- Players are highlighted in green text if they are the best player in their position

- [Suggested Squad] uses position ranking and age to determine where they should go

- The best outfield First Team and Reserve players to chuck in goal in an emergency are also highlighted

- [Original Positions] the currently trained in positions, e.g. DM, AM, etc.

- [Calculated Position] uses the stat weights and role requirements to determine their best position

- [Calculated Role] Uses the attribute weightings to determine which role suits the player best

- [Positional Rank] orders the players from 1 (highest) to lowest based on their ability scores within their position

- [Overall Rank] orders the players from 1 (highest) to lowest based on their ability scores within the squad

- [Overall Rating and all attributes] uses a harmonic mean of a players weighted attributes to calculate a player's best role

- Attributes with a black outline indicate the players best role


**[Position Strength]**

- Shows the top 3 players and their roles for each part of the pitch based on their overall rating

- Colours are based on some simplistic estimations of skill at each footballing level

- Can be useful to see what formations might work outside of your coach's recommendations

<a href="https://drive.google.com/uc?export=view&id=14_4vJF6vKDpqrZyEnRb6bU9S-XbOA_yW"><img src="https://drive.google.com/uc?export=view&id=14_4vJF6vKDpqrZyEnRb6bU9S-XbOA_yW" style="width: 500px; max-width: 100%; height: auto" title="Click for the larger version." /></a>


**[Individual Training]**

- Uses a player's suggested role from the Weighted Summary tab to determine which areas need work.

- Attempts to recommend a training focus for each player, based on their suggested role's weakest area

- Uses a traffic light system to highlight which attributes are weakest (grey is below 5, red is below 10, yellow is below 15, and green is below 20)

<a href="https://drive.google.com/uc?export=view&id=1MO293XH617hurxY77IkXow0z11YfRIu7"><img src="https://drive.google.com/uc?export=view&id=1MO293XH617hurxY77IkXow0z11YfRIu7" style="width: 500px; max-width: 100%; height: auto" title="Click for the larger version." /></a>


**Other Tabs**

There are also 5 other tabs; WeightedParse, Training, Roles, Weights, and SquadExport.

[WeightedParse] takes the exported squad html (which is imported to [SquadExport]) and weights them against the values in the [Weights] tab.  A striker would have different attribute requirements to a full back, and so this was an easy way of calculating which players had useful attributes.

[Training] checks a role's attributes against each training focus to derive a 1-3 score
For example, A wingback's role includes Crossing, Dribbling, First Touch, Marking, Passing, Tackling, Technique, Anticipation, Concentration, Decisions, Off the Ball, Positioning, Teamwork, Work Rate, Acceleration, Agility, Pace, and Stamina.  The training focus 'Ball Control' covers Dribbling, First Touch, and Technique (so a wingback would get a score of 3), whereas the training focus 'Final Third' covers Composure and Decisions, and so a wingback gets a score of 1 (as only Decisions are matched).  These numbers are used to weight against a players attributes to work out which are the weakest for their role, and which training focus would improve them the most.

[Roles] were taken from the in game scout suggested attributes for each role

[Weights] stat weighting for attribute, for each position.

[SquadExport] This is where you'll keep your exported html output.  You can either just paste in your data, or set up a data connection in Excel using Data > Get Data > From File > From XML > and importing it directly into the SquadExport tab at $A$1.  if you import it anywhere else, it's probably not going to work.

