Day 6: Growth of Functions
===========================

Morning
-------

### Reflection from Last Day:
* Answer questions about for objects, libraries in Python
* Discuss exercises from previous day

Understanding the growth of functions and asymptotic notation is crucial in analyzing the efficiency of algorithms and data structures. These concepts help in quantifying how the runtime or space requirements of algorithms change with input size. Let's delve into each of these concepts:

### Growth of Functions

In computer science, the growth of a function refers to how its runtime (or space) increases as the size of the input grows. This growth is typically measured in terms of the input size $n$.

#### Example of Growth Functions:

Consider two functions:
- $f(n) = 2n + 1$
- $g(n) = n^2 + 3n$

As $n$ increases:
- $f(n)$ grows linearly $O(n)$ because the dominant term is $n$.
- $g(n)$ grows quadratically $O(n^2)$ because the dominant term is $n^2$.

### Asymptotic Notation

Asymptotic notation provides a formal way to describe the limiting behavior (as $n$ becomes very large) of a function:

1. **Big O Notation (O)**:
   - **Definition**: Represents the upper bound of the function's growth rate. It describes the worst-case scenario.
   - **Example**: Intuition is that $O(n^2)$ means the function grows no faster than $n^2$.

2. **Omega Notation ($\Omega$)**:
   - **Definition**: Represents the lower bound of the function's growth rate. It describes the best-case scenario.
   - **Example**: Intuition is that $\Omega(n)$ means the function grows at least as fast as $n$.

3. **Theta Notation ($\Theta$)**:
   - **Definition**: Represents both the upper and lower bounds, providing a tight bound on the function's growth rate.
   - **Example**: Intuition is that $\Theta(n)$ means the function grows exactly like $n$.

In mathematical terms, Big O notation $O(f(n))$ is used to denote an upper bound on the asymptotic growth rate of a function $f(n)$ as $n$ becomes large. Here's the mathematical definition of Big O notation:

### Definition

Given two functions $f(n)$ and $g(n)$:

$$f(n) = O(g(n))$$

This statement means that there exist constants $c > 0$ and $n_0 \geq 0$ such that for all $n \geq n_0$, the function $f(n)$ is bounded above by $c \cdot g(n)$:

$$|f(n)| \leq c \cdot |g(n)| \quad \text{for all } n \geq n_0$$

### Key Points

- **Upper Bound**: Big O notation provides an upper bound on the growth rate of $f(n)$.
- **Constant Factors**: It ignores constant factors and lower-order terms, focusing on the dominant term that contributes most significantly to the growth rate as $n$ increases.
- **Asymptotic Behavior**: Big O notation describes the long-term behavior of functions as $n$ approaches infinity.

### Example Interpretation

If $f(n) = 2n + 1$, we say $f(n) = O(n)$ because for sufficiently large $n$, $2n + 1$ is bounded above by $cn$ for some constant $c$. Specifically, for $c = 3$ and $n_0 = 1$, $2n + 1 \leq 3n$ holds for all $n \geq 1$.

### Practical Use

In algorithm analysis, Big O notation is widely used to characterize the time complexity (and sometimes space complexity) of algorithms. It helps in comparing the efficiency of algorithms and predicting how they will perform with larger inputs.

In mathematical terms, Big Omega notation $\Omega(f(n))$ is used to denote a lower bound on the asymptotic growth rate of a function $f(n)$ as $n$ becomes large. Here's the mathematical definition of Big Omega notation:

### Definition

Given two functions $f(n)$ and $g(n)$:

$$f(n) = \Omega(g(n))$$

This statement means that there exist constants $c > 0$ and $n_0 \geq 0$ such that for all $n \geq n_0$, the function $f(n)$ is bounded below by $c \cdot g(n)$:

$$|f(n)| \geq c \cdot |g(n)| \quad \text{for all } n \geq n_0$$

### Key Points

- **Lower Bound**: Big Omega notation provides a lower bound on the growth rate of $f(n)$.
- **Constant Factors**: Similar to Big O notation, it ignores constant factors and lower-order terms, focusing on the dominant term that contributes most significantly to the growth rate as $n$ increases.
- **Asymptotic Behavior**: Big Omega notation describes the long-term behavior of functions as $n$approaches infinity.

### Example Interpretation

If $f(n) = n^2 + 3n$, we say $f(n) = \Omega(n^2)$ because for sufficiently large $n$, $n^2 + 3n$ is bounded below by $cn^2$ for some constant $c$. Specifically, for $c = 1$ and $n_0 = 1$, $n^2 + 3n \geq n^2$ holds for all $n \geq 1$.

