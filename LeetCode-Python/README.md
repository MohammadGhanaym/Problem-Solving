## Table of Contents
<li><a href="#Two Sum">Two Sum</a></li>
<li><a href="#Palindrome Number">Palindrome Number</a></li>
<li><a href="#Roman to Integer">Roman to Integer</a></li>
<li><a href="#Longest Common Prefix">Longest Common Prefix</a></li>
<li><a href="#Valid Parentheses">Valid Parentheses</a></li>
<li><a href="#Merge Two Sorted Lists">Merge Two Sorted Lists</a></li>
<li><a href="#Remove Duplicates from Sorted Array">Remove Duplicates from Sorted Array</a></li>
<li><a href="#Remove Element">Remove Element</a></li>
<li><a href="#Search Insert Position">Search Insert Position</a></li>
<li><a href="#Length of Last Word">Length of Last Word</a></li>
<li><a href="#Plus One">Plus One</a></li>
<li><a href="#Add Binary">Add Binary</a></li>
<li><a href="#Sqrt(x)">Sqrt(x)</a></li>
<li><a href="#Climbing Stairs">Climbing Stairs</a></li>
<li><a href="#Remove Duplicates from Sorted List">Remove Duplicates from Sorted List</a></li>
<li><a href="#Merge Sorted Array">Merge Sorted Array</a></li>
<li><a href="#q_28">28. Find the Index of the First Occurrence in a String</a></li>
<li><a href="#bt_inorder_traversal">Binary Tree Inorder Traversal</a></li>
<li><a href="#Same_Tree">Same Tree</a></li>
<li><a href="#Symmetric_Tree">Symmetric Tree</a></li>
<li><a href="#Maximum_Depth_of_Binary_Tree">Maximum Depth of Binary Tree</a></li>
<li><a href="#Convert__Array_to_Binary_Search_Tree">Convert Sorted Array to Binary Search Tree</a></li>
<li><a href="#Balanced_Binary_Tree">Balanced_Binary_Tree</a></li>
<li><a href="#Minimum_Depth_of_Binary_Tree">Minimum_Depth_of_Binary_Tree</a></li>
<li><a href="#Path_Sum">Path_Sum</a></li>
<li><a href="#Pascal's_Triangle">Pascal's_Triangle</a></li>
<li><a href="#Pascal's_Triangle_II">Pascal's_Triangle_II</a></li>
<li><a href="#Valid_Palindrome">Valid_Palindrome</a></li>
<li><a href="#Single_Number">Single_Number</a></li>
<li><a href="#Linked_List_Cycle">Linked_List_Cycle</a></li>
<li><a href="#Binary_Tree_Preorder_Traversal">Binary_Tree_Preorder_Traversal</a></li>
<li><a href="#Binary_Tree_Postorder_Traversal">Binary_Tree_Postorder_Traversal</a></li>
<li><a href="#Intersection_of_Two_Linked_Lists">Intersection_of_Two_Linked_Lists</a></li>
<li><a href="#Excel_Sheet_Column_Title">Excel_Sheet_Column_Title</a></li>
<li><a href="#Majority_Element">Majority_Element</a></li>
<li><a href="#Excel_Sheet_Column_Number">Excel_Sheet_Column_Number</a></li>
<li><a href="#Combine_Two_Tables">Combine_Two_Tables</a></li>
<li><a href="#Employees_Earning_More_Than_Their_Managers">Employees_Earning_More_Than_Their_Managers</a></li>
<li><a href="#Duplicate_Emails">Duplicate_Emails</a></li>
<li><a href="#Customers_Who_Never_Order">Customers_Who_Never_Order</a></li>
<li><a href="#Reverse_Bits">Reverse_Bits</a></li>
<li><a href="#Number_of_1_Bits">Number_of_1_Bits</a></li>
<li><a href="#Missing_Number">Missing_Number</a></li>
<li><a href="#Intersection_of_Two_Arrays_II">Intersection_of_Two_Arrays_II</a></li>
<li><a href="#Count_Complete_Tree_Nodes">Count_Complete_Tree_Nodes</a></li>
<li><a href="#Happy_Number">Happy_Number</a></li>
<li><a href="#Reverse_Linked_List">Reverse_Linked_List</a></li>
<li><a href="#Contains_Duplicate">Contains_Duplicate</a></li>
<li><a href="#Palindrome_Linked_List">Palindrome_Linked_List</a></li>
<li><a href="#Valid_Anagram">Valid_Anagram</a></li>
<li><a href="#Move_Zeroes">Move_Zeroes</a></li>
<li><a href="#Power_of_Three">Power_of_Three</a></li>
<li><a href="#Reverse_String">Reverse_String</a></li>
<li><a href="#First_Unique_Character_in_a_String">First_Unique_Character_in_a_String</a></li>
<li><a href="#Fizz_Buzz">Fizz_Buzz</a></li>
<li><a href="#H-Index">H-Index</a></li>
<li><a href="#Insert_Delete_GetRandom_O(1)">Insert_Delete_GetRandom_O(1)</a></li>
<li><a href="#Product_of_Array_Except_Self">Product_of_Array_Except_Self</a></li>
<li><a href="#Gas_Station">Gas_Station</a></li>
<li><a href="#First_Bad_Version">First_Bad_Version</a></li>
<li><a href="#Intersection_of_Two_Arrays">Intersection_of_Two_Arrays</a></li>
<li><a href="#Remove_Linked_List_Elements">Remove_Linked_List_Elements</a></li>
<li><a href="#Power_of_Two">Power_of_Two</a></li>
<li><a href="#Concatenation_of_Array">Concatenation_of_Array</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>
<li><a href="#Write_Here">Write_Here</a></li>


```python
input().replace(' ', '_')
```

     1929. Concatenation of Array
    




    '1929._Concatenation_of_Array'




```python
# Provided ListNode class
class ListNode:
    def __init__(self, x):
        self.val = x  # Value stored in the node
        self.next = None  # Reference to the next node (initially None)

# Function to build a singly linked list from a Python list
def build_linked_list_from_list(input_list):
    """
    Build a singly linked list from a Python list.
    Args:
        input_list (list): The list of elements to convert into a linked list.
    Returns:
        ListNode: The head of the constructed linked list.
    """
    if not input_list:  # If the input list is empty, return None
        return None

    # Create the head of the linked list
    head = ListNode(input_list[0])
    current = head

    # Iterate through the remaining elements in the list
    for value in input_list[1:]:
        current.next = ListNode(value)  # Create a new node and link it
        current = current.next  # Move to the new node
    
    return head  # Return the head of the linked list

# Function to display the linked list
def display_linked_list(head):
    """
    Display the linked list as a string.
    Args:
        head (ListNode): The head of the linked list.
    """
    elements = []
    current = head
    while current:
        elements.append(str(current.val))  # Add each node's value to the list
        current = current.next
    print(" -> ".join(elements))  # Print the linked list as a string
```


