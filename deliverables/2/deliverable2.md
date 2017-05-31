# CS 1632 - Software Quality Assurance

### Summer Semester 2017

Due 20 June 2017

## Deliverable 2

For this assignment, you (not a group) will implement several new features and unit tests for JBefunge, creating the next generation of Befunge programming - Befunge++.  These features will include the commands 'i' (increment counter), 'd' (decrement counter), 't' (take value from counter), 'r' (reverse stack), and '(' and ')' (comment / end comment).  

Specific requirements for this program are in the requirements.md file in this directory.  Sample output is also provided for several runs of the program.  In case of ambiguity, please see the sample output in `samples.md` as an example of what the final stack and output should be.  Unlike the manual testing test plan, you do not need to map your unit tests to the requirements.  You should use some exploratory testing to ensure that the system meets all of the requirements, but the focus in this deliverable is to use unit testing to test the methods you have added.

All code and tests should be on GitHub in a _private_ repository accessible to me.  Be sure you do NOT create a public repository.

## Format
You should turn in a title page with:
* Your name
* The URL of your code and tests on GitHub
* The title "CS 1632 - DELIVERABLE 2: Unit Testing"

ENSURE THAT NANNAN (THE TA) AND I ARE ADDED AS A COLLABORATOR AND CAN CLONE YOUR REPOSITORY!  My username is laboon on both GitHub.  The TA's username is NannanWen.  You will lose an automatic 10 points if either I or the TA cannot access your repository.

Add a short ( < 1 page ) description of issues you faced when writing this code and tests.  If any tests you wrote fail, they should be included here, along with why you think that they are failing. 

After this, ON A SEPARATE PAGE, include a screen shot of the executed unit tests.    If a test doesn't pass, it should be included in the concerns section above.  Ideally, all tests should be green (passing).  However, if you have what you think is a valid test and it is not passing, I would prefer that you include a note (and perhaps comment out the tests) rather than just deleting it.  Knowing that a defect exists and reporting it is much better than having it discovered by the customer (me)!

There is no need to print out the code.  It should be on GitHub (or GitLab) BY THE BEGINNING OF CLASS.

At least three (3) unit tests should use test doubles and/or mocks.

At least three (3) unit tests should use stubbing of methods.

I expect unit tests for all methods that you add, using a variety of assertions and looking at different failure modes and edge cases.  You should make all methods that you add public.  Keep in mind some of the things we learned when doing manual testing; you should be cognizant of equivalence classes, boundary values, etc. etc., and focus on them.  There should be, at an absolute bare minimum, 20 unit tests.  You will most likely require more if you perform good object-oriented design.

I warn you, write tests as you write methods!  Do not try to write the whole program and then write tests for it afterwards.  You will write untestable code and may need to rewrite major parts of your program.  Trust me on this one!  Testing is not something that should be done after development is complete.

The program should use appropriate object-oriented design.  Do not attempt to do this entirely with static methods and variables, without classes, etc.  It is, of course, possible but will make testing more difficult!

Before each test, add some comments (two or three sentences, on average) explaining what the test is checking.  For example...

```java
	// Two LLs with different sizes should never be equal.
	// Create two linked lists, both of which have the same value in the initial node,
	// but one has several more nodes. 
	// They should not be equal to each other.
		@Test
		public void testNotEqualsDiffSizes() {
			LinkedList<Integer> ll11 = new LinkedList<Integer>();
			LinkedList<Integer> ll_3elems = new LinkedList<Integer>();

			ll11.addToFront(new Node<Integer>(new Integer(1)));
			ll_3elems.addToFront(new Node<Integer>(new Integer(3)));
			ll_3elems.addToFront(new Node<Integer>(new Integer(2)));
			ll_3elems.addToFront(new Node<Integer>(new Integer(1)));

			assertFalse(ll_3elems.equals(ll11));
		}
```

## Grading
I remind you that grammar and good code count as well as functionality.  By good code, I mean -

No commented-out code unless there's an EXPLICIT reason, e.g.
```java
// I couldn't get this assertion to work, but instead used a different assertion, below
// assertEquals(foo, 3);
assertTrue(foo == 3);
```

Properly indented code, e.g.
```java
public void doSomething() {
    doStuff();
}
```
NOT
```java
public
  void
                     doSomething()
{ doStuff(); }
```

Don't misspell words or use bad grammar, in comments or summaries.

For this project, you should endeavour to get a good sampling of different equivalence classes and success/failure cases.

## Befunge++

## Grading Breakdown
* Summary and Testing Concerns- 5%
* Screenshot of executed unit tests - 5%
* Program Code - 45%
* Test Code - 45%

Please feel free to email me or come to office hours to discuss any problems you have. 
 