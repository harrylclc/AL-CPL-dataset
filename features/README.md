## Feature Description
For each concept pair (A, B) in the "*.pairs" file, we calculate the following features:

ID | Feature
---| ---
0 | outd A
1 | outd B
2 | ind A
3 | ind B
4 | #cat A
5 | #cat B
6 | common neighbors
7 | common categories
8 | # A links to B
9 | # B links to A
10 | RefD
11 | A in B's first sent
12 | B in A's first sent
13 | B in A's title
14 | NGD
15 | \|In_A\cap In_B\|/\|In_A\|
16 | \|In_A\cap In_B\|/\|In_B\|
17 | wiki2vec sim
18 | BoW sim (1st par)
19 | docvec sim (1st par)',
20 | title jaccard
21 |PMI
22 | LDA entropy A
23 | LDA entropy B 
24 | LDA cross entropy A;B
25 | LDA cross entropy B;A
26 | # words A
27 | # words B'
28 | # B appears in A
29 | # A appears in B
30 | # B appears in A (norm)
31 | # A appears in B (norm)
32 | # noun phrases A
33 | # noun phrases B
34 | # common noun phrases
35 | Hub_A - Hub_B
36 | Auth_A - Auth_B
37 | PageRank_A - PageRank_B