```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```


```python
def build_tree(level_order):
    if not level_order:
        return None
    
    # Create the root node
    root = TreeNode(level_order[0])
    queue = [root]
    i = 1
    
    # Use a queue to construct the tree level by level
    while queue and i < len(level_order):
        current_node = queue.pop(0)
        
        # Left child
        if i < len(level_order) and level_order[i] is not None:
            current_node.left = TreeNode(level_order[i])
            queue.append(current_node.left)
        i += 1
        
        # Right child
        if i < len(level_order) and level_order[i] is not None:
            current_node.right = TreeNode(level_order[i])
            queue.append(current_node.right)
        i += 1
    
    return root
```

<a id='Two Sum'></a>
### Two Sum


```python
def twoSum(nums, target):
    idx1 = 0
    idx2 = idx1 + 1
    nums_size = len(nums)
    while idx1 < nums_size - 1:
        if nums[idx1] + nums[idx2] == target:
            return [idx1, idx2]
        else:
            if idx2 == nums_size - 1:
                idx1 = idx1 + 1
                idx2 = idx1 + 1
            else:
                idx2 = idx2 + 1
                
            continue
    return []
```


```python
print(twoSum([2,7,11,15], 9))
```

    [0, 1]
    


```python
print(twoSum([3, 3], 6))
```

    [0, 1]
    


```python
print(twoSum([3, 2, 4], 6))
```

    [1, 2]
    


```python
print(twoSum([3, 2, 3], 6))
```

    [0, 2]
    

<a id='Palindrome Number'></a>
### Palindrome Number



```python
def isPalindrome(x):
    x = str(x)
    if x == x[::-1]:
        return True
    return False
```


```python
def isPalindrome(x):
    x = str(x)
    return x == x[::-1]
```


```python
val = int(input())
print(isPalindrome(val))
```

    121
    True
    

<a id='Roman to Integer'></a>
### Roman to Integer


```python
def romanToInt(s):
    roman_symbols = {'I':1, 'V':5, 'X':10, 'L':50, 'C':100, 'D':500, 'M':1000}
    sub_roman = {'IV':4, 'IX':9, 'XL':40, 'XC':90, 'CD':400, 'CM':900}
    num = 0
    while len(s) >= 2:
        if s[:2] in sub_roman.keys():
            num = num + sub_roman.get(s[:2])
            s = s[2:]
        else:
            num = num + roman_symbols.get(s[0])
            s = s[1:]
    
    if s:
        num = num + roman_symbols.get(s)
    return num 
    
```


```python
print(romanToInt("MCDLXXVI")) # 1476
```

    1476
    

<a id='Longest Common Prefix'></a>
### Longest Common Prefix


```python
def longestCommonPrefix(strs):
    '''
    This function takes a list of strings and return the longest common prefix among these strings
    '''
    prefix = 0
    check=False
    strs_sorted = sorted(strs, key=lambda x:len(x))
    print(strs_sorted)
    while not check:
        if strs_sorted[0] == "" or len(strs_sorted) == 1:
            return strs_sorted[0]
        else:
            s0 = strs_sorted[0][prefix]
        for s in strs_sorted[1:]:
            if s != "":
                if s[prefix] == s0:
                    check = False
                else:
                    check = True
                    break
            else:
                return ""
            
        if not check:
            prefix = prefix + 1
            
        if prefix == len(strs_sorted[0]):
            break
            
    if prefix == 0:
        return ""
    else:
        return strs[0][:prefix]
```


```python
longestCommonPrefix(['flower', 'flow', 'flight'])
```

    ['flow', 'flower', 'flight']
    




    'fl'




```python
def longestCommonPrefix(strs):
    prefix = ""
    size = len(sorted(strs, key=lambda x:len(x))[0])
    
    for idx in range(size):
        demo = []
        for s in strs:
            demo.append(s[idx])
        if len(set(demo)) == 1:
            prefix += demo[0]
            
        else:
            break
            
    return prefix
```


```python
longestCommonPrefix(['flower', 'flow', 'flight'])
```




    'fl'



<a id='Valid Parentheses'></a>
### Valid Parentheses


```python
def isValid(s):
        if len(s) % 2 != 0:
            return False

        stack = []
        for char in s:
            if char in ['{', '(', '[']:
                stack.append(char)
            else:
                if not stack:
                    return False
                left_brace = stack.pop()
                if left_brace == '{' and char == '}':
                    continue
                elif left_brace == '(' and char == ')':
                    continue
                elif left_brace == '[' and char == ']':
                    continue
                else:
                    return False
                
        if stack:
            return False
        return True
```


```python
def isValid(s):
    if len(s) % 2 != 0:
        return False
    stack = []
    for char in s:
        if char in ['{', '(', '[']:
            stack.append(char)
        elif char == '}' and stack and stack[-1] == '{':
            stack.pop()
        elif char == ')' and stack and stack[-1] == '(':
            stack.pop()
        elif char == ']' and stack and stack[-1] == '[':
            stack.pop()
        else:
            return False
    
    if stack:
        return False
    return True
```


```python
print(isValid('{}()[]'))
print(isValid('{([])}'))
print(isValid('{[]{}}'))
print(isValid('{()}()'))
print(isValid('[]{}()()'))
print(isValid("((}}"))
print(isValid("()]"))
```

    True
    True
    True
    True
    True
    False
    False
    

<a id='Merge Two Sorted Lists'></a>
### Merge Two Sorted Lists


```python
#Definition for singly-linked list.
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next        
```


```python
def forward_linked_list(size):
    head = None
    last = None
    
    while size > 0:
        val = int(input())
        newNode = ListNode(val)
        if head == None:
            head = newNode
            last = newNode
        else:
            last.next = newNode
            last = newNode
            
        size = size - 1
    return head
```


```python
def display_linked_list(head):
    current = head
    while current:
        print(current.val, end=' ')
        if current.next:
            print(' --> ', end=' ')
        current = current.next
```


```python
list1 = forward_linked_list(3)
```

    1
    2
    4
    


```python
display_linked_list(list1)
```

    1  -->  2  -->  4 


```python
list2 = forward_linked_list(3)
```

    1
    3
    4
    


