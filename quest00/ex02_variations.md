# Exercise 2: Strengthening Through Variations

Objective: Extend your solution and practice independent problem-solving.

Modify your palindrome function to:

Ignore spaces and punctuation.

Be case-insensitive.

Return the position where the string stops being a palindrome (if not one).

After your first attempt, ask AI:

"I modified my palindrome function to handle more cases.
Did I miss anything? Can it be more efficient?"
Reflect on what AI added that you didn't consider initially.

### My Answers
The more efficient code:
```python
def is_palindrome(s: str):
    cleaned = []
    positions = []

    # NOrmalize string and track original positions
    for idx, c in enumerate(s):
        if c.isalnum():
            cleaned.append(c.lower())
            positions.append(idx)

    left = 0
    right = len(cleaned) - 1

    while left < right:
        if cleaned[left] != cleaned[right]:
            # return the position in the ORIGINAL string
            return positions[left]
        
        left += 1
        right -= 1

    return True

if __name__ == "__main__":
    # This code runs only when the file is executed directly
    print(is_palindrome("racecar"))
    print(is_palindrome("hello"))
    print(is_palindrome("A man a plan a canal Panama"))
```

Reflecting back on the above code which is more effiecent, I didn't think about ignoring spaces and case sensitivity.

So, what AI added for me are:
- Ignoring all punctuations, not all spaces.
- Tracking original character positions
- Avoiding .isalnum() misuse
- Preserving meaningful error output