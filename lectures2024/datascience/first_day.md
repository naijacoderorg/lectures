Day 1: Introduction to Data Science
===================================

Data science is a growing field that combines mathematics, statistics, and computer science to extract meaningful insights from data. By analyzing and interpreting large amounts of information, data scientists can uncover patterns, make predictions, and help solve complex problems. In this introduction to data science, you will learn how to use Python to analyze real-world data.

Japa!
-----

Every data science project begins with data, and understanding the context behind the data is crucial for gaining meaningful insights.

Our dataset is extracted from the [World Bank's](https://databank.worldbank.org/source/global-bilateral-migration) Global Bilateral Migration database. The dataset provides detailed information on international migration patterns between countries. It includes data on the number of migrants by origin and destination countries, from 1960 to 2000, in ten-year intervals. This dataset can help in analyzing migration trends, demographic changes, and the impacts of migration on economies and societies globally. It is a valuable resource for researchers, policymakers, and organizations involved in migration studies and related fields.

*For our project, we will use a subset of this data containing only African origin countries.*

Let's spend some time exploring the dataset.

### Load the data

We begin by loading the data into Python using the `pandas` library which offers many useful functions for reading data. Our dataset is a CSV file stored in a GitHub repository; hence, we will use its URL with the `read_csv()` function to access it. _You can find more examples on reading in csv files [here](https://www.geeksforgeeks.org/reading-csv-files-in-python/)._

```python
import pandas as pd

url = 'https://raw.githubusercontent.com/naijacoderorg/lectures/main/lectures2024/day5/migration_africa.csv'
df = pd.read_csv(url)
```
df is short form for DataFrame. It's a lazy way to name our initial dataset. We should be more specific in our naming in the future.

### Pandas DataFrame Attributes and Methods

Let's check what class our data object has inherited.

```python
df.__class__ # check for the class of df
```
As a pandas dataframe, our `df` object has certain attributes and methods. An attribute in programming is a property of an object that stores data about that object. A method is a function that can perform an action on an object of the specified class. Both attributes and methods are accessed using dot notation, but methods additionally have parentheses `()`, even when no arguments are specified.

Let's explore some DataFrame attributes and methods for our dataset.

#### `.head()` displays the first few rows of the DataFrame

By default, only the first five rows are displayed. To get a different number of rows, you can specify that in the argument, like `df.head(10)`.

```python
df.head()
```

Our dataset is tabular. This means that it has rows and columns. The rows represent a single observation, and the columns are features that contain specific information (like country of origin) on each observation. 

Whenever we explore a dataset, one of the first questions we ask ourselves is this: **What is the level of an observation?** Can you describe what information a specific row gives you?

In this case, each row of the dataset represents a specific migration flow over time. For example, the first row shows the number of migrations from Nigeria (the origin) to Afghanistan (the destination) for the years 1960, 1970, 1980, 1990, and 2000. We always spend time ensuring that we understand what each observation represents as the rest of our analysis is hinged on this knowledge.

#### `.shape` displays the number of rows and columns

We can also check for the dimensions (number of rows and columns) of our dataset using the `.shape` attribute. Try to interpret the result you get? Why do you think the dataset is this large? We'll explore this later, but feel free to brainstorm now.

```python
df.shape
```

Try out the following attributes and methods to learn more about your dataset.
+ df.columns
+ df.dtypes
+ df.index
+ df.size
+ df.values
+ df.info()
+ df.describe()
+ df.isnull().sum()

## Asking Good Data Questions

In tomorrow's session, we will spend some time exploring the data more deeply and finding exact answers to questions we have about the data. But today, we need to learn how to generate effective data questions that can lead to valuable insights and informed decision-making.

### Principles for Formulating Good Data Questions

#### 1. Specificity

- Good questions are specific. Vague questions lead to unclear answers. Specific questions narrow down the focus and make it easier to find precise answers.
- Example: Instead of asking "How are our sales?", ask "How did our sales perform in the last quarter compared to the previous quarter?"

#### 2. Measurability

- Questions should be measurable and quantifiable. If you can't measure it, you can't analyze it.
- Example: "What is the average customer satisfaction score for the past six months?" rather than "Are our customers happy?"

#### 3. Relevance:

- Questions should be relevant to the business goals or research objectives. They should address a real need or problem.
- Example: "Which marketing channel has the highest return on investment in the past year?" is more relevant than "What are all the marketing channels we use?"

#### 4. Actionability:

- A good data question leads to actionable insights. The answers should help make decisions or drive actions.
- Example: "What are the top three reasons customers are canceling their subscriptions?" This can lead to actions to reduce churn.

In our work this week, we will ensure that our questions always satisfy Principles 1 and 2. While our questions may not always meet Principles 3 and 4, these principles will become more useful as we begin practicing asking data questions in real-world situations beyond this camp.

### Steps to Formulate Good Data Questions:

#### 1. Identify the Objective:

- Start by understanding the problem or goal. What do you want to achieve with this analysis?
- Example: If the goal is to increase sales, your questions should focus on factors influencing sales.

#### 2. Break Down the Problem:

- Divide the main objective into smaller, more manageable questions.
- Example: Instead of "How can we increase sales?", ask "Which products have seen a decline in sales?", "Which customer segments are underperforming?", and "Which marketing campaigns were most effective?"

#### 3. Consider the Data Available:

- Ensure that the questions can be answered with the data you have or can realistically obtain.
- Example: If you have sales data by region, you can ask "Which regions have the highest growth in sales?"

#### 4. Iterate and Refine:

- Continuously refine your questions based on initial findings and feedback.
- Example: After analyzing the initial sales data, you might refine the question to focus on a specific product line or customer segment.

### Brainstorming Activity

In small groups, let's practice coming up with good questions based on our dataset. In your group, brainstorm a list of specific, measurable, (relevant), and (actionable) questions that you would ask.

When the time is up, you will present your questions to the class.
