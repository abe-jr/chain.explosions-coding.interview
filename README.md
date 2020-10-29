# chain.explosions-coding.interview

Dynamite is an effective tool for clearing ice to allow logs to flow downstream in the great Canadian log drive. But as every Canadian knows, successful use of dynamite requires a certain finesse. Logan the logging director is planning to hook up a network of dynamite sticks using fuse wires so that they may be detonated from afar.
Logan would like to use at most 2000 sticks of dynamite and at most 2000 fuse wires to build his dynamite network at a certain job site. He'll number the sticks from 11 to NN, and the wires from 11 to MM (for some NN and MM of his choice). Each fuse wire is used to connect two different sticks of dynamite together. No two fuse wires may be used to connect the same unordered pair of sticks. The resulting dynamite network must all be connected (that is, it must be possible to reach each dynamite stick from each other stick by following a sequence of connected wires and sticks).
There's just one problem: sticks of dynamite are not individually powerful enough to break the thick ice. Logan must rely on chain explosions to amplify the dynamite's power. A potential chain explosion can occur anywhere in Logan's network where there is an ordered triple (a, b, c)(a,b,c) of distinct sticks of dynamite such that sticks aa and bb are connected by a fuse wire, as are sticks bb and cc. Logan would like to build a network with exactly KK potential chain explosions, where KK is an even integer. Any less than KK, and there might not be enough ice-breaking power; any more than KK, and he risks damaging the logs.
Help Logan bust some ice by constructing any valid dynamite network for the given value of KK. Please note that at least one valid network exists for each possible valid value of KK.
Constraints
1 \le T \le 1001≤T≤100
2 \le K \le 2,000,0002≤K≤2,000,000
KK is even
The sum of KK across all job sites is at most 10,000,000.
Input
Input begins with an integer TT, the number of job sites. For each job site, there is a line containing a single integer KK.
Output
For the iith job site, print a line containing "Case #i: ", followed by 2 integers NN and MM, the number of sticks of dynamite and fuse wires your network will use (1 \le N, M \le 2000)(1≤N,M≤2000). After that, print MM more lines, the jjth of which contains 2 integers A_jA 
j
​	  and B_jB 
j
​	 , the two sticks of dynamite connected by the jjth fuse wire (1 \le A_j, B_j \le N, A_j \ne B_j)(1≤A 
j
​	 ,B 
j
​	 ≤N,A 
j
​	 ≠B 
j
​	 ).
Explanation of Sample
Note: For each job site, other outputs would also be accepted.
For the first job site, the chosen network (depicted below) has exactly 2 potential chain explosions (involving dynamic stick triples (1, 2, 3)(1,2,3) and (3, 2, 1)(3,2,1)), as required.

For the second job site, the chosen network (depicted below) has exactly 6 potential chain explosions (involving sticks (1, 2, 3)(1,2,3), (1, 3, 2)(1,3,2), (2, 1, 3)(2,1,3), (2, 3, 1)(2,3,1), (3, 1, 2)(3,1,2), and (3, 2, 1)(3,2,1)).

The following output would not be accepted, due to having a fuse wire connecting a stick of dynamite to itself (stick 3) and having two fuse wires connecting the same unordered pair of dynamite sticks (sticks 1 and 2):
3 5
1 2
2 1
2 3
3 3
3 1
The following output would also not be accepted, due to the dynamite network not being connected:
7 5
1 2
2 3
3 4
5 6
6 7
For the third job site, the chosen network is as follows:
