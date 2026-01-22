https://coursys.sfu.ca/2026sp-cmpt-473-e1/pages/WhiteBox
# White Box Testing
- Testing software where we can see inside the box and can actually look at the code.
- Code based test coverage

## Code Based Test Coverage
- how thoroughly the various logical elements within the software are exercised by the test suite. 
- 

## Control Flow Graphs
- Nodes represent code segments
- Edges represent control flow 
Node Type	Purpose	Incoming Edges	Outgoing Edges
Entry node	Identifies the entry point of a routine or code segment	0	1
Exit node	Identifies the exit point of a routine or code segment	1	0
Decision node	A node representing a control-flow choice (if, switch, ...)	1*	>1
Processing node	A node representing a simple statement or a straight-line segment of code (basic block)	*	1
Junction node	A node at which two or more control flow actions converge.	>1	1*

- Programs are modeled as graphs for flow
- used in testing and compiler optimizations
- nodes comprise the code of a program
- Edges show the paths that an execution may take through a program
- Entry nodes have 0 incoming edges
- Exit nodes have 0 outgoing edges
- Decision/branch nodes have >1 outgoing edges
- Join nodes



## Basic Structural Coverage: Statements and Branches
- statement covereage which is node coverage where coverage is testesd and basic statements
- Branch Coverage or edge coverage is the fraction of branches that are touched

## Recall Coverage/Adequacy
- How good is our test suite?
- Need to determine if a test suite covers/is adequate for our quality objectives

## Graph Coverage
- Why is graph coverage used? its easy to measure and do.
- path is a list of pairwise connected nodes.


## Statement Coverage -> Node Coverage
- Try to cover all reachable basic blocks
- Every basic part of the code is executed
- But sometimes we have code that cannot be reached during normal execution

## Branch Coverage -> Edge Coverage
- Edge coverage confirms node coverage but not vice versa
- Branchs

## In both of these things full coverage?
- Syntactic reachability is whether its reachable in its code like if something will never execute no matter what.
- Semantic Reachability - based on the meaning of the code.
- So relative degrees of coverage matter (40%? 80%?)

## Pragmatic Concerns
- Many branch coverage tools work only at if granularity
- Condition coverage can complement this but is also misleading
- The path taken by each path matters
- Other tools consider short circuits
- Stronger graph coverage criteria can help

## Is it reasonable to test all paths through the graph?
- Exponential effect of iteration where it can take many iterations
- Loop structure that could be infinite.

## Loop's are wacky
- What criteria do we use when testing loops?
- Simple paths
- No Node appears more than once in the path
- Prime paths are paths that are not a subpath
- More simple paths than prime paths
- I need to understand prime and simple paths in the context of testing. Lowkey confusing.
