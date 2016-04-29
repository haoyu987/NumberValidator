# NumberValidator
Pattern design and DFA

If there are too many cases to check.

https://leetcode.com/problems/valid-number/

Patter Design
https://leetcode.com/discuss/23447/a-clean-design-solution-by-using-design-pattern

DFA
https://leetcode.com/discuss/13691/c-my-thought-with-dfa
https://leetcode.com/discuss/70510/a-simple-solution-in-python-based-on-dfa

We start with trimming.

 If we see [0-9] we reset the number flag.
 We can only see . if we didn't see e or ..
 We can only see e if we didn't see e but we saw a number. We reset numberAfterE flag.
 We can only see + and - in the beginning or immediately after an e
 any other character break the validation.
 At the and it is only valid if there was at least 1 number and if we did see an e then a number after it as well.

The number should match this regular expression:

[-+]?[0-9]*(.[0-9]+)?(e[-+]?[0-9]+)?
