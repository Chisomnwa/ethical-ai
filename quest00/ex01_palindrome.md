# Exercise 1: The Palindrome Challenge

Objective: Experience the difference between using AI as a shortcut and using it as a learning tool.

## Step 1 - Do it yourself

- Write pseudocode for a function that checks if a string is a palindrome.

- Implement your solution in Python.

- Test with examples like "racecar", "hello", and "A man a plan a canal Panama".

- Add comments explaining your reasoning.


### My Pseudocode

```text
function is_palindrome(input_string):
    cleaned_string = ""

    for each character in input_string:
        if character is alphanumeric:
        cleaned_string = cleaned_string + lowercase(character)

    left = 0
    right = length(cleaned_string) - 1

    while left < right:
        if cleaned_string[left] != cleaned_string[right]:
        return False

        left = left + 1
        right = right = 1

    return True
```

```Ps
function is_palindrome(input_string):
    ## split out space within the string
   
    stringToUse = string.split(" ").join("")

    ## find length of stringToUse
    n = (length of stringToUse)

    ## half of length n
    nHalf = n/2
    
    
    # initialize string index with i
    i = 0

    ## loop through nHalf times
    for i less than nHalf

        ## get and compare string characters at index i and the opposite end
        character = string at index i

        oppositeIndex = n - 1 - i

        characterAtOppositeEnd = string at index oppositeIndex 

        if character is not equal to characterAtOppositeEnd:
            return False

        ## increment string index by 1
        i++

    end of loop

    ## if loop completes without returning, then string is a palindrome
    return true

end function




```

```python
def is_palindrome(input_string):
    cleaned_string = ""

    for c in input_string:
        if c.isalnum():
            cleaned_string += c.lower()

    left = 0
    right = len(cleaned_string) - 1

    while left < right:
        if cleaned_string[left] != cleaned_string[right]:
            return False

        left += 1
        right -= 1

    return True
```

## Step 2 - Use AI to learn

Now that your function works, use AI to go deeper:
