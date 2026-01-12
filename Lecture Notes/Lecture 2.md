# Testing 

Kill a test suite if it fails the test

## Assignment 1: Group Project due date: Tuesday, January 27th, 2026
- Open Source project
- has to have existing test suite 
- test with mutants to see how it effects things. Create like 100 mutants. Create a script. 
- Show the diff files for each thing
- Improve the test suite. 
- Find the test that kills the mutant and see how we can improve it.
- Parabix-devel (Professors open-source project) can be a potential project but look at google summer of code 2025 for open source project contributions. 

## Quiz 1: Readings from Beautiful Testing: Due in one week so start reading like Saturday?
- First chapter
- Keep some notes
- In class, could be on paper or on computer. 


## Actual Lecture Stuff

### Cobalt and Fortran
- Language
- Mutation operators named and defined in these languages. (look at the long ass list from Coursys: https://coursys.sfu.ca/2026sp-cmpt-473-e1/pages/MutationOperators)


### Too Many Mutants?
- Cost of compiling mutants is high because we need to compile every time we make a small change
- 10K mutants is like crazy numbers

### Reducing the number of mutants
- To reduce it we can just run the first few to see if we only kill like 8 out of the first 100 then there is a serious issue and we do not need to run the rest of them.


### Strong vs Weak Mutations
- Strong mutations are producing different outputs that fail to pass the test cases
- Weak mutations simply produce a different output but don't fail the test cases

### Dealing with Equivalent Mutants
- Usually you need a human to see if a test is equivalent or not
- slow and potentially error-prone
- we can use a few automated techniques such as a trivial compiler equivalence if many equivalent mutants are produced exactly the same object code as the PUT and are therefore known to be equivalent.
- LLM's also been looking at becoming the test oracle but not super reliable at the moment.

### Research in Mutation Testing
- Mutation Testing for energy awareness (non-functional, does an app use too much energy?)
- Focused Mutation Testing on change sets (Deltas) (focuses the mutation testing on only the changes made.)