```python
display_linked_list(list2)
```

    1  -->  3  -->  4 


```python
def mergeTwoLists(list1, list2):
    if list1 == None and list2:
        return list2
    elif list1 and list2 == None:
        return list1
    elif list1 == None and list2 == None:
        return None
    
    # merge lists
    new_list = []
    current1 = list1
    while current1:
        new_list.append(current1.val)
        current1 = current1.next
        
    current2 = list2
    while current2:
        new_list.append(current2.val)
        current2 = current2.next
        
    # sort list
    new_list = sorted(new_list)
    head = None
    last = None
    for item in new_list:
        newNode = ListNode(item)
        if head == None:
            head = newNode
            last = newNode
        else:
            last.next = newNode
            last = newNode
    return head
```


```python
newlist = mergeTwoLists(list1, list2)
display_linked_list(newlist)
```

    1  -->  1  -->  2  -->  3  -->  4  -->  4 

<a id='Remove Duplicates from Sorted Array'></a>
### Remove Duplicates from Sorted Array


```python
def removeDuplicates(nums):
    idx = 1
    while True:
        if len(nums) >= 2:
            if nums[idx] == nums[idx-1]:
                nums.pop(idx)
                if idx > 1:
                    idx = idx - 1
            elif idx < len(nums) - 1:
                idx = idx + 1
                continue
            else:
                break
        else:
            break
    return len(nums)
```


```python
def removeDuplicates(nums):
    last = 0
    for i in range(1, len(nums)):
        if nums[i] == nums[i - 1] or nums[i - 1] == '_' and nums[i] == nums[last]:
            nums[i] = '_'
        elif nums[i - 1] == '_':
            nums[last + 1] = nums[i]
            nums[i] = '_'
            last = last + 1
        else:
            last = last + 1
        
    for _ in range(nums.count('_')):
        nums.remove('_')
    return len(nums)
```


```python
def removeDuplicates(nums):
    for i in range(len(nums)):
        try:
            for _ in range(nums.count(nums[i]) - 1):
                nums.remove(nums[i])
        except:
            break
            
    return len(nums)
```


```python
def removeDuplicates(nums):
    last = 1
    for idx in range(len(nums) - 1):
        if nums[idx] != nums[idx+1]:
            nums[last] = nums[idx+1]
            last += 1
    return last
```

<a id='Remove Element'></a>
### Remove Element


```python
def removeElement(nums, val):
    for _ in range(nums.count(val)):
        nums.remove(val)
    return len(nums)
```

<a id='Search Insert Position'></a>
### Search Insert Position


```python
def searchInsert(nums, target):
    for idx in range(len(nums)):
        if target > nums[idx]:
            continue
        else:
            return idx
            
    return idx + 1
```

<a id='Length of Last Word'></a>
### Length of Last Word


```python
def lengthOfLastWord(s):
    return len(s.split()[-1])
```

<a id='Plus One'></a>
### Plus One


```python
def plusOne(digits):
    num = int(''.join([str(digit) for digit in digits])) + 1
    digits = []
    for digit in str(num):
        digits.append(int(digit))
    return digits
```


```python
def plusOne(digits):
    num = int(''.join([str(digit) for digit in digits])) + 1
    return [int(digit) for digit in str(num)]
```

<a id='Add Binary'></a>
### Add Binary


```python
def addBinary(a, b):
        idx_a = 0
        idx_b = 0
        final_res = ''
        remind = 0
        a = a[::-1]
        b = b[::-1]

        def get_res(num_a=0, num_b=0, remind=0):
            val = int(num_a) + int(num_b) + remind
            if val > 1:
                remind = 1
            else:
                remind = 0
            return str(val % 2), remind

        while idx_a < len(a) or idx_b < len(b):
            res = ''
            if idx_a < len(a) and idx_b < len(b):
                res, remind = get_res(a[idx_a], b[idx_b], remind)
                final_res = res + final_res
                idx_a += 1
                idx_b += 1
            elif idx_a < len(a) and idx_b >= len(b):
                res, remind = get_res(num_a=a[idx_a], remind=remind)
                final_res = res + final_res
                idx_a += 1
            else:
                res, remind = get_res(num_b = b[idx_b], remind=remind)
                final_res = res + final_res
                idx_b += 1

        if remind == 1:
            final_res = '1' + final_res
        return final_res
```


```python
def addBinary(a, b):
    idx_a = len(a) - 1
    idx_b = len(b) - 1
    final_res = ''
    carry = 0

    while idx_a >= 0 or idx_b >= 0:
            sum = carry
            if idx_a >= 0:
                sum += int(a[idx_a])
            if idx_b >= 0:
                sum += int(b[idx_b])

            idx_a, idx_b = idx_a - 1, idx_b - 1

            carry = 1 if sum > 1 else 0
            final_res += str(sum % 2)

    if carry != 0:
        final_res += str(carry)
    return final_res[::-1]
```

<a id='Sqrt(x)'></a>
### Sqrt(x)


```python
# using Newton Raphson Method

def mySqrt(x):
    x_0 = 1
    while True:
        x_1 = x_0 - ((x_0**2 - x)/(2 * x_0))
        if abs(x_1 - x_0) < 1e-5:
            break
        x_0 = x_1
    return int(x_1)
```

<a id='Climbing Stairs'></a>
### Climbing Stairs


```python
def climbStairs(n):
    if n == 1:
        return 1
    if n == 2:
        return 2
    if n == 3:
        return 3
    
    res = [2, 3, 0]
        
    for _ in range(n-3):
        res[2] = res[0] + res[1]
        res[0] = res[1]
        res[1] = res[2]
    return res[2]
```

<a id='Remove Duplicates from Sorted List'></a>
### Remove Duplicates from Sorted List


```python
def deleteDuplicates(self, head: ListNode) -> ListNode:
    """head: head of sorted linked list
    return linked list with no duplicates"""
    if head == None:
        return head
    
    newNode = ListNode(head.val)
    newlist = newNode
    last = newNode
    current = head.next
    while current != None:
        if current.val != last.val:
            newNode = ListNode(current.val)
            last.next = newNode
            last = newNode
        current = current.next
    return newlist
```

<a id='Merge Sorted Array'></a>
### Merge Sorted Array


```python
def merge(nums1, m, nums2, n):
    for idx, val in enumerate(nums2):
        nums1[m+idx] = val
    nums1.sort()
```

<a id='q_28'></a>
### 28. Find the Index of the First Occurrence in a String


