- Markdown
   - [语法](https://www.jianshu.com/p/191d1e21f7ed/)
   
- redis

- mysql

- java常用语法  
  
```
  //获取字符串
  String a = "asd";
  char key = a.charAt(i);

  //map 使用
  //是否包含
  if(map.containsKey(key)){
  }

  Map<Character, Integer> map = new HashMap();
  for(Integer num:map.values()){    
  }
```

- 好的资源
   - https://github.com/CyC2018/CS-Notes
   - [敖丙](https://github.com/AobingJava/JavaFamily)
   - [涛哥](https://github.com/songtao110/precipitation)
   - [代码随想录](https://github.com/youngyangyang04/leetcode-master)
- 算法
   - [刷题目录](https://github.com/CyC2018/CS-Notes/blob/master/notes/Leetcode%20%E9%A2%98%E8%A7%A3%20-%20%E7%9B%AE%E5%BD%95.md)
   - 推荐的学习频道👍🏻
      - [Youtube ：Back To Back SWE](https://www.youtube.com/channel/UCmJz...)
   - B站：
      - [花花酱](https://space.bilibili.com/9880352?fr...)
      - [小Q刷题](https://space.bilibili.com/149758?fro...)
      - [绵羊教授](https://space.bilibili.com/354892788?...)

- 刷题目录
   - 哈希表
      - 考察map的使用 
      - [有效的字母异位词](https://leetcode-cn.com/problems/valid-anagram/)
      ``` 
        public boolean isAnagram(String s, String t) {
              if(s.length() != t.length())
                  return false;
              int[] alpha = new int[26];
              for(int i = 0; i< s.length(); i++) {
                  alpha[s.charAt(i) - 'a'] ++;
                  alpha[t.charAt(i) - 'a'] --;
              }
              for(int i=0;i<26;i++)
                  if(alpha[i] != 0)
                      return false;
              return true;
          }
      ```  
      - [字母异位词分组](https://leetcode-cn.com/problems/group-anagrams/)  
      - [两数之和](https://leetcode-cn.com/problems/two-sum/)
      
   - 树
      - [二叉搜索树 Demo](https://visualgo.net/zh/bst)
         - 左子树所有节点小于根结点，右子树大于根节点
      - [前序遍历](https://leetcode-cn.com/problems/binary-tree-inorder-traversal/solution/er-cha-shu-de-zhong-xu-bian-li-by-leetcode-solutio/)
         - 循环遍历，利用栈，先将根节点压入栈中，然后左节点，循环至左节点为null, 然后将栈弹出一个节点。
         - 递归遍历 

         解释一下为什么需要“右子节点、自身、左子节点依次入栈”
         我们有一棵二叉树：

                        中
                       /  \
                      左   右
         前序遍历：中，左，右
         中序遍历：左，中，右
         后序遍历：左，右，中

         本题需要中序遍历。

         栈是一种 先进后出的结构，出栈顺序为左，中，右
         那么入栈顺序必须调整为倒序，也就是右，中，左

         同理，如果是前序遍历，入栈顺序为 右，左，中；后序遍历，入栈顺序中，右，左
      - [前序遍历](https://leetcode-cn.com/problems/binary-tree-preorder-traversal/)
      ``` 
        public List<Integer> preorderTraversal(TreeNode root) {
            List<Integer> res = new ArrayList();
            Stack<TreeNode> stack = new Stack();
            stack.add(root);
            while(!stack.empty()){
               TreeNode node = stack.pop();
               res.add(node.val);
               if(node.right != null){
                   stack.add(node.right);
               }
               if(node.left != null) {
                   stack.add(node.left);
               }
            }   
            return res; 
      }
      ``` 
     - 颜色标记法
     ``` 
      public class ColorNode{
        String color;
        TreeNode node;
        ColorNode(TreeNode node, String color){
            this.node = node;
            this.color = color;
        }
    }

    public List<Integer> inorderTraversal(TreeNode root) {
        if(root == null) {
            return new ArrayList();
        }
        List<Integer> res = new ArrayList();
        Stack<ColorNode> stack = new Stack();
        stack.add(new ColorNode(root, "white"));

        while(! stack.empty()){
            ColorNode cn = stack.pop();
            if(cn.color.equals("white")) {
                if(cn.node.right != null) stack.add(new ColorNode(cn.node.right, "white"));
                stack.add(new ColorNode(cn.node, "gray"));
                if(cn.node.left != null) stack.add(new ColorNode(cn.node.left, "white"));
            } else {
                res.add(cn.node.val);
            }
        }

        return res; 
    }
    ``` 
 
   
