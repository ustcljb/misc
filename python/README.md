## 1. How to make a flat list out of list of lists?

```python
l = [[1, 2, 3], [4, 5, 6], [7], [8, 9]]
flat_list = [item for sublist in l for item in sublist]
```

## 2. What is the difference between dict and collections.defaultdict?

The difference is that a `defaultdict` will "default" a value if that key has not been set yet. If you didn't use a `defaultdict` you'd have to check to see if that key exists, and if it doesn't, set it to what you want.
