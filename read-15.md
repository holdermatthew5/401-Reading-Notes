## Trees

**Root** - first and highest node in a tree.
**Left/Right Child** - Respective child node in a tree.
**Edge** - Link between parent and child node.
**Leaf** - A node with no child nodes.
**Height** - Number of edges between Root and furthest Leaf.
**Search a tree:**
- **Breadth First** - Moving straight across nodes finishing each line of nodes befor continuing to the next.
- **Depth First** - Straight down then through every node to get to the opposite side.
  - **Pre-order:** root > left > right
  - **In-order:** left > root > right
  - **Post-order:** left > right > root
**BigO Time** - The Big O time complexity of a Binary Search Tree’s insertion and search operations is O(h), or O(height). In the worst case, we will have to search all the way down to a leaf, which will require searching through as many nodes as the tree is tall. In a balanced (or “perfect”) tree, the height of the tree is log(n). In an unbalanced tree, the worst case height of the tree is n.
**BigO Space** - The Big O space complexity of a BST search would be O(1). During a search, we are not allocating any additional space.