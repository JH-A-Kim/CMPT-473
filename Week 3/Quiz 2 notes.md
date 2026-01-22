# Dynamic Quality Assesment

## Functional vs Non-functional Testing
- TLDR is Functional testing is focused on input output specifications. IE if something goes in the right thing comes out.
- Non-functional is something like maybe we reach the right end point but we take 30 million extra CPU cycles because it is poorly optimized. It is concerned with reliability and performance

## Defects
- Otherwise known as faults are flaws in the software that could cause issues

## Failures
- This is defined by some event when the program is running that is a deviation from the accepted behaviour that is way away from what it should be doing

## Latent Defects!
- This is where some defect lays hidden in the code for a long time because testing may not be able to detect these things.

## Test Oracle 
- What is it? The test oracle is the thing that decides whether a given test case produces the behaviour we want or not. This is usually an assertion like assertEquals or something along those lines
- For a very precise thing where an input always produces some output we can define it with simple unit testing 
- Test Driver is something that performs simple tests and is basically running the test. The test oracle is the verification component of the test.
- In regression testing the test oracle may be the file difference to assert 
- In some cases this test oracle is just a human being.

## Test Data Adequacy Criteria 
- But then how to find out when to stop testing
- What defines Adequacy?
- Some ways could be having a sufficient number of tests to address as many of the program properties as possible
- Lack of failures when using the test suite is another way to show its ready for delivery.

### But there are 2 common but inadequate answers lol
- Testing stops when you aint got time
- Testing stops when you aint got the moolah

### And how does it change depending on white box and black box?
- For White box you might check how much coverage of program statements and branchs
- Black box adequacy might look at how thorough the coverage of input specifications. So basically how many different types of inputs did we test. 

### Finally there is mutation adequacy criteria where we provide an independent assesment of tests.
- we create some amount of mutants that each differ ever so slightly (single insertion, deletion, replacement)
- Apply the tests to mutants
- determine number of mutants that fail at least one of the test cases
- The ratio of M/N can be used to measure test adequacy
- Could be equivalent mutants that should be removed.


# Fault Seeding and Mutation Adequacy

## Fault Seeding
- So what is it? Technique for evaluating how good the testing process is
- Faults are added into the code without informing testers and we see how many the testers detect.
- How many seeded faults were found can be used as a way to test how good the testing process is.
- If S is the total number of seeded faults and s(t) be the number of faults discovered at time t then s(t)/S is the effectivess of the test process given time t
- But doing this obviously leaves the risk of forgetting they are there :dead:

## Mutation Adequacy
- Pivoting to something else 
- Mutation Adequacy uses a similar concept as fault seeding
- Tests your tests
- Adequacy score is= # of mutants killed / Total mutants created (M)

### Automated Mutation: Mutation Operators
- Automation of creating mutants with some level of rule
Examples
- Add 1 -> adds 1 to some constant like q=0 becomes q=1
- Replace Variable -> replaces a variable with a different one of the same type like r=x becomes r=y
- Replace Operator -> Replaces an operator with a compatible on like q=q+1 becomes q=q-1

and many more!

## Mutation Theory
- First order mutants are where we change just one thing in the code
- Higher order mutants are where we change a sequence of things
- In the competent programmer hypothesis we assume programmers write good programs therefore a single mutation is good for realistic bug testing
- Coupling Effect -> complex errors combined with simple ones, a test suite that is sensitive enough to kill first-order mutants is also likely to kill higher-order mutants
- Equivalent mutants long story short same logic but slightly different in these cases we must do Test Suite=Killed/(mutants-equivalents)
- Mutation Based test Generation -> After mutant generation and testing live mutants may live. We can then make some tests or something to kill surviving mutants.

