## Exercise 5 - Combinatorial Testing

In this exercise, you will write a combinatorial test plan to see which Firefly characters can get together on a scout ship and accomplish their mission.

Using the same technique as we used for creating a three-element combinatorial test, develop a 2-way, four-element combinatorial test.  That is, your test cases should check for all possible pairs of the four characters.

There is no need to write out individual test cases (as in Deliverable 1).  You can simply use 1 and 0 in the covering matrix to show which characters are being sent out on the scout ships.

Download the Firefly.class file.  You may run it by typing `java Firefly`.  Simply type the letters of the characters who are going on the mission: i for Inara, m for Mal, k for Kaylee, and w for Wash.  Note that these are case-insensitive (i.e., you may type `W` or `w` for Wash).

For each group of characters, the mission may or may not be successful.  An unsuccessful mission is NOT an error.  Errors will consist of an exception being thrown along with the message "ERROR ERROR ERROR".  There are two errors which you must find.

Examples:

In the first run, Kaylee and Inara go on the mission, and Mal and Wash do not.  In the second run, Kaylee, Mal, and Wash go on the mission, and Inara does not.

```
penelope:5 laboon$ java Firefly k i
Going scouting:
Inara: true
Mal: false
Kaylee: true
Wash: false
Mission was not a success!

penelope:5 laboon$ java Firefly m k w
Going scouting:
Inara: false
Mal: true
Kaylee: true
Wash: true
Mission successful!
```



Email me the final set of tests and whichever test cases failed, along with their error messages.  Based on this information, which two true/false pairings are problematic?  Note that a "pairing" may also involve a negative, e.g., a mission may fail because one haracter goes and another does _not_ go.

## Grading

```
Covering matrix: 1 point
Errors found: 0.5 point
Problematic Pairings reported: 0.5 point
```