```python
def strStr(haystack, needle):
    """
    :type haystack: str
    :type needle: str
    :rtype: int
    """
    return haystack.find(needle)
```


```python
# test
haystack = "sadbutsad" 
needle = "sad"
assert strStr(haystack, needle) == 0
```


```python
haystack = "leetcode" 
needle = "leeto"
assert strStr(haystack, needle) == -1
```

<a id='bt_inorder_traversal'></a>
### Binary Tree Inorder Traversal


```python
# Definition for a binary tree node.
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
     self.val = val
     self.left = left
     self.right = right
```


```python
# inorderTraversal (left - root - right)
def inorderTraversal(root):
    result = []
    if not root:
        return []
    result += inorderTraversal(root.left)
    result.append(root.val)
    result += inorderTraversal(root.right)
    return result
```


```python
root = TreeNode(val=1, right = TreeNode(val=2, left=TreeNode(val=3)))
inorderTraversal(root)
```




    [1, 3, 2]




```python
inorderTraversal(None)
```




    []




```python
root = TreeNode(val=1)
inorderTraversal(root)
```




    [1]



<a id='Same_Tree'></a>
### Same Tree


```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```


```python
def isSameTree(p, q) -> bool:
    if not p and not q:
        return True
    if not p or not q:
        return False

    # check the root 
    if p.val == q.val:
        # check the left and the right subtrees if the roots are equal
        return isSameTree(p.left, q.left) and isSameTree(p.right, q.right)
    return False
```


```python
n1 = TreeNode(val=1, right = TreeNode(val=3), left=TreeNode(val=2))
n2 = TreeNode(val=6, right = TreeNode(val=3), left=TreeNode(val=2))

isSameTree(n1, n2)
```




    False



<a id='Symmetric_Tree'></a>
### Symmetric Tree


```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```


```python
def isMirror(left, right):
    if not left and not right:
        return True
    if not left or not right:
        return False
    return left.val == right.val and isMirror(left.left, right.right) and isMirror(left.right, right.left)
    
def isSymmetric(root) -> bool:
    if not root:
        return True
    return isMirror(root.left, root.right)
```


```python
root = TreeNode(val=1, left=TreeNode(val=2, right=TreeNode(val=4)), 
                       right=TreeNode(val=2, right=TreeNode(val=3)))
```


```python
isSymmetric(root)
```




    False



<a id='Maximum_Depth_of_Binary_Tree'></a>
### Maximum Depth of Binary Tree


```python
def maxDepth(root) -> int:
    if not root:
        return 0
    return max(maxDepth(root.left), maxDepth(root.right)) + 1
```


```python
max(1, 2)
```




    2



<a id='Convert__Array_to_Binary_Search_Tree'></a>
### Convert Sorted Array to Binary Search Tree


```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```


```python
def sortedArrayToBST(nums):
    if not nums:
        return None
    mid = len(nums) // 2
    root = TreeNode(val=nums[mid])
    root.left = sortedArrayToBST(nums[:mid])
    root.right = sortedArrayToBST(nums[mid + 1:])
    return root
```

<a id='Balanced_Binary_Tree'></a>
### Balanced_Binary_Tree


```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```


```python
def maxDepth(root):
    if not root:
        return 0
    return max(maxDepth(root.left), maxDepth(root.right)) + 1
```


```python
def isBalanced(root) -> bool:
    if not root:
        return True
    left_max_depth = maxDepth(root.left)
    right_max_depth = maxDepth(root.right)
    
    # Check if the current node is balanced and if both subtrees are balanced
    return abs(left_max_depth - right_max_depth) <= 1 and \
           isBalanced(root.left) and \
           isBalanced(root.right)
```


```python
root = TreeNode(val=3, left=TreeNode(val=9), right=TreeNode(val=20, left=TreeNode(val=15), right=TreeNode(val=7)))
isBalanced(root)
```




    True




```python
root = TreeNode(val=1, left=TreeNode(val=2, left=TreeNode(val=3, left=TreeNode(val=4), 
                                                                 right=TreeNode(val=4)),
                                            right=TreeNode(val=3)), 
                       right=TreeNode(val=2))
isBalanced(root)
```




    False



<a id='Minimum_Depth_of_Binary_Tree'></a>
### Minimum_Depth_of_Binary_Tree


```python
def minDepth(root) -> int:
    if not root:
        return 0
        
    if root.left and not root.right:
        return minDepth(root.left) + 1
    elif root.right and not root.left:
        return minDepth(root.right) + 1
    else:
        return min(minDepth(root.left) + 1, minDepth(root.right) + 1)
```


```python
class TreeNode:
    def __init__(self, val=0, left=None, right=None):
        self.val = val
        self.left = left
        self.right = right
```


```python
def build_tree(level_order):
    if not level_order:
        return None
    
    # Create the root node
    root = TreeNode(level_order[0])
    queue = [root]
    i = 1
    
    # Use a queue to construct the tree level by level
    while queue and i < len(level_order):
        current_node = queue.pop(0)
        
        # Left child
        if i < len(level_order) and level_order[i] is not None:
            current_node.left = TreeNode(level_order[i])
            queue.append(current_node.left)
        i += 1
        
        # Right child
        if i < len(level_order) and level_order[i] is not None:
            current_node.right = TreeNode(level_order[i])
            queue.append(current_node.right)
        i += 1
    
    return root
```


```python
root = build_tree([3,9,20,None,None,15,7])

minDepth(root)
```




    2




```python
root = build_tree([2,None,3,None,4,None,5,None,6])
minDepth(root)
```




    5



<a id='Path_Sum'></a>
### Path_Sum


```python
root = build_tree([5,4,8,11,None,13,4,7,2,None,None,None,1])
#root = build_tree([1,2,3])
```


```python
def hasPathSum(root, targetSum: int) -> bool:
    if not root:
        return False
    if not root.left and not root.right:
        return targetSum == root.val

    return hasPathSum(root.left, targetSum - root.val) or hasPathSum(root.right, targetSum - root.val)
```


```python
hasPathSum(root, 22)
```




    True



<a id="Pascal's_Triangle"></a>
### Pascal's_Triangle


```python
def generate(numRows: int) -> list[list[int]]:
    triangle = []
    for i in range(numRows):
        triangle.append([1])
        for j in range(1, i + 1):
            if i == j:
                triangle[i].append(1)
            else:
                triangle[i].append(triangle[i-1][j] + triangle[i-1][j-1])
    return triangle
```


```python
generate(5)
```




    [[1], [1, 1], [1, 2, 1], [1, 3, 3, 1], [1, 4, 6, 4, 1]]



