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
         - 循环遍历，利用栈
         - 递归遍历 

 
   
