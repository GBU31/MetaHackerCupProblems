
#### [Cheeseburger Corollary 1]( https://www.facebook.com/codingcompetitions/hacker-cup/2023/practice-round/problems/A1)

You're interested in building a K-decker cheeseburger, which alternates between buns, cheese, and patty starting and ending with a bun.

**You've already bought S single cheeseburgers and D double cheeseburgers**. Each provides you with two buns, though a **single provides one patty and one cheese**, **while a double provides two patties and two cheese.**

Code:
```python
def cheeseburger_corollary_1():
    s, d, k = map(int, input().split())

    total_buns = 2 * s + 2 * d
    total_cheese = s + 2 * d
    total_patties = s + 2 * d

    return "YES" if total_buns >= k + 1 and total_cheese >= k and total_patties else "NO"
    
```

Get the values of S (single cheeseburgers), D (double cheeseburgers), and K (k-decker cheeseburger):
```python
s, d, k = map(int, input().split())
```

Multiply the number of S and D by 2, sense we have two buns in each D and S:
```python
total_buns = 2 * s + 2 * d
```

D has 2 cheese and 2 patties while S has 1 cheese and 1 patty:
```python
total_cheese = s + 2 * d
total_patties = s + 2 * d
```

If we have enough buns (==**number of k + 1**==), cheese, and patties we return "YES",
"NO" if we don't: 
```python
return "YES" if total_buns >= k + 1 and total_cheese >= k and total_patties else "NO"
```


Run function:
```python
for case in range(int(input())):
    print('Case #%d: %s' % (case+1, cheeseburger_corollary_1()))
```

Run program: 
```
python3 sol.py cheeseburger_corollary_1_sample_input.txt
```
