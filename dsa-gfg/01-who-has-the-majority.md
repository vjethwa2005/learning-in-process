### 🔗 Problem Link: [Who has the majority?](https://www.geeksforgeeks.org/problems/who-has-the-majority/0)

#### 🧠 Problem Summary:
Given an array of size `N` consisting of only `0s and 1s`, find which element has the majority.  
**Majority** means: appears **more than N/2 times**.  
If no such element, return `"No Majority Element"`.

---

#### ✅ Examples:

**Input:**  
`N = 5`  
`A = [0, 1, 1, 0, 1]`  
**Output:** `1`  
**Explanation:** `1` appears 3 times → `3 > 5/2` → So 1 is the majority.

**Input:**  
`N = 4`  
`A = [0, 1, 1, 0]`  
**Output:** `No Majority Element`  
**Explanation:** Both appear twice → `2 = 4/2` → Not a majority.

---

#### 🛠️ Solution Approach:
- Count how many 0s and 1s are present.
- If either appears **more than N/2**, it’s the majority.

---

#### 🧾 Code (Python):

```python
def majorityElement(arr, n):
    count_0 = arr.count(0)
    count_1 = arr.count(1)
    
    if count_0 > n // 2:
        return 0
    elif count_1 > n // 2:
        return 1
    else:
        return "No Majority Element"
