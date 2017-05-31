FUN-COUNTER: The internal counter for the program shall start at 0.  The counter shall not be displayed to the user, except indirectly through taking 

FUN-INCREMENT-COUNTER: Upon the program cursor encountering the character `i`, the internal counter shall be incremented by one.

FUN-DECREMENT-COUNTER: Upon the program cursor encountering the character `d`, the internal counter shall be decremented by one.

FUN-TAKE-VALUE-COUNTER: Upon the program cursor encountering the character `t`, the value of the internal counter shall be pushed to the stack.

FUN-REVERSE-STACK: Upon the program cursor encountering the character `r`, the stack shall be reversed (e.g., if the stack was `[1, 2, 3]`, after this command it would be `[3, 2, 1]`).  The GUI shall display the updated value of the stack in the Program Stack area immediately after reversing it.

FUN-COMMENTS: Upon the program cursor encountering the character `(`, the program cursor shall continue moving in the same direction as it had been, but it shall ignore any opcodes, including `(`, until it encounters a close comment character, `)`.  Comments cannot be nested (e.g., `((((()` is one comment).
