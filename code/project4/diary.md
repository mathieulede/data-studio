## Diary

### Extract values in Pandas value_counts()
https://stackoverflow.com/questions/35523635/extract-values-in-pandas-value-counts

```python
df_composers['composerName'].value_counts().nlargest(10).index.tolist()
```

### Draw the right label in a graph made on a groupby
```python
import matplotlib.pyplot as plt

fig, ax = plt.subplots(figsize=(16,4))

for label, df in popular_composers_plot.groupby('composerName'):
    df.plot(x='Date', y='count', ax=ax, label=label)
    
plt.show()
```

### Add missing dates to pandas dataframe
https://stackoverflow.com/questions/19324453/add-missing-dates-to-pandas-dataframe

```python
Series.reindex
```

```python
idx = pd.date_range('09-01-2013', '09-30-2013')

s = pd.Series({'09-02-2013': 2,
               '09-03-2013': 10,
               '09-06-2013': 5,
               '09-07-2013': 1})
s.index = pd.DatetimeIndex(s.index)

s = s.reindex(idx, fill_value=0)
```