### Practical Use

Big Omega notation is used similarly to Big O notation in algorithm analysis. It helps in characterizing the lower bounds of algorithms' time complexity (and sometimes space complexity), providing insight into their performance guarantees for large inputs.

### Comparison with Big O Notation

- **Big O vs. Big Omega**: While Big O provides an upper bound on the growth rate of a function $f(n)$, Big Omega provides a lower bound. Together, they can give a more complete picture of an algorithm's complexity by indicating both its worst-case and best-case scenarios.

In mathematical terms, Big Theta notation $\Theta(f(n))$ is used to denote a tight bound on the asymptotic growth rate of a function $f(n)$ as $n$ becomes large. Here's the mathematical definition of Big Theta notation:

### Definition

Given two functions $f(n)$ and $g(n)$:

$$f(n) = \Theta(g(n))$$

This statement means that there exist constants $c_1 > 0$, $c_2 > 0$, and $n_0 \geq 0$ such that for all $n \geq n_0$, the function $f(n)$ is bounded both above and below by $c_1 \cdot g(n)$ and $c_2 \cdot g(n)$, respectively:

$$c_1 \cdot |g(n)| \leq |f(n)| \leq c_2 \cdot |g(n)| \quad \text{for all } n \geq n_0$$

### Key Points

- **Tight Bound**: Big Theta notation provides a tight or asymptotically tight bound on the growth rate of $f(n)$. It means $f(n)$ grows at the same rate as $g(n)$ within constant factors, asymptotically speaking.
  
- **Constant Factors**: Similar to Big O and Big Omega notations, Big Theta ignores constant factors and lower-order terms, focusing on the dominant term that contributes most significantly to the growth rate as $n$ increases.
  
- **Asymptotic Behavior**: Big Theta notation describes the long-term behavior of functions as $n$approaches infinity, indicating that $f(n)$ and $g(n)$ grow at the same rate.

### Example Interpretation

If $f(n) = n^2 + 3n$, and $g(n) = n^2$, we say $f(n) = \Theta(n^2)$ because there exist constants $c_1 = 1$, $c_2 = 1$, and $n_0 = 1$ such that $n^2 \leq n^2 + 3n \leq n^2$ holds for all $n \geq 1$.

### Practical Use

Big Theta notation is particularly useful in algorithm analysis as it provides a precise description of an algorithm's asymptotic behavior. It indicates both the upper and lower bounds of the growth rate of algorithms' time complexity (and sometimes space complexity), giving a clear understanding of their efficiency across different input sizes.

### Comparison with Big O and Big Omega Notations

- **Big O vs. Big Omega vs. Big Theta**: 
  - Big O provides an upper bound on the growth rate of $f(n)$.
  - Big Omega provides a lower bound on the growth rate of $f(n)$.
  - Big Theta provides both upper and lower bounds, indicating that $f(n)$ grows asymptotically at the same rate as $g(n)$.

In mathematical analysis, small o $o(f(n))$ and small omega $\omega(f(n))$ notations are used to describe the asymptotic behavior of functions in terms of limits. Here’s how they are defined using limits:

### Small o Notation $o(f(n))$

Small o notation $o(f(n))$ denotes that a function $g(n)$ grows asymptotically slower than $f(n)$ as $n$ approaches infinity.

#### Definition:

$$g(n) = o(f(n)) \quad \text{if and only if} \quad \lim_{n \to \infty} \frac{g(n)}{f(n)} = 0$$

In simpler terms, $g(n)$ is in $o(f(n))$ if for every positive constant $c > 0$, there exists a constant $n_0 \geq 0$ such that for all $n \geq n_0$, $|g(n)| < c \cdot |f(n)|$.

### Small Omega Notation $\omega(f(n))$

Small omega notation $\omega(f(n))$ denotes that a function $g(n)$ grows asymptotically faster than $f(n)$ as $n$ approaches infinity.

#### Definition:

$$g(n) = \omega(f(n)) \quad \text{if and only if} \quad \lim_{n \to \infty} \frac{g(n)}{f(n)} = \infty$$

In other words, $g(n)$ is in $\omega(f(n))$ if for every positive constant $c > 0$, there exists a constant $n_0 \geq 0$ such that for all $n \geq n_0$, $|g(n)| > c \cdot |f(n)|$.

### Key Points:

