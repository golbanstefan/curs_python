# 🤖 AI Prompts Guide for Data Science

## Effective Prompts for ChatGPT & Claude

---

## 📊 DATA EXPLORATION

### Good Prompts:
```
✅ "Write pandas code to load a CSV file and display the first 5 rows, data types, and missing value count"

✅ "Create a function that takes a DataFrame and returns a summary of missing values per column as a percentage"

✅ "Show me how to check for duplicate rows in a pandas DataFrame"
```

### Bad Prompts:
```
❌ "help with data"  # Too vague
❌ "pandas"  # No context
❌ "fix my code"  # No code provided
```

---

## 🧹 DATA CLEANING

### Good Prompts:
```
✅ "I have a DataFrame with missing values in columns A, B, C. Column A is income (should not be 0), column B is age (numeric), column C is category. Suggest cleaning strategies for each"

✅ "Write a function to replace negative values (-1, -2, -4, -5) with NaN in all numeric columns of a DataFrame"

✅ "How do I convert a column with mixed data types to numeric, handling errors gracefully?"
```

---

## 📈 STATISTICAL ANALYSIS

### Good Prompts:
```
✅ "Write code to calculate income quintiles using pandas qcut and label them Q1-Q5"

✅ "Create a function that calculates the Q5/Q1 income ratio (ratio of mean income in top 20% vs bottom 20%)"

✅ "How do I calculate correlation between all numeric columns and sort by correlation with a specific column?"
```

---

## 📊 VISUALIZATION

### Good Prompts:
```
✅ "Create a matplotlib figure with 2 subplots: left is histogram of income, right is box plot. Add title, labels, and legend"

✅ "Write seaborn code to create a heatmap showing correlation between variables X, Y, Z with annotations"

✅ "How do I create a grouped bar chart comparing mean values across categories?"
```

---

## 🐛 DEBUGGING

### Good Prompts:
```
✅ "I'm getting 'KeyError: column_name'. Here's my code: [paste code]. What's wrong?"

✅ "This code runs but gives wrong results: [paste code]. The expected output is X but I get Y. Why?"

✅ "I get 'SettingWithCopyWarning' when doing df[col] = value. How do I fix it properly?"
```

### Include:
- ✅ Error message (full traceback)
- ✅ Relevant code snippet
- ✅ Expected vs actual behavior
- ✅ Data sample (if safe to share)

---

## 🔍 CODE EXPLANATION

### Good Prompts:
```
✅ "Explain what this code does line by line: [paste code]"

✅ "What's the difference between df.loc[] and df.iloc[]? When should I use each?"

✅ "Explain this groupby operation: df.groupby('category')['value'].agg(['mean', 'sum'])"
```

---

## 🚀 OPTIMIZATION

### Good Prompts:
```
✅ "This code is slow: [paste code]. Can you suggest a faster vectorized approach?"

✅ "I'm using a for loop to calculate X. Is there a pandas method to do this faster?"

✅ "How can I reduce memory usage of this DataFrame that has 1M rows?"
```

---

## 📝 DOCUMENTATION

### Good Prompts:
```
✅ "Write a docstring for this function: [paste function]"

✅ "Add inline comments explaining this complex code: [paste code]"

✅ "Create a README section explaining what this analysis does"
```

---

## ⚠️ PROMPT BEST PRACTICES

### DO:
1. **Be specific**
   - Bad: "help with pandas"
   - Good: "How do I filter a DataFrame where column A > 5 and column B == 'cat'?"

2. **Provide context**
   - Include data structure
   - Mention column names
   - Specify data types

3. **Include examples**
   - Show sample input
   - Show desired output
   - Clarify edge cases

4. **Iterate**
   - Start simple
   - Refine based on response
   - Ask follow-up questions

### DON'T:
1. **Don't be vague**
   - "make it better" → Better how?
   - "fix this" → What's wrong?

2. **Don't paste huge code blocks**
   - Extract relevant section
   - Provide minimal reproducible example

3. **Don't trust without testing**
   - Always run AI code
   - Verify output
   - Check edge cases

---

## 🎯 DOMAIN-SPECIFIC PROMPTS

### Income Inequality Analysis:
```
✅ "Write a function to calculate the Gini coefficient from an array of income values"

✅ "Create a visualization comparing income distribution across urban/rural areas"

✅ "How do I calculate the share of total income held by each quintile?"
```

### EU-SILC Specific:
```
✅ "EU-SILC uses codes -1, -2, -4, -5 for missing values. Write code to convert these to NaN in all numeric columns"

✅ "Create a function to map EU-SILC urbanization codes (1=urban, 2=intermediate, 3=rural) to readable labels"

✅ "How do I calculate equivalized household size for income comparison?"
```

---

## 💡 ADVANCED TECHNIQUES

