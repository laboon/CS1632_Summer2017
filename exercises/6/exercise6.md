## Exercise 6 - Web Testing with Selenium

In this exercise, you will test a real web application - the Hibersense portal.  You will perform 20 to 30 minutes of exploratory testing, and then write 4 Selenium/Junit tests to test some subset of its functionality.  Ideally, these Selenium tests will check for a defect that you found.

Your group will get +0.5 bonus points (= +0.5% on your final grade) for each _valid_ defect that you find and report.  There is a maximum of +1 bonus point (= +1% on your final grade) on this assignment (in other words, you will not get credit for finding more than two defects).  In the case that multiple groups report the same defect, the first to report it gets the bonus points for it.

Your four Selenium tests are _not_ expected to cover all, or even most, of the functionality embedded in the requirements.  However, during your exploratory testing, I expect you to at least do some minimal testing for each requirement.

Note that this exercise _must_ be done in a group, as we have a limited number of logins to the Hibersense system.

### Login

You will be assigned a username and password at the beginning of class.  We only have 15 logins, and so all students will be required to work in a group.

Once your group has a username and password, you may login at https://hibersense.com/access/login

### Requirements

FUN-LOGIN - A user shall only be able to log in with a valid username and password.  If an invalid username or password is entered, the user shall be informed.

FUN-FEEDBACK - All accessible pages shall have a link to the "Provide Feedback" functionality.

FUN-LEFT-MENU - A menu shall exist on the left.  Clicking on the first menu item shall direct the user to https://hibersense.com/access/temperature, the second item to https://hibersense.com/access/view, the third item to https://hibersense.com/access/edit, the fourth item to https://hibersense.com/access/settings.

FUN-VIEW-PAGE - After selecting a sensor, data for that sensor shall be viewable on the page https://hibersense.com/access/view.  This data shall include Temperature, Motion, Humidity, and Light, along with any other data specific to that sensor.

FUN-VIEW-CHART - The chart on the View page ( https://hibersense.com/access/view) shall be adjustable to any time range.

FUN-TEMP-SCALE - There shall be a button on the page to switch between Fahrenheit and Celsius temperature scales.  After selecting 

FUN-TEMP-PAGE - The page at https://hibersense.com/access/temperature shall allow users to select their subjective assessment of the current temperature, which shall be one of the following options: Cold, Cool, Perfect, Warm, Hot.

FUN-SETTINGS - The Settings page ( https://hibersense.com/access/settings ) shall display the house for the user, along with its ID, name, location, number of occupants, safety and comfort ranges, and information for all thermostats in the building.

FUN-MENU-RIGHT - The menu on the right shall show all sensors available to that user.  Selecting a sensor shall show the appropriate data from that sensor.

### Turning in the Assignment

Put your final set of tests on a GitHub repository and include me as a collaborator.

Send me an email which includes a link to the GitHub repository and a short (1-2 paragraphs) description of your exploratory work  beforehand.

Be sure to include your name as well as the names of all people in your group.

This needs to be emailed to me by WEDNESDAY at 12:30 PM Eastern.  Note that this is the DAY BEFORE OUR NEXT CLASS.

If you find any defects, submit them using the "Provide Feedback" button at the top of the page.  Additionally, you must email me the defect you submitted (copy and paste).  Remember that defects can be violations of _implicit_ requirements!  All defects should be submitted using the standard defect template as discussed in class.  Final determination of whether or not something counts as a defect is at the sole discretion of the instructor.


### Grading

```
Description - 0.5 points
Selenium tests - 1.5 points
Valid defect filed (+0.5 each, limit 2 (i.e. max +1))
```