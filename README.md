README
Highest Value Palindrome

Given a string representing a number, change at most k digits to create the largest possible palindrome. If no palindrome can be formed within the allowed changes, return -1.

Approach
Traverse from both ends and fix mismatched pairs using the minimum number of changes.
If the required changes exceed k, return -1.
Use the remaining changes to maximize the palindrome:
Convert digit pairs to 9.
If a pair was already modified, upgrading it to 9 costs only one extra change.
For odd-length strings, use any leftover change to make the middle digit 9.
Algorithm
Make the string a palindrome with minimum changes.
Track which positions were modified.
Upgrade pairs to 9 whenever possible.
Handle the middle digit if the length is odd.
Return the resulting palindrome.
Complexity
Time: O(n)
Space: O(n)
Example

Input

6 3
092282

Output

992299

The string becomes a palindrome first, then the remaining changes are used to maximize its value by replacing digits with 9.