- **Asymptotic Behavior**: Small o notation $o(f(n))$ indicates that $g(n)$ grows slower than $f(n)$ as $n$ becomes large, while small omega $\omega(f(n))$ indicates that $g(n)$ grows faster than $f(n)$.
  
- **Limits**: Both notations are defined using limits to formalize the concept of growth rate in asymptotic analysis.
  
- **Precision**: These notations provide a more precise characterization of asymptotic relationships compared to Big O and Big Omega, especially in contexts where exact growth rates are important.


Afternoon - Data Science Part 2
---------
### Reflection for Last Day:

- Recap of Day 1: Asking Good Questions and basic DataFrame inspections.

If you need to read in the migrations dataset again, here is the code you need.
```python
import pandas as pd

url = 'https://raw.githubusercontent.com/naijacoderorg/lectures/main/lectures2024/datascience/migrations.csv'
df = pd.read_csv(url)
df
```

Last time, we learned how to ask good data questions. Today, we will learn how to find answers to the following data questions. You can add your own questions and follow the principles we learn today to answer them.

<span style="color:blue">**Q1. What were the top 10 migration routes in the world in each of 1960, 1970, 1980, 1990, and 2000?**</span>

<span style="color:blue">**Q2. What were the top 10 migration routes ending in an African country in each of 1960, 1970, 1980, 1990, and 2000?**</span>

<span style="color:blue">**Q3. What are the top 5 continents that Nigerians migrated to in 2000?**</span>