<a id="Pascal's_Triangle_II"></a>
### Pascal's_Triangle_II


```python
def getRow(rowIndex: int) -> list[int]:
    triangle = []
    for i in range(rowIndex + 1):
        triangle.append([1])
        for j in range(1, i + 1):
            if i == j:
                triangle[i].append(1)
            else:
                triangle[i].append(triangle[i-1][j] + triangle[i-1][j-1])
    return triangle[rowIndex]
```


```python
getRow(1)
```




    [1, 1]



<a id='Valid_Palindrome'></a>
### Valid_Palindrome


```python
def isPalindrome(s: str) -> bool:
    pattern = re.compile(r'[A-Za-z0-9]')
    res = re.findall(pattern, s.lower())
    res = ''.join(res)
    if res == res[::-1]:
        return True
    return False
```


```python
s = "A man, a plan, a canal: Panama"
#s = "race a car"
#s = " "
isPalindrome(s)
```




    True




```python
import re
def isPalindrome(s: str) -> bool:
    pattern = re.compile(r'[A-Za-z0-9]')
    res = re.findall(pattern, s.lower())
    res = ''.join(res)
    
    if res == "":
        return True
        
    size = len(res)
    start = 0
    end = size - 1
    while start < end:
        if res[start] == res[end]:
            start += 1
            end -= 1
        else:
            return False
            
    return True
```


```python
s = "A man, a plan, a canal: Panama"
#s = "race a car"
#s = " "
isPalindrome(s)
```




    True



<a id='Single_Number'></a>
### Single_Number


```python
def singleNumber(nums: list[int]) -> int:
    uniqueNum = 0
    
    for n in nums:
        uniqueNum ^= n
        
    return uniqueNum
```


```python
#nums = [2,2,1]
nums = [4,1,2,1,2]
singleNumber(nums)
```




    4



<a id='Linked_List_Cycle'></a>
### Linked_List_Cycle


```python
# Definition for singly-linked list.
class ListNode:
    def __init__(self, x):
        self.val = x
        self.next = None

```


```python
def hasCycle(head: ListNode) -> bool:
    nodes = []
    while head:
        if head in nodes:
            return False
        nodes.append(head)
        head = head.next
    return True
```


```python
def hasCycle(head: ListNode) -> bool:
    fast = head
    slow = head
    while fast and fast.next:
        fast = fast.next.next
        slow = slow.next
        if fast == slow:
            return True
    return False
```


```python
head = ListNode(3)
head.next = ListNode(2)
head.next.next = ListNode(0)
head.next.next.next = ListNode(-4)
head.next.next.next.next = head.next
hasCycle(head)
```




    True



<a id='Binary_Tree_Preorder_Traversal'></a>
### Binary_Tree_Preorder_Traversal


```python
def preorderTraversal(root) -> list[int]:
    if not root:
        return []
    lst = []
    lst.append(root.val)
    lst += preorderTraversal(root.left)
    lst += preorderTraversal(root.right)
    return lst
```


```python
root = build_tree([1,2,3,4,5,None,8,None,None,6,7,9])
preorderTraversal(root)
```




    [1, 2, 4, 5, 6, 7, 3, 8, 9]



<a id='Binary_Tree_Postorder_Traversal'></a>
### Binary_Tree_Postorder_Traversal


```python
def postorderTraversal(root: TreeNode) -> list[int]:
    if not root:
        return []

    lst = []
    lst += postorderTraversal(root.left)
    lst += postorderTraversal(root.right)
    lst.append(root.val)
    return lst
```


```python
root = build_tree([1,2,3,4,5,None,8,None,None,6,7,9])
postorderTraversal(root)
```




    [4, 6, 7, 5, 2, 9, 8, 3, 1]



<a id='Intersection_of_Two_Linked_Lists'></a>
### Intersection_of_Two_Linked_Lists


```python
def getIntersectionNode(headA: ListNode, headB: ListNode) -> ListNode:
    lst = []
    while headA:
        lst.append(headA)
        headA = headA.next
   
    while headB:
        if headB in lst:
            return headB
        headB = headB.next
    return None
```


```python
def getIntersectionNode(headA: ListNode, headB: ListNode) -> ListNode:
    if headA is None or headB is None:
        return None
    pA, pB = headA, headB
    while pA != pB:
        pA = headB if pA is None else pA.next
        pB = headA if pB is None else pB.next
    return pB
```


```python
head1 = ListNode(1)
head2 = ListNode(1)

head2.next = head1

intersect = getIntersectionNode(head1, head2)
intersect
```




    <__main__.ListNode at 0x29e6d2811f0>



<a id='Excel_Sheet_Column_Title'></a>
### Excel_Sheet_Column_Title


```python
def convertToTitle(columnNumber) -> str:
    excel_column = ""
    while columnNumber > 0:
        # 65 is ASCII number for 'A'
        excel_column = chr(65 + ((columnNumber - 1) % 26)) + excel_column
        columnNumber = (columnNumber - 1 ) // 26
    return excel_column
```


```python
convertToTitle(1000)
```




    'ALL'



<a id='Majority_Element'></a>
### Majority_Element


```python
def majorityElement(nums: list[int]) -> int:
    num_vote = 0
    candidate = 0
    for num in nums:
        if num_vote == 0:
            candidate = num
            
        if candidate == num:
            num_vote += 1
        else:
            num_vote -= 1
            
    return candidate
```

<a id='Excel_Sheet_Column_Number'></a>
### Excel_Sheet_Column_Number


```python
def titleToNumber(columnTitle: str) -> int:
    columnNum = 0
    for c in columnTitle:
        cNum = (ord(c) - 65) + 1
        columnNum = (columnNum * 26) + cNum
    
    return columnNum
```


```python
titleToNumber('ZY')
```




    701



<a id='Combine_Two_Tables'></a>
### Combine_Two_Tables


```python
import pandas as pd

# Person Table
data_person = {
    'personId': [1, 2],
    'lastName': ['Wang', 'Alice'],
    'firstName': ['Allen', 'Bob']
}
person_df = pd.DataFrame(data_person)

# Address Table
data_address = {
    'addressId': [1, 2],
    'personId': [2, 3],
    'city': ['New York City', 'Leetcode'],
    'state': ['New York', 'California']
}
address_df = pd.DataFrame(data_address)

# Display the DataFrames
print("Person Table:")
print(person_df)

print("\nAddress Table:")
print(address_df)
```

    Person Table:
       personId lastName firstName
    0         1     Wang     Allen
    1         2    Alice       Bob
    
    Address Table:
       addressId  personId           city       state
    0          1         2  New York City    New York
    1          2         3       Leetcode  California
    


