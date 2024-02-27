Types of binary trees
Tree terminology is not well-standardized and so varies in literatures.

A rooted binary tree has a root node and every node has at most two children.

A full binary tree

An ancestry chart which can be mapped to a perfect 4-level binary tree.
A full binary tree (sometimes referred to as a proper,[15] plane, or strict binary tree)[16][17] is a tree in which every node has either 0 or 2 children. Another way of defining a full binary tree is a recursive definition. A full binary tree is either:[11]
A single vertex (a single node as the root node).
A tree whose root node has two subtrees, both of which are full binary trees.
A perfect binary tree is a binary tree in which all interior nodes have two children and all leaves have the same depth or same level (the level of a node defined as the number of edges or links from the root node to a node).[18] A perfect binary tree is a full binary tree.
A complete binary tree is a binary tree in which every level, except possibly the last, is completely filled, and all nodes in the last level are as far left as possible. It can have between 1 and 2h nodes at the last level h.[19] A perfect tree is therefore always complete but a complete tree is not always perfect. Some authors use the term complete to refer instead to a perfect binary tree as defined above, in which case they call this type of tree (with a possibly not filled last level) an almost complete binary tree or nearly complete binary tree.[20][21] A complete binary tree can be efficiently represented using an array.[19]

A complete binary tree (that is not full)
In the infinite complete binary tree is a tree with 
ℵ
0
{\displaystyle {\aleph _{0}}} levels, where for each level d the number of existing nodes at level d is equal to 2d. The cardinal number of the set of all levels is 
ℵ
0
{\displaystyle {\aleph _{0}}} (countably infinite). The cardinal number of the set of all paths (the "leaves", so to speak) is uncountable, having the cardinality of the continuum.
A balanced binary tree is a binary tree structure in which the left and right subtrees of every node differ in height (the number of edges from the top-most node to the farthest node in a subtree) by no more than 1 (or the skew is no greater than 1).[22] One may also consider binary trees where no leaf is much farther away from the root than any other leaf. (Different balancing schemes allow different definitions of "much farther".[23])
A degenerate (or pathological) tree is where each parent node has only one associated child node.[24] This means that the tree will behave like a linked list data structure. In this case, an advantage of using a binary tree is significantly reduced because it is essentially a linked list which time complexity is O(n) (n as the number of nodes) and it has more data space than the linked list due to two pointers per node, while the complexity of O(log2n) for data search in a balanced binary tree is normally expected.
Properties of binary trees
The number of nodes 
�
{\displaystyle n} in a full binary tree is at least 
2
ℎ
+
1
{\displaystyle 2h+1} and at most 
2
ℎ
+
1
−
1
{\displaystyle 2^{h+1}-1} (i.e., the number of nodes in a perfect binary tree), where 
ℎ
{\displaystyle h} is the height of the tree. A tree consisting of only a root node has a height of 0. The least number of nodes is obtained by adding only two children nodes per adding height so 
2
ℎ
+
1
{\displaystyle 2h+1} (1 for counting the root node). The maximum number of nodes is obtained by fully filling nodes at each level, i.e., it is a perfect tree. For a perfect tree, the number of nodes is 
1
+
2
+
4
+
…
+
2
ℎ
=
2
ℎ
+
1
−
1
{\displaystyle 1+2+4+\ldots +2^{h}=2^{h+1}-1}, where the last equality is from the geometric series sum.
The number of leaf nodes 
�
{\displaystyle l} in a perfect binary tree is 
�
=
(
�
+
1
)
/
2
{\displaystyle l=(n+1)/2} (where 
�
{\displaystyle n} is the number of nodes in the tree) because 
�
=
2
ℎ
+
1
−
1
{\displaystyle n={{2}^{h+1}}-1} (by using the above property) and the number of leaves is 
2
ℎ
{\displaystyle 2^{h}} so 
�
=
2
⋅
2
ℎ
−
1
=
2
�
−
1
→
�
=
(
�
+
1
)
/
2
{\displaystyle n=2\cdot {{2}^{h}}-1=2l-1\to l=\left(n+1\right)/2}. It also means that 
�
=
2
�
−
1
{\displaystyle n=2l-1}. In terms of the tree height 
ℎ
{\displaystyle h}, 
�
=
(
2
ℎ
+
1
−
1
+
1
)
/
2
=
2
ℎ
{\displaystyle l=(2^{h+1}-1+1)/2=2^{h}}.
For any non-empty binary tree with 
�
{\displaystyle l} leaf nodes and 
�
2
{\displaystyle i_{2}} nodes of degree 2 (internal nodes with two child nodes), 
�
=
�
2
+
1
{\displaystyle l=i_{2}+1}.[25] The proof is the following. For a perfect binary tree, the total number of nodes is 
�
=
2
ℎ
+
1
−
1
{\displaystyle n=2^{h+1}-1} (A perfect binary tree is a full binary tree.) and 
�
=
2
ℎ
{\displaystyle l=2^{h}}, so 
�
=
�
−
�
=
(
2
ℎ
+
1
−
1
)
−
2
ℎ
=
2
ℎ
−
1
=
�
−
1
→
�
=
�
+
1
{\displaystyle i=n-l=(2^{h+1}-1)-2^{h}=2^{h}-1=l-1\to l=i+1}. To make a full binary tree from a perfect binary tree, a pair of two sibling nodes are removed one by one. This results in "two leaf nodes removed" and "one internal node removed" and "the removed internal node becoming a leaf node", so one leaf node and one internal node is removed per removing two sibling nodes. As a result, 
�
=
�
+
1
{\displaystyle l=i+1} also holds for a full binary tree. To make a binary tree with a leaf node without its sibling, a single leaf node is removed from a full binary tree, then "one leaf node removed" and "one internal nodes with two children removed" so 
�
=
�
+
1
{\displaystyle l=i+1} also holds. This relation now covers all non-empty binary trees.
With given 
�
{\displaystyle n} nodes, the minimum possible tree height is 
ℎ
�
�
�
=
log
2
⁡
(
�
+
1
)
−
1
{\displaystyle h_{min}=\log _{2}(n+1)-1} with which the tree is a balanced full tree or perfect tree. With a given heigh 
ℎ
{\displaystyle h}, the number of nodes can't exceed the 
2
ℎ
+
1
−
1
{\displaystyle 2^{h+1}-1} as the number of nodes in a perfect tree. Thus 
�
≤
2
ℎ
+
1
−
1
→
ℎ
≥
log
2
⁡
(
�
+
1
)
−
1
{\displaystyle n\leq 2^{h+1}-1\to h\geq \log _{2}(n+1)-1}.
A binary Tree with 
�
{\displaystyle l} leaves has at least the height 
ℎ
�
=
log
2
⁡
(
�
)
{\displaystyle h_{m}=\log _{2}(l)}. With a given height 
ℎ
{\displaystyle h}, the number of leaves at that height can't exceed 
2
ℎ
{\displaystyle 2^{h}} as the number of leaves at the height in a perfect tree. Thus 
�
≤
2
ℎ
→
ℎ
≥
log
2
⁡
(
�
)
{\displaystyle l\leq 2^{h}\to h\geq \log _{2}(l)}.
In a non-empty binary tree, if 
�
{\displaystyle n} is the total number of nodes and 
�
{\displaystyle e} is the total number of edges, then 
�
=
�
−
1
{\displaystyle e=n-1}. This is obvious because each node requires one edge except for the root node.
The number of null links (i.e., absent children of the nodes) in a binary tree of n nodes is (n + 1).
The number of internal nodes in a complete binary tree of n nodes is 
⌊
�
/
2
⌋{\displaystyle \lfloor n/2\rfloor }.
