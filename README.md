# SWE_2021_41_2024_2_week_6
## Week 4
### Assignment: Complete Python code for judging if a number is 'happy' or not
__unordered list__ (*,+,-)
* Link to Repository
###Insert URL


+ Code Description
```python
def isHappy(n):
  if n == 1 or n == 7:                # both numbers which are happy numbers
    return True
  if n < 10:                          # other than 1 and 7, all numbers under 10 loop
    return False
  num = list(map(int, str(n)))        # map all digits in number to list
  while(1):
    sq = 0
    for i in num:
      sq = sq + i**2
    if sq == 1 or sq == 7:
      return True
    elif sq < 10:                     # note: this assumes all numbers at some point will have digits adding up to a number under 10, e.g., 11 -> 1 + 1 = 2
      return False                    # thus if at no point do those digits == 1 or 7, then they are not happy
    num = list(map(int, str(sq)))     # re-map (update) digits of number to list
```
