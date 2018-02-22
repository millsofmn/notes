# Clean Code Note - Uncle Bob

## Names
1. Choose your names thoughtfully.
2. Communicate your intent.
3. Avoid Disinformation (a name should say what it means and mean what it says). 
   If you have to read the code to understand the name then that's a bad name.
4. Use Pronounceable Names.
5. Avoid Encodings.
   (Like Hungarian Notation we don't needs it anymore, they are distracting.)
6. Choose parse of Speech Well. The code should read like a sentence.
   - Give variables and classes noun names
	 - Give methods verb names
	 - Give booleans predicate names
7. Scope Rules:
   - If scope is small then use small names.
	 - If scope is large then use large names.
	 - Function names should be small if the scope is large.
	 - Function names should be large if the scope is small.
	 - Class names should be small when they are public.
	 - Class names should be large when they are private.
