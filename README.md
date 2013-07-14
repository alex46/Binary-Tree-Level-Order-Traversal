Binary-Tree-Level-Order-Traversal
=================================

/**
 * Definition for binary tree
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode(int x) { val = x; }
 * }
 */
 
public class Solution {
    public ArrayList<ArrayList<Integer>> levelOrder(TreeNode root) {
        // Start typing your Java solution below
        // DO NOT write main() function
        ArrayList<ArrayList<Integer>> result = new ArrayList<ArrayList<Integer>>();
        
       
        
        if(root == null) return result;
        
        ArrayList<TreeNode> toVisit = new ArrayList<TreeNode>();
        
        toVisit.add(root);
        
       
        
       while(!toVisit.isEmpty()){
       ArrayList<Integer> a = new ArrayList<Integer>();
            
       ArrayList<TreeNode> temp = new ArrayList<TreeNode>();
            
        for(int i = 0; i < toVisit.size();i++){
            a.add(toVisit.get(i).val);
        }
            
        result.add(a);
        
        for(int i = 0; i < toVisit.size();i++){
            TreeNode node = toVisit.get(i);
        
        if(node.left!=null) {
        temp.add(node.left);
        }
         
        if(node.right!=null) {
        temp.add(node.right);
        }
        }
        
        toVisit = temp;
        
        
        
    }
    return result;
    }
}