### Chain of Thought:
```
✅ "I need to analyze income inequality. Let's think step by step:
1. First, explain how to calculate income quintiles
2. Then, show how to calculate mean income per quintile
3. Finally, calculate Q5/Q1 ratio
Provide code for each step."
```

### Comparison Requests:
```
✅ "Compare three approaches to handle missing values: dropping rows, mean imputation, and median imputation. Show code and discuss pros/cons"

✅ "Show me both matplotlib and seaborn approaches to create a histogram. Which is better for my use case?"
```

### Learning-Oriented:
```
✅ "I want to understand groupby better. Create a simple example dataset and show 5 different groupby operations with explanations"

✅ "Explain pivot tables in pandas like I'm 5, then show a real example"
```

---

## 📋 PROMPT TEMPLATES

### Template 1: Code Generation
```
Context: [describe your data and goal]
Input: [sample data structure]
Desired output: [what you want]
Requirements: [specific needs, e.g., handle NaN, performance]

Example:
Context: I have EU-SILC income data with households
Input: DataFrame with columns HB030 (ID), HY010 (income), HH030 (size)
Desired output: Income per capita for each household
Requirements: Handle zero household size gracefully
```

### Template 2: Debugging
```
Problem: [what's wrong]
Code: [paste problematic code]
Error: [full error message]
Expected: [what should happen]
Actual: [what actually happens]
```

### Template 3: Explanation
```
Code: [paste code]
What I think it does: [your understanding]
What I'm unsure about: [specific parts]
Please explain: [what you want clarified]
```

---

## 🎓 LEARNING FROM AI

### How to Learn (Not Just Copy):

1. **Ask for explanation FIRST**
   ```
   ✅ "Explain the concept of groupby before showing code"
   ✅ "What are the steps to handle missing values?"
   ```

2. **Request alternatives**
   ```
   ✅ "Show me 3 different ways to do X, with pros/cons"
   ```

3. **Ask "why"**
   ```
   ✅ "Why use .loc[] instead of direct indexing?"
   ✅ "Why is vectorization faster than loops?"
   ```

4. **Build incrementally**
   ```
   ✅ "First show basic groupby, then add multiple aggregations, then add filtering"
   ```

---

## ⚠️ RED FLAGS (When AI is Wrong)

Watch out for:

1. **Non-existent functions**
   - `df.calculate_gini()` ❌ (doesn't exist in pandas)
   - Always check official docs

2. **Deprecated syntax**
   - `df.ix[]` ❌ (old pandas)
   - `.append()` ❌ (deprecated in pandas 2.0)

3. **Wrong statistical concepts**
   - "Always use mean for imputation" ❌
   - Statistics depend on context!

4. **Inefficient code**
   - AI might suggest loops when vectorization exists
   - Test performance on your data

---

## 📊 EXAMPLE CONVERSATION

**You:**
```
I have a DataFrame with income data (column: HY010).
I want to create 5 equal groups (quintiles) and calculate average income for each group.
Show code and explain each step.
```

**AI (Good Response):**
```python
# Step 1: Create quintiles using pd.qcut
# qcut divides data into equal-sized bins (20% each)
df['quintile'] = pd.qcut(df['HY010'],
                          q=5,  # 5 groups
                          labels=['Q1', 'Q2', 'Q3', 'Q4', 'Q5'])

# Step 2: Calculate mean income per quintile
# groupby groups by quintile, then we calculate mean
quintile_means = df.groupby('quintile')['HY010'].mean()

print(quintile_means)
```

**Explanation:**
- `pd.qcut()` creates equal-frequency bins
- `q=5` means 5 groups (quintiles)
- `labels` assigns names to each group
- `groupby` groups data by quintile
- `.mean()` calculates average for each group


**You (Follow-up):**
```
How is qcut different from cut?
```

**AI:**
```
Great question!

- `pd.cut()`: Equal-width bins
  - Divides range into equal intervals
  - Example: income 0-10k, 10-20k, 20-30k
  - Groups may have different sizes

- `pd.qcut()`: Equal-frequency bins
  - Each group has same number of observations
  - Example: bottom 20%, next 20%, etc.
  - Bin edges may be different widths

For quintiles, use qcut to ensure each group has same size!
```

---

## 🎯 SUMMARY

### Key Principles:
1. **Be specific** - context is everything
2. **Provide examples** - input/output samples
3. **Verify always** - test AI code
4. **Learn, don't copy** - understand before using
5. **Iterate** - refine prompts based on responses

### Remember:
- ✅ AI is a tool to boost productivity
- ✅ You must understand the code
- ✅ Always verify statistical claims
- ❌ Never trust blindly
- ❌ Don't use for critical decisions without validation

---

**Happy prompting! 🤖📊**

*Use AI to learn faster, not to avoid learning!*
