## 1. How to make a flat list out of list of lists?

```python
l = [[1, 2, 3], [4, 5, 6], [7], [8, 9]]
flat_list = [item for sublist in l for item in sublist]
```