<span style="color:blue">**Q4. Ghana-Must-Go. Investigate this phenomenon by plotting a line graph showing Nigeria-to-Ghana and Ghana-to-Nigeria migrations from 1960 to 2000. Then compare your results with the story in this [article](https://atavist.mg.co.za/ghana-must-go-the-ugly-history-of-africas-most-famous-bag/).**</span>

#### Learning Objectives
By the end of today's session, you will have learned to:
- Manipulate dataframes to find answers to your data questions
- Select a column from a dataset
- Filter data based on some conditions
- Sort a dataset based on the values of some columns
- Group and aggregate data to calculate summary statistics for each group
- Generate plots to visualize your data


### Concepts

To prepare us to answer our data questions, we will learn some important concepts.

_Note: `df` is our input dataset. We will use more descriptive names for any new datasets we create._

#### 1. Selecting columns

To select columns in a DataFrame, we pass a list of column names enclosed within square brackets after the DataFrame name. Since a list is also created using square brackets, this results in double square brackets.

```python
df[['dest_country']] # select a single column
df[['origin_country', 'dest_country']] # select multiple columns
```

#### 2. Sorting Data

Using the `sort_values()` method, we can sort (arrange) the rows of a DataFrame based on the values of one or more columns. This can be useful if you want to present your results in ascending or descending order.

Let's sort `df` **by** the values in the `1960` column in **descending** order.

```python
df.sort_values(by='1960', ascending=False)
```

We can also sort by more than one column, which is useful when we want to apply a secondary sorting criterion to break ties in the primary sort. For example, if we want to sort our input dataset `df` by the destination country first, but then sort by the origin country when the destination values are the same, we can achieve this using multi-column sorting.

```python
df.sort_values(by=['dest_country', 'origin_country']) # pass a list into the 'by' argument to sort by multiple columns
```

We are now ready to answer our first question restated below:

<span style="color:blue">**Q1. What were the top 10 migration routes in the world in each of 1960, 1970, 1980, 1990, and 2000?**</span>


First, the game plan:
- Create a different table for each year
- Select only the necessary columns for each table: `origin_country`, `dest_country` and the year
- Sort by values in the year column in descending order
- Display only the top 10 rows

Here is how we would answer this question for 1960.

```python
top_immigrations_1960 = df[['origin_country', 'dest_country', '1960']].sort_values(by='1960', ascending=False).head(10)
top_immigrations_1960
```

In the last code chunk, we sequentially applied column selections and methods to our starting dataset. Sometimes, the code generated in this process can get really long and messy. In such situations, we can break it into several lines by wrapping the whole operation in parentheses. This makes the code more readable while performing the same operations.

```python
top_immigrations_1960b = (
    df[['origin_country', 'dest_country', '1960']]
    .sort_values(by='1960', ascending=False)
    .head(10)
)

top_immigrations_1960b
```

##### Practice Exercise 1
Now, answer the question for the other years.

#### 3. Filtering Data

Filtering in data analysis involves selecting rows from a DataFrame that meet specific conditions. This allows you to focus on subsets of the data that are relevant to your analysis. For example, you can filter rows based on column values, such as selecting only the rows where a particular column's value exceeds a certain threshold. This is done by applying logical conditions directly to the DataFrame.

Let's say we want to filter the data to contain only rows that have information on migrations FROM Ghana. What kind of logic should we apply?

First of all, we need to find the column that contains information on migration origins, which in this case is `'origin_country'`. We will use this column to create a filtering criterion: `'origin_country' == 'Ghana'`. Next, we use this criterion to apply a boolean condition on the dataset.

```python
df[df['origin_country'] == 'Ghana']

# LET'S BREAK DOWN THIS CODE
### df['origin_country'] SELECTS A COLUMN
### df['origin_country'] == 'Ghana' CHECKS IF THE ROWS OF THAT COLUMN ARE EQUAL TO 'GHANA'. FOR EACH ROW, THIS RETURNS TRUE OR FALSE.
### df[df['origin_country'] == 'Ghana'] RETURNS ONLY ROWS OF df THAT MEET THE CONDITION ABOVE
```

##### Practice Exercise 2

- Create two datasets named `emigrations_NGA` and `immigrations_NGA` containing only rows that satisfy the description in the names.

###### Filtering on Multiple Conditions

We can also apply multiple conditions when filtering data. Let's create a dataset named `nonzero_emigrations_NGA_2000` containing only rows of migrations from Nigeria with values greater than 0 in the year 2000. _Note that for compound conditions, we put each condition in parentheses to keep the logic clear._

```python
nonzero_emigrations_NGA_2000 = df[
    (df["origin_country"] == "Nigeria") &
    (df['2000'] > 0)
]

nonzero_emigrations_NGA_2000 #note that all migrations in this dataset originate from Nigeria and the 2000 column contains only nonzero values
```

We are now ready to answer the second question restated below:

<span style="color:blue">**Q2. What were the top 10 migration routes ending in an African country in each of 1960, 1970, 1980, 1990, and 2000?**</span>

Game plan:
- Create a filtered dataset containing migrations to African countries only
- Select only the necessary columns for each table: `origin_country`, `dest_country`, and the year
- Sort by values in the year column in descending order
- Display only the top 10 rows

Here is an example for 1960. Do you notice anything interesting in the results?

```python
top_african_immigrations_1960 = (
    df[df["dest_continent"] == "Africa"]
    [['origin_country', 'dest_country', '1960']]
    .sort_values(by='1960', ascending=False)
    .head(10)
)

top_african_immigrations_1960
```

###### Practice Exercise 3

Now, go ahead and create your own datasets for the other years.






#### 4. Grouping and Aggregating Data

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

If we want to find the sum of migrations for each origin country, we can group `df` by `origin_country` and then find the sum of migrations for each year column.

In the code below, notice the sequential application of the `.groupby()` and `.sum()` methods. We first apply `.groupby()` and then apply the sum aggregation.

```python
# Group data by origin and sum the migrations
emigrations_total = (df[['origin_country', '1960', '1970', '1980', '1990', '2000']] #select the relevant columns
                     .groupby('origin_country') #groupby
                     .sum() #aggregate
                     .reset_index()
                    )
emigrations_total
```

We are ready to answer our third data question restated below:

<span style="color:blue">**Q3. What are the top 5 continents that Nigerians migrated to in 2000?**</span>

Game plan:
- Filter for rows with origin country equal to Nigeria
- Group by origin country and destination continent
- Select the '2000' column before aggregating
- Aggregate using a sum function
- Reset index. This step is necessary to add our grouping variables back into the dataset as columns instead of as indices.
- Sort values in descending order

```python
NGA_continent_emigrations = (df[df['origin_country'] == 'Nigeria']
                             .groupby(['origin_country','dest_continent'])
                             ['2000']
                             .sum()
                             .reset_index()
                             .sort_values(by='2000', ascending=False)
                            )

NGA_continent_emigrations
```

#### 5. Visualizing the data

Visualization is key in data analysis because it turns complex numbers into pictures that are easier to understand. By using charts and graphs, we can quickly spot patterns and trends, making it easier to see what's important. This helps us make better decisions because we can base them on clear, visual information instead of just numbers.

We will use the matplotlib library for visualizing our data. Matplotlib is a powerful and widely-used Python library for creating static, animated, and interactive visualizations.

We start by importing matplotlib using an alias _plt_.

```python
import matplotlib.pyplot as plt
```

To generate a plot, we write several lines of code, each line calling a **pyplot** method (function) that serves a specific purpose. Here’s a brief explanation of the common methods used in `matplotlib.pyplot (plt)` and why they are essential for creating a visual:

- `plt.figure()`: This method creates a new figure or canvas for the plot. It’s like setting up a blank sheet of paper where you’ll draw your chart. You can also specify the size of the figure here using the `figsize` parameter.

- Depending on the type of plot we want to create, we can use one of the following methods.

    - `plt.plot()`: This is the core method for creating a line plot. You pass in the data you want to visualize, and plt.plot() draws the lines connecting your data points. It’s the main action that puts the data on the canvas.
    
    - `plt.scatter()`: Creates a scatter plot, which is used to show the relationship between two variables. It displays individual data points as dots, making it easier to see patterns or correlations.
    
    - `plt.bar()`: Generates a bar chart, which is useful for comparing categorical data. Bars represent the frequency or amount of each category, allowing for easy comparison.

    - `plt.hist()`: Creates a histogram, which is used to show the distribution of a dataset. It groups data into bins and displays the frequency of data points within each bin.
    
    - `plt.boxplot()`: Produces a box plot, which visualizes the distribution of data based on quartiles. It highlights the median, quartiles, and outliers, providing insights into the data’s spread and variability.
    
    - `plt.pie()`: Makes a pie chart, which shows the proportion of each category as a slice of a pie. It’s useful for illustrating how different parts make up a whole.
    
    - `plt.barh()`: Creates a horizontal bar chart, similar to plt.bar() but with bars oriented horizontally. This can be useful for displaying longer category names.

- `plt.title()`: This method adds a title to your plot. It’s important because it gives context to the visual, letting the viewer know what the data represents.

- `plt.xlabel()` and `plt.ylabel()`: These methods label the x-axis and y-axis, respectively. Labels are crucial because they tell the viewer what each axis represents, making the chart easier to understand.

- `plt.legend()`: When you have multiple lines or data series in one plot, the legend helps identify which line corresponds to which data. It adds a small box that labels each line, making the plot clearer.

- `plt.show()`: This method displays the plot. Without it, the plot might not appear, especially in some programming environments. It’s like hitting the “display” button to see the final chart.

Each of these methods contributes to creating a clear, informative, and visually appealing plot that effectively communicates the data to the viewer.

##### Example

Using a bar graph, visualize the number of migrations from Nigeria in 2000 by destination continent. _Hint:_ Use the dataset you created for Q3.

```python
# Create the bar chart
plt.figure(figsize=(10, 6))  # Optional: Set the figure size
plt.bar(NGA_continent_emigrations['dest_continent'], NGA_continent_emigrations['2000'], color='green') # first arg is for x-axis, second arg is for y-axis, we can optionally specify a color for the bars

# Add labels and title
plt.xlabel('Destination Continent')
plt.ylabel('Number of Emigrations')
plt.title('Migrations from Nigeria in 2000 by Destination Continent')

# Display the plot
plt.show()
```

You can now attempt Q4 restated below using the concepts we have learned today.

<span style="color:blue">**Q4. Ghana-Must-Go. Investigate this phenomenon by plotting a line graph showing Nigeria-to-Ghana and Ghana-to-Nigeria migrations from 1960 to 2000. Then compare your results with the story in this [article](https://atavist.mg.co.za/ghana-must-go-the-ugly-history-of-africas-most-famous-bag/).**</span>



Exercises
---------

### Exercise 1: Identifying Notations

For each pair of functions $f(n)$ and $g(n)$, determine whether $f(n)$ is in Big O, Small o, Big Theta, Small omega, or Big Omega relative to $g(n)$.

1. $f(n) = 2n + 1$, $g(n) = n$
2. $f(n) = n^2$, $g(n) = 3n^2$
3. $f(n) = \log n$, $g(n) = \sqrt{n}$
4. $f(n) = n^{0.5}$, $g(n) = n^{0.4}$
5. $f(n) = n \log n$, $g(n) = n$

### Exercise 2: Verifying Limits

Determine whether the following statements are true (T) or false (F):

1. $n^2 = O(n^3)$
2. $n^2 = o(n^3)$
3. $n^2 = \Theta(n^2)$
4. $n^2 = \omega(n)$
5. $n^2 = \Omega(n^2)$

### Exercise 3: Matching Functions

Match each function $f(n)$ with the appropriate notation (Big O, Small o, Big Theta, Small omega, Big Omega) describing its asymptotic behavior:

1. $f(n) = n^2$
2. $f(n) = \log n$
3. $f(n) = 3n + 5$
4. $f(n) = n^{0.5}$
5. $f(n) = 2^n$