```python
def combine_two_tables(person: pd.DataFrame, address: pd.DataFrame) -> pd.DataFrame:
    df = person.merge(right=address, on='personId', how='left')
    df.drop(['personId', 'addressId'], axis=1, inplace=True)
    return df
```


```python
combine_two_tables(person=person_df, address=address_df)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>lastName</th>
      <th>firstName</th>
      <th>city</th>
      <th>state</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Wang</td>
      <td>Allen</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Alice</td>
      <td>Bob</td>
      <td>New York City</td>
      <td>New York</td>
    </tr>
  </tbody>
</table>
</div>



<a id='Employees_Earning_More_Than_Their_Managers'></a>
### Employees_Earning_More_Than_Their_Managers


```python
import pandas as pd
import numpy as np  # For handling null values

# Employee Table
data_employee = {
    'id': [1, 2, 3, 4],
    'name': ['Joe', 'Henry', 'Sam', 'Max'],
    'salary': [70000, 80000, 60000, 90000],
    'managerId': [3, 4, np.nan, np.nan]  # Use np.nan for null values
}
employee_df = pd.DataFrame(data_employee)

# Display the DataFrame
print("Employee Table:")
print(employee_df)
```

    Employee Table:
       id   name  salary  managerId
    0   1    Joe   70000        3.0
    1   2  Henry   80000        4.0
    2   3    Sam   60000        NaN
    3   4    Max   90000        NaN
    


```python
def find_employees(employee: pd.DataFrame) -> pd.DataFrame:
    df = employee.merge(right=employee, left_on='id', right_on='managerId', how='inner')
    earn_more = df[df['salary_y'] > df['salary_x']][['name_y']]
    earn_more.rename(columns={'name_y': 'Employee'}, inplace=True)
    return earn_more
```


```python
find_employees(employee_df)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Employee</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Joe</td>
    </tr>
  </tbody>
</table>
</div>



<a id='Duplicate_Emails'></a>
### Duplicate_Emails


```python
import pandas as pd

# Create the DataFrame
data = {
    'id': [1, 2, 3],
    'email': ['a@b.com', 'a@b.com', 'a@b.com']
}

df = pd.DataFrame(data)
print(df)
```

       id    email
    0   1  a@b.com
    1   2  a@b.com
    2   3  a@b.com
    


```python
df.duplicated(subset='email', keep=False)
```




    0    True
    1    True
    2    True
    dtype: bool




```python
def duplicate_emails(person: pd.DataFrame) -> pd.DataFrame:
    return person[person.duplicated(subset='email')][['email']].drop_duplicates()
```


```python
duplicate_emails(df)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>email</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>a@b.com</td>
    </tr>
  </tbody>
</table>
</div>



<a id='Customers_Who_Never_Order'></a>
### Customers_Who_Never_Order


```python
import pandas as pd

# Customers table
customers_data = {
    'id': [1, 2, 3, 4],
    'name': ['Joe', 'Henry', 'Sam', 'Max']
}
customers_df = pd.DataFrame(customers_data)

# Orders table
orders_data = {
    'id': [1, 2],
    'customerId': [3, 1]
}
orders_df = pd.DataFrame(orders_data)

print("Customers Table:")
print(customers_df)
print("\nOrders Table:")
print(orders_df)
```

    Customers Table:
       id   name
    0   1    Joe
    1   2  Henry
    2   3    Sam
    3   4    Max
    
    Orders Table:
       id  customerId
    0   1           3
    1   2           1
    


```python
customers_df.merge(right=orders_df, left_on='id', right_on='customerId', how='outer', indicator=True).query("_merge == 'left_only'")[['name']]
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Henry</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Max</td>
    </tr>
  </tbody>
</table>
</div>




```python
def find_customers(customers: pd.DataFrame, orders: pd.DataFrame) -> pd.DataFrame:
    df = customers.merge(right=orders, left_on='id', right_on='customerId', how='outer', indicator=True)
    return df.query("_merge == 'left_only'")[['name']].rename(columns={'name':'customers'})
```


```python
find_customers(customers_df, orders_df)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>customers</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Henry</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Max</td>
    </tr>
  </tbody>
</table>
</div>



<a id='Reverse_Bits'></a>
### Reverse_Bits


```python
def reverseBits(n: int) -> int:
    bin_ = format(n, 'b')
    bin_ = '0' * (32 - len(bin_)) + bin_
    return int(bin_[::-1], base=2)
```


```python
reverseBits(43261596)
```




    964176192




```python
def reverseBits(n: int) -> int:
    res = 0
    for _ in range(32):
        bit = (n & 1)
        res = (res << 1) | bit
        n = n >> 1
    return res
```


```python
reverseBits(43261596)
```




    964176192



<a id='Number_of_1_Bits'></a>
### Number_of_1_Bits


```python
def hammingWeight(n: int) -> int:
    return format(n, 'b').count('1')
```


```python
hammingWeight(11)
```




    3




```python
def hammingWeight(n: int) -> int:
    count = 0
    while n > 0:
        count += (n & 1)
        n = n >> 1
    return count
```


```python
hammingWeight(2147483645)
```




    30



<a id='Missing_Number'></a>
### Missing_Number


```python
def missingNumber(nums: list[int]) -> int:
    return (set(range(len(nums) + 1)) - set(nums)).pop()
```


```python
missingNumber([9,6,4,2,3,5,7,0,1])
```




    8




```python
def missingNumber(nums: list[int]) -> int:
    # No need to sort if input is guaranteed to be numbers 0 to n with one missing
    nums.sort()
    start, end = 0, len(nums) - 1

    while start <= end:
        mid = (start + end) // 2
        # Check if nums[mid] matches its index
        if nums[mid] == mid:
            # Missing number is in the right half
            start = mid + 1
        else:
            # Missing number is in the left half
            end = mid - 1

    # The missing number is the point where the index starts to deviate
    return start

```


```python
missingNumber([9,6,4,2,3,5,7,0,1])
```




    8



<a id='Intersection_of_Two_Arrays_II'></a>
### Intersection_of_Two_Arrays_II


```python
def intersect(nums1: list[int], nums2: list[int]) -> list[int]:
    res = []
    nums2.sort()
    
    for n in nums1:
        start = 0
        end = len(nums2) - 1
        while start <= end:
            mid = (start + end) // 2
            if nums2[mid] > n:
                end = mid - 1
            elif nums2[mid] < n:
                start = mid + 1
            else:
                res.append(n)
                nums2.pop(mid)
                break
                
    return res

