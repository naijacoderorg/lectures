Session 2. Exploring the Data
====================

## Reflection for Last Day:

- Recap of Day 1: Asking Good Questions and basic DataFrame inspections.
- Brief introduction to the importance of DataFrame manipulation in analyzing data.


## Concepts

### 1. Selecting columns

To select a single column, we use the column name (in quotation marks) inside square brackets [] with the DataFrame.

```python
df['Country Dest Name']
```

To select multiple columns, we pass a list of column names inside square brackets with the DataFrame. Recall that a list is created using square brackets too, so we will end up with double square brackets.

```python
df[['Country Origin Name', 'Country Dest Name']]
```

### 2. Filtering Data

Let's say we want to filter the data to contain only rows that have information on migrations from Ghana. What kind of logic should we apply?

First of all, we need to find the column that contains information on origins, which in this case is `Country Origin Name`. We will use this column to create a filtering criterion: `Country Origin Name` should equal `Ghana`. Next, we use this criterion to apply a boolean condition on the dataset.

```python
df[df['Country Origin Name'] == 'Ghana']
```

#### Exercise 1

- Create two datasets named `migrations_from_Nigeria` and `migrations_to_Nigeria` containing only rows that satisfy the description in the names.

#### Example

We can also apply multiple conditions when filtering data. Let's create a dataset named `nonzero_emigrations_Nigeria_2020` containing only rows of migrations from Nigeria with values greater than 0 in the year 2020.

```python
nonzero_emigrations_NGA_2000 = df[
    (df["Country Origin Name"] == "Nigeria") &
    (df['y2000'] > 0)
]

# select only the origin, destination and y2000 columns
nonzero_emigrations_NGA_2000 = nonzero_emigrations_NGA_2000[['Country Origin Name', 'Country Dest Name', 'y2000']]

nonzero_emigrations_NGA_2000
```

### 3. Sorting Data

Using the `sort_values()` method, we can sort (arrange) the rows of a DataFrame based on the values of one or more column. This can be useful if you want to present your results in ascending or descending order.

Let's sort the `nonzero_emigrations_Nigeria_2020` DataFrame **by** the values in the `y2000` column in **descending** order.

```python
nonzero_emigrations_NGA_2000.sort_values(by='y2000', ascending=False)
```

#### Exercise 2
- What questions can the sorted dataset above answer?

We can also sort by more than one column, which is useful when we want to apply a secondary sorting criterion to break ties in the primary sort. For example, if we want to sort our original dataset `df` by the origin country first, but then sort by the destination country when the origin values are the same, we can achieve this using multi-column sorting.

```python
df.sort_values(by=['Country Origin Name', 'Country Dest Name'])
```

### 4. Grouping and Aggregating Data

**Grouping Data**

Grouping data involves creating subsets of the DataFrame based on the unique values in one or more columns. For instance, we might want to group our migration dataset by the origin country.

**Aggregation Functions**

Aggregation functions are used to compute summary statistics for each group. Common aggregation functions include:

- **Sum**: Adds up the values in each group.
- **Mean**: Calculates the average of the values in each group.
- **Count**: Counts the number of values in each group.
- **Max**: Finds the maximum value in each group.
- **Min**: Finds the minimum value in each group.

**Example**

Using `df`, let's group by the origin country and find the sum of migrations for each year.

In the code below, notice the sequential application of the `.groupby()` and `.sum()` methods. We first apply `.groupby()` and then apply the aggregation.

We don't need to specify the numeric columns because the `.sum()` aggregation is automatically applied to numeric columns. Try replacing `.sum()` with `.count()` and see the difference.

```python
# Group data by origin and sum the migrations
emigrations_total = df.groupby('Country Origin Name').sum()
emigrations_total.head()
```

**Exercise**

What if we only want to see aggregation for a subset of columns? We can apply the column selection syntax we learned earlier after the groupby method and before the aggregation.

Additionally, we can group by more than one column.

Let's find the sum of immigrations in 2000 for each migration route. _Migration route_ here refers to pairs of origin and destination countries. Nigeria to Ghana is a separate route from Ghana to Nigeria.

```python
# this will make more sense when continents are introduced
df.groupby(['Country Origin Name', 'Country Dest Name'])['y2000'].sum().reset_index()
```
