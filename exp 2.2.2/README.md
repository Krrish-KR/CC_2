# CC-2-exp12 (24BDA70064)
## Problem Satement: 285 Inorder successor in BST 

class Solution:
    def inorderSuccessor(self, root, p):
        successor = None

        while root:
            if p.val >= root.val:
                root = root.right
            else:
                successor = root
                root = root.left

        return successor