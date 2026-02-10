# Exercise 1: The Palindrome Challenge

Objective: Experience the difference between using AI as a shortcut and using it as a learning tool.

## Step 1 - Do it yourself

- Write pseudocode for a function that checks if a string is a palindrome.

- Implement your solution in Python.

- Test with examples like "racecar", "hello", and "A man a plan a canal Panama".

- Add comments explaining your reasoning.


### My Pseudocode

```Ps
function is_palindrome(input_string):
    ## split out space within the string and join them back together
    stringToUse = string.split(" ").join("")

    # convert string back to lowercase
    stringToUse = lowercase(stringToUse)

    ## find length of stringToUse
    n = length of stringToUse

    ## get half of length n
    nHalf = n/2

    ## loop tloop from start of string to the middle
    For i from 0 to nHalf - 1

        # get index of character from opposite end
        oppositeIndex = n - 1 - i

        # compare characters
        If stringToUse[i] is not equal to stringToUse[oppositeIndex]
            return False
        end if

    end for loop

    ## if all characters matched
    return true

end function 
```

```python
def is_palindrome(s: str):
    sToUse = "".join(s.split(" ")).lower()

    # length of sToUse
    n = len(sToUse)
            
    # half of length n
    nHalf = int(n/2)

    for i in range(nHalf):
        nEnd = n-1-i

        # Compare string characters at index i and the opposite end
        if sToUse[i] != sToUse[nEnd]:
            return False
    
    return True
```

## Step 2 - Use AI to learn

Now that your function works, use AI to go deeper:

What's the time complexity? 


    The time complexity overall is O(n).  This is because, the time complexity it took for the these processes: s.split(" "), "".join(...), .lower(), for i in range(n/2) is O(n). THis means it didn't take much time for these operations to run.

What edge cases migth I miss?

    The different edge cases I migth miss are:
    1. PUnctuation not removed: EXample "A man, a plan, a canal: Panama" will return false because of the , and : that remains.

    2. Not considering non-alphanumeric symbols: In words like "race@car". the symbol @ will break the palindrome check.

    3. Not considering unicode/accented characters: A sentence like "A man à plan à canal Panama" will return false.

    4. Empty string/spaces only: This "     " will return True. I have learnbed that this is usualy acceptable but must be defined.

Are there better approaches?

    I could have implemented better normalization.
    e.g: sToUse = "".join(c.lower() for c in s if c.isalnum())

    The above line will handle punctuation and all whitespaces, and will still be on O(n).

## Step 3 - Reflection

What did you learn from solving it before asking AI?

    I learned about logical thinkng. I mean, how to think through the processes. I actually have seen that that is what the pseudocode helps me with. I mean, I have seen if you don't understand the logic, you can't implement the code.

How is your understanding different now?

    My understanding is different now in the sense that I understand the logic of writing a code that identifies a palindrome. IF I understand in simple terms how that works, the I can implement the code.
