# SWE_2021_41_2024_2_week_6
### Week 4 Assignment
#### Week 4 repository link
>>https://github.com/twerkitboii/SWE_2021_41_2024_2_week_4
#### Week 4 Code
<pre>
<code>
```python
def isHappy(n):
    if n>2^31-1:
        return 0
    def get_next(number):
        total_sum = 0
        while number > 0:
            digit = number % 10
            total_sum += digit ** 2
            number //= 10
        return total_sum

    seen = set()

    while n != 1 and n not in seen:
        seen.add(n)
        n = get_next(n)

    return n == 1


n = int(input('Input: '))
if isHappy(n):
    print("True")
else:
    print("False")
```
</code>
    
</pre>


### Week 5 Assignment