```


```python
nums1 = [4,9,5]
nums2 = [9,4,9,8,4]
nums1 = [1,2,2,1]
nums2 = [2]
intersect(nums1, nums2)
```




    [2]



<a id='Count_Complete_Tree_Nodes'></a>
### Count_Complete_Tree_Nodes


```python
def countNodes(root: TreeNode):
    if not root:
        return 0

    return countNodes(root.left) + countNodes(root.right) + 1
```


```python
root = build_tree([1,2,3,4,5,6])
countNodes(root)
```




    6



<a id='Happy_Number'></a>
### Happy_Number


```python
def isHappy(n: int) -> bool:
    visited = set()
    while n not in visited:
        if n == 1:
            return True

        visited.add(n)
        output = 0
        while n:
            digit = n % 10
            output += digit**2
            n = n // 10
        n = output
    return False
```


```python
isHappy(15)
```




    False




```python
def isHappy(n: int) -> bool:    
    
    def get_next_number(n):    
        output = 0
        
        while n:
            digit = n % 10
            output += digit ** 2
            n = n // 10
        
        return output

    slow = get_next_number(n)
    fast = get_next_number(get_next_number(n))

    while slow != fast:
        if fast == 1: return True
        slow = get_next_number(slow)
        fast = get_next_number(get_next_number(fast))

    return slow == 1
```

<a id='Reverse_Linked_List'></a>
### Reverse_Linked_List


```python
# Definition for singly-linked list.
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

def reverseList(head: ListNode) -> ListNode:
    if not head:
        return head
    nextNode = head.next
    head.next = None
    preNode = head
    while nextNode:
        head = nextNode
        nextNode = nextNode.next
        head.next = preNode
        preNode = head
      
    return head
```


```python
head = build_linked_list_from_list([1,2,3,4,5])

display_linked_list(reverseList(head))
```

    5 -> 4 -> 3 -> 2 -> 1
    


```python
def reverseList(head: ListNode) -> ListNode:
    if not head or not head.next:
        return head

    new_head = reverseList(head.next)
    head.next.next = head
    head.next = None
    
    return new_head
```


```python
head = build_linked_list_from_list([1,2,3,4,5])

display_linked_list(reverseList(head))
```

    5 -> 4 -> 3 -> 2 -> 1
    

<a id='Contains_Duplicate'></a>
### Contains_Duplicate


```python
def containsDuplicate(nums: list[int]) -> bool:
    return len(set(nums)) < len(nums)
```


```python
containsDuplicate([1, 2])
```




    False




```python
def containsDuplicate(nums: list[int]) -> bool:
    nums.sort()
    for i in range(1, len(nums)):
        if nums[i] == nums[i-1]:
            return True
    return False
```


```python
containsDuplicate([1, 2, 1])
```




    True



<a id='Palindrome_Linked_List'></a>
### Palindrome_Linked_List


```python
def isPalindrome(head: ListNode) -> bool:
    stack = []
    current = head
    while current:
        stack.append(current.val)
        current = current.next
    while head:
        if head.val != stack.pop():
            return False
        head = head.next
    return True
```


```python
head = build_linked_list_from_list([1,2, 1, 2])
isPalindrome(head)
```




    False




```python
def isPalindrome(head: ListNode) -> bool:
    list_vals = []
    while head:
        list_vals.append(head.val)
        head = head.next
    left, right = 0, len(list_vals) - 1
    while left < right and list_vals[left] == list_vals[right]:
        left += 1
        right -= 1
        
    return left >= right
```


```python
head = build_linked_list_from_list([1, 2])
isPalindrome(head)

```




    False



<a id='Valid_Anagram'></a>
### Valid_Anagram


```python
def count_let(s: str):
    count = {}
    for let in s:
        count[let] = count.get(let, 0) + 1
    return count
    
def isAnagram(s: str, t: str) -> bool:
    s_count = count_let(s)
    t_count = count_let(t)

    for let in t_count: 
        if (s_count != t_count) or (s_count[let] != t_count[let]):
            return False
    return True
```


```python
s = "ab"
t = "a"
isAnagram(s, t)
```




    False




```python
s_count == t_count
```

<a id='Move_Zeroes'></a>
### Move_Zeroes


```python
def moveZeroes(nums: list[int]) -> None:
    """
    Do not return anything, modify nums in-place instead.
    """
    slow = 0
    for fast in range(len(nums)):
        if nums[fast] != 0:
            nums[slow], nums[fast] = nums[fast], nums[slow]
            slow += 1                 
```


```python
nums = [0,1,0,3,12]
moveZeroes(nums)
nums
```




    [1, 3, 12, 0, 0]



<a id='Power_of_Three'></a>
### Power_of_Three


```python
def isPowerOfThree(n: int) -> bool:
    if n <= 0:
        return False

    pow_ = 0
    while 3**pow_ < n:
        pow_ +=1

    return n == 3**pow_
```


```python
def getPow(n, pow_):
    if 3**pow_ >= n:
        return 3**pow_
    return getPow(n, pow_ + 1)
    
def isPowerOfThree(n: int) -> bool:
    if n <= 0:
        return False
    return n == getPow(n, 0)
```


```python
isPowerOfThree(9)
```




    True



<a id='Reverse_String'></a>
### Reverse_String


```python
def reverseString(s: list[str]) -> None:
    """
    Do not return anything, modify s in-place instead.
    """
    start = 0
    end = len(s) - 1
    while start < end:
        s[start], s[end] = s[end], s[start]
        start += 1
        end -= 1
```


```python
#s = ["h","e","l","l","o"]
s = ["H","a","n","n","a","h"]
reverseString(s)
s
```




    ['h', 'a', 'n', 'n', 'a', 'H']




```python
def reverseString(s: list[str]) -> None:
    """
    Do not return anything, modify s in-place instead.
    """
    s[:] = s[::-1]
```


```python
|#s = ["h","e","l","l","o"]
s = ["H","a","n","n","a","h"]
reverseString(s)
s
```




    ['h', 'a', 'n', 'n', 'a', 'H']



<a id='First_Unique_Character_in_a_String'></a>
### First_Unique_Character_in_a_String


```python
def firstUniqChar(s: str) -> int:
    let_count = {}
    for let in s:
        let_count[let] = let_count.get(let, 0) + 1
    for i in range(len(s)):
        if let_count[s[i]] == 1:
            return i

    return -1
            
