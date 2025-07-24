🔗 Problem link : https://www.geeksforgeeks.org/problems/who-has-the-majority/0

🧠 Explanation or code: 
🧠 Problem Summary:
Given an array of size N consisting of only 0s and 1s, find which element has the majority.
Majority means: it appears more than N/2 times.
If no such element, return "No Majority Element".

✅ Example:
Input: 
N = 5  
A = [0, 1, 1, 0, 1]

Output: 
1

Explanation: 
1 appears 3 times → 3 > 5/2 → So 1 is the majority.
Input:
N = 4  
A = [0, 1, 1, 0]

Output: 
No Majority Element

Explanation:
Both 0 and 1 appear 2 times → not more than 4/2 → no majority.
✅ Solution Approach:
Since the array only contains 0 and 1, we can just count the number of 0s and 1s, and check which one is greater than N/2.

🔽 Python Code:
def majorityElement(arr, n):
    count_0 = arr.count(0)
    count_1 = arr.count(1)
    
    if count_0 > n // 2:
        return 0
    elif count_1 > n // 2:
        return 1
    else:
        return "No Majority Element"
⏱ Time Complexity:
O(n) for counting 0s and 1s.
