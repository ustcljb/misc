## 1. How to make a flat list out of list of lists?

```python
l = [[1, 2, 3], [4, 5, 6], [7], [8, 9]]
flat_list = [item for sublist in l for item in sublist]
```

## 2. dict vs collections.defaultdict?

The difference is that a `defaultdict` will "default" a value if that key has not been set yet. If you didn't use a `defaultdict` you'd have to check to see if that key exists, and if it doesn't, set it to what you want.

## 3. How to remap values in pandas dataframe with a dict?

There are two methods: `.replace` and `.map` as follows:
```python
>>> df = pd.DataFrame({'col2': {0: 'a', 1: 2, 2: np.nan}, 'col1': {0: 'w', 1: 1, 2: 2}})
>>> di = {1: "A", 2: "B"}
>>> df
  col1 col2
0    w    a
1    1    2
2    2  NaN
>>> df.replace({"col1": di})
  col1 col2
0    w    a
1    A    2
2    B  NaN
```
or
```python
>>> df['col1'] = df['col1'].map(di)
>>> df
  col1 col2
0    w    a
1    A    2
2    B  NaN
```
However, if the dict contains large amount of keys, `.map` would be much faster.
