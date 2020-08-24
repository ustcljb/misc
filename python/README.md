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

## 4. Issues when using pickle.load()

The following error
```python
mydata = pickle.load(myfile, "rb")
ValueError: unsupported pickle protocol: 3
```
is because the file was created using Python 3(which has the default protocol 3), while loaded using Python 2(which has the protocol 2).

To solve this issue, the simplest and easiest approach will be to write a Python3 script that unpickles everything using protocol 3 and repickles it again using protocol 2. 
```python
pickle.dump(pickle.load(sys.stdin), sys.stdout, 2)
```
And then in Python 2:
```python
pickle.load(...) # This will work now in Python 2.
```

## 5. Difference between list.reverse() and list[::-1]
list.reverse() reverses the list in-place, while list[::-1] gives a new list in reverse order.