```


```python
firstUniqChar('loveleetcode')
```




    2



<a id='Fizz_Buzz'></a>
### Fizz_Buzz


```python
def fizzBuzz(n: int) -> list[str]:
    ans = []
    for num in range(1, n + 1):
        if num % 3 == 0 and num % 5 == 0:
            ans.append('FizzBuzz')
        elif num % 3 == 0:
            ans.append('Fizz')
        elif num % 5 == 0:
            ans.append('Buzz')
        else:
            ans.append(f'{num}')
    return ans
```


```python
fizzBuzz(15)
```




    ['1',
     '2',
     'Fizz',
     '4',
     'Buzz',
     'Fizz',
     '7',
     '8',
     'Fizz',
     'Buzz',
     '11',
     'Fizz',
     '13',
     '14',
     'FizzBuzz']



<a id='H-Index'></a>
### H-Index


```python
def hIndex(citations: list[int]) -> int:
    size = len(citations)
    citations.sort()
    for idx, n_cit in enumerate(citations):
        if n_cit >= (size - idx):
            return size - idx
    
    return 0
```


```python
citations = [0, 1, 3, 5, 6]
hIndex(citations)
```




    3



<a id='Insert_Delete_GetRandom_O(1)'></a>
### Insert_Delete_GetRandom_O(1)


```python
import random
class RandomizedSet:

    def __init__(self):
        self.lst = {}

    def insert(self, val: int) -> bool:
        if val in self.lst:
            return False
        else:
            self.lst[val] = val
            return True

    def remove(self, val: int) -> bool:
        if val not in self.lst:
            return False
        else:
            self.lst.pop(val)
            return True

    def getRandom(self) -> int:
        idx = random.randint(0, len(self.lst)-1)
        return list(self.lst.keys())[idx]
```


```python
randLst = RandomizedSet() 
randLst.insert(1)
randLst.remove(2)
randLst.insert(2)
randLst.getRandom()
```




    2



<a id='Product_of_Array_Except_Self'></a>
### Product_of_Array_Except_Self


```python
def productExceptSelf(nums: list[int]) -> list[int]:
    ans = [1] * len(nums)

    left = 1
    for i in range(len(nums)):
        ans[i] *= left
        left *= nums[i]

    right = 1

    for i in range(len(nums)-1, -1, -1):
        ans[i] *= right
        right *= nums[i]
    return ans
```


```python
productExceptSelf([1, 2, 3, 4])
```




    [24, 12, 8, 6]



<a id='Gas_Station'></a>
### Gas_Station


```python
def canCompleteCircuit(gas: list[int], cost: list[int]) -> int:
    if sum(gas) < sum(cost):
        return -1

    current_gas = 0
    start = 0
    for i in range(len(gas)):
        current_gas += gas[i] - cost[i]
        if current_gas < 0:
            current_gas = 0
            start = i + 1
            
    return start
```


```python
gas = [5,1,2,3,4]
cost = [4,4,1,5,1]

canCompleteCircuit(gas, cost)
```




    4



<a id='First_Bad_Version'></a>
### First_Bad_Version


```python
class Solution:
    def firstBadVersion(self, n: int) -> int:
        start = 1
        end = n
        while start < end:
            mid = (start + end) // 2
            if not isBadVersion(mid):
                start = mid + 1
            else:
                end = mid
                
        return start
```

<a id='Intersection_of_Two_Arrays'></a>
### Intersection_of_Two_Arrays


```python
def intersection(nums1: list[int], nums2: list[int]) -> list[int]:
    nums1.sort()
    nums2.sort()
    idx1, idx2, ans = 0, 0, set()
    while idx1 < len(nums1) and idx2 < len(nums2):
        if nums1[idx1] < nums2[idx2]:
            idx1 += 1
        elif nums1[idx1] > nums2[idx2]:
            idx2 += 1
        else:
            ans.add(nums1[idx1])
            idx1 += 1
            idx2 += 1
    return list(ans)
```


```python
nums1 = [1,2,2,1]
nums2 = [2,2]
intersection(nums1, nums2)
```




    [2]




```python
def intersection(nums1: list[int], nums2: list[int]) -> list[int]:
    return list(set(nums1) & set(nums2))
```


```python
def intersection(nums1: list[int], nums2: list[int]) -> list[int]:
    if len(nums1) < len(nums2):
        nums1, nums2 = nums2, nums1

    nums1.sort()
    nums2 = set(nums2)
    ans = []
    for num in nums2:
        start, end = 0, len(nums1) - 1
        while start <= end:
            mid = (start + end) // 2
            if nums1[mid] == num:
                ans.append(num)
                break
            elif nums1[mid] < num:
                start = mid + 1
            else:
                end = mid - 1
    return ans
```


```python
nums1 = [1,2,2,1]
nums2 = [2,2]
intersection(nums1, nums2)
```




    [2]



<a id='Remove_Linked_List_Elements'></a>
### Remove_Linked_List_Elements


```python
def removeElements(head: ListNode, val: int) -> ListNode:
    if head is None:
        return head

    head.next = removeElements(head.next, val)
    
    return head.next if head.val == val else head
```


```python
head = build_linked_list_from_list([1,2,6,3,4,5,6])
head = removeElements(head, 6)
display_linked_list(head)
```

    1 -> 2 -> 3 -> 4 -> 5
    

<a id='Power_of_Two'></a>
### Power_of_Two


```python
class Solution:
    def isPowerOfTwo(self, n: int) -> bool:
        if n <= 0:
            return False
        if n == 1:
            return True
        return (n % 2 == 0) and self.isPowerOfTwo(n // 2)
```

<a id='Concatenation_of_Array'></a>
### Concatenation_of_Array


```python
def getConcatenation(nums):
    ans = []
    for i in range(2):
        for n in nums:
            ans.append(n)
    return ans
```


```python
nums = [1,2,1]
getConcatenation(nums)
```




    [1, 2, 1, 1, 2, 1]




```python
def isAnagram(s: str, t: str) -> bool:
    return sorted(s) == sorted(t)
```


```python
s = 'nour'
t = 'roun'
isAnagram(s, t)
```




    True




```python
<a id='Refer_to'></a>
### Refer_to
```


```python
<a id='Refer_to'></a>
### Refer_to
```


```python
<a id='Refer_to'></a>
### Refer_to
```


```python
<a id='Refer_to'></a>
### Refer_to
```


```python
<a id='Refer_to'></a>
### Refer_to
```


```python
<a id='Refer_to'></a>
### Refer_to
```


```python
<a id='Refer_to'></a>
### Refer_to
```
