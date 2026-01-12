# Software Quality Assurance (tldr) 

## https://coursys.sfu.ca/2026sp-cmpt-473-e1/pages/

### What will be the course about?
- What makes software good or bad ie: User Perspective, IT Team Perspective (Operational Perspective), Developer Perspective.
(Could be bad for a developer if it is difficult to extend? How easy is it to read? These are just a few examples) 
- Learn about the software quality standards ISO:
Functionality
Reliability
Usability
Efficiency
Maintainability
Portability
Security 
Compatibility
Can be further broken down into sub-characteristics
- Quality Metrics IE ways to come up with suitable ways to assess these quality characteristics.

- Broadly its about software quality and security.

## Software Process
- Testing repeatability
- Automated testing and manual testing (code checks, code reviews, etc)
- Creating a level of predictability in all things. We make one thing? We can use those metrics to predict the next project. Big.

## Software Testing
- Functional Testing (input, output testing)
- Non-Functional Testing (performance, reliability)
- Defects and Failures

Failure is a big problem that happens during program execution that go away from acceptable behavior
Latent Defects are defects that remain in systems for a long period of time that has been failed to notice.

### Test Oracle
- Tests outcomes - can be human, unit tests, integration tests.
- Something to determine whether a test passed or failed. 

### How do you know that you have done enough testing?
- Test data adequacy criteria ie. Success Criteria
- Stop Testing when you are out of time lol.
- When you run out of money is one stopping criteria. Not really principled criteria though.
- Coverage is one way: Black Box (input output only knowledge, covering all input cases, no knowledge of inside) and White Box (We look at actual software and provide inputs and make sure all paths of the program are reached)
- Mutation Adequacy Criteria (Assignment 1 important) - What does this mean?

### Mutation Adequacy Criteria
- We create mutants with individual changes of insertion, deletion, or replacement of code. Each has a small bug
- We create tons of mutants, and each copy has one change. How many of these mutants find a bug. If it finds tons of bugs then your test suite is good. If it does not then it is just cooked.
- These mutants are changes to the actual code itself like a > to >= and if it lets the mutant live then it's a problem.


## Fault Seeding
- Testing the effectiveness of a testing process
- We introduce defects intentionally into the software and see if they are found.
- This can show the effectiveness of the system.

### Mutation Theory
- First order Mutation is changing one thing from the original code
- Higher order Mutation is changing a series of things from the original code.
- Equivalent Mutants is where the code might have changed syntactically but the functionality of the code does not change so evaluating from this becomes meaningless because it will always output the same thing as the original code.

Original 
```
x+y
```

Equivalent Mutant
```
x+y+0
```

