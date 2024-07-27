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

'''
df is short form for DataFrame.
It's a lazy way to name our initial dataset.
We will be more specific in our naming in the future.
'''
```

