# 🎯 AI Best Practices for Data Science

## Guidelines for Using ChatGPT, Claude, and Other AI Tools

---

## ✅ WHEN TO USE AI

### Perfect Use Cases:

**1. Code Generation (Starting Points)**
- ✅ "Write boilerplate code for X"
- ✅ "Create a template function for Y"
- ✅ "Generate example data for testing"

**2. Learning & Understanding**
- ✅ "Explain how X works"
- ✅ "What's the difference between A and B?"
- ✅ "Show me examples of Z"

**3. Debugging**
- ✅ Paste error + code → get suggestions
- ✅ "Why doesn't this work?"
- ✅ "How do I fix this warning?"

**4. Documentation**
- ✅ "Write docstring for this function"
- ✅ "Add comments to this code"
- ✅ "Create README for this analysis"

**5. Code Review**
- ✅ "Is this code efficient?"
- ✅ "Can this be simplified?"
- ✅ "Are there any bugs?"

**6. Alternative Approaches**
- ✅ "Show me 3 ways to do X"
- ✅ "Is there a faster method?"
- ✅ "What's the pandas-idiomatic way?"

---

## ❌ WHEN NOT TO USE AI

### Inappropriate Use Cases:

**1. Critical Statistical Decisions**
- ❌ "Should I drop or impute missing values?"
  - → Depends on YOUR data and domain
- ❌ "Is this result statistically significant?"
  - → Calculate yourself, don't trust AI

**2. Domain-Specific Judgments**
- ❌ "What does this income distribution mean for policy?"
  - → Requires domain expertise
- ❌ "Is this outlier real or an error?"
  - → Need to understand your data source

**3. Data Privacy/Security**
- ❌ Don't paste actual sensitive data
- ❌ Don't share personal information
- ❌ Don't upload confidential datasets

**4. Complete Replacement for Learning**
- ❌ Using AI without understanding
- ❌ Copying code blindly
- ❌ Skipping learning fundamentals

---

## 🔍 VERIFICATION CHECKLIST

### Before Using AI Code:

**1. Read and Understand**
```
✓ Can you explain each line?
✓ Do you understand why it works?
✓ Could you modify it if needed?
```

**2. Test Thoroughly**
```
✓ Run on sample data first
✓ Check edge cases
✓ Verify output manually for small dataset
```

**3. Check Documentation**
```
✓ Are functions real? (pandas docs)
✓ Is syntax current? (not deprecated)
✓ Are parameters correct?
```

**4. Validate Logic**
```
✓ Does statistical approach make sense?
✓ Are assumptions valid for your data?
✓ Would a domain expert agree?
```

---

## 🎓 LEARNING WITH AI (Not Just Using)

### Effective Learning Strategy:

**BEFORE asking AI:**
1. Try to solve it yourself (15-30 min)
2. Identify specific stuck points
3. Form specific questions

**WHEN asking AI:**
1. Ask for explanation BEFORE code
2. Request step-by-step breakdown
3. Ask "why" for each recommendation

**AFTER getting AI response:**
1. Test code on small dataset
2. Modify code to understand it
3. Try similar problem without AI
4. Explain solution to someone else

### Example:
```
❌ Bad: "Write code to clean my data"
      → Just copy-paste, learn nothing

✅ Good: "I tried cleaning with fillna(0) but got unexpected results.
         Explain when fillna(0) is appropriate vs median imputation.
         Then show examples of each."
      → Understand concepts, learn when to apply
```

---

## ⚠️ COMMON AI MISTAKES

### 1. Hallucinations (Fake Functions)

**Problem:** AI invents functions that don't exist

```python
# ❌ AI might suggest:
df.calculate_gini_coefficient()  # Doesn't exist!
df.create_quintiles()             # Doesn't exist!
```

**Solution:** Always check pandas documentation
```python
# ✅ Correct:
import numpy as np

def gini_coefficient(x):
    # Manual implementation
    sorted_x = np.sort(x)
    n = len(x)
    cumsum = np.cumsum(sorted_x)
    return (2 * np.sum((n - i) * sorted_x[i] for i in range(n))) / (n * cumsum[-1]) - 1

# OR use external library:
# from gini import gini_coefficient
```

---

### 2. Deprecated Syntax

**Problem:** AI training data includes old pandas

```python
# ❌ AI might suggest (deprecated):
df.ix[0]  # Removed in pandas 1.0+
df.append(new_row)  # Deprecated in pandas 2.0+
```

**Solution:** Check pandas version compatibility
```python
# ✅ Current syntax:
df.iloc[0]  # Use iloc or loc
pd.concat([df, new_row])  # Use concat
```

---

### 3. Inefficient Code

**Problem:** AI might not optimize

```python
# ❌ AI might suggest:
result = []
for i in range(len(df)):
    result.append(df.loc[i, 'A'] * 2)
df['B'] = result
```

**Solution:** Ask for vectorized version
```python
# ✅ Vectorized (much faster):
df['B'] = df['A'] * 2
```

---

### 4. Wrong Statistical Advice

**Problem:** AI doesn't understand your data distribution

```python
# ❌ AI might say: "Always use mean for imputation"
df['income'].fillna(df['income'].mean())
```

**Reality:** For skewed data (like income), median is usually better!
```python
# ✅ Better for skewed distributions:
df['income'].fillna(df['income'].median())
```

---

## 📊 CASE STUDY: Good vs Bad AI Usage

### Scenario: Missing Income Data

**❌ BAD Approach:**
```
You: "I have missing income data. Fix it."

AI: "Use mean imputation: df['income'].fillna(df['income'].mean())"

You: [Copies code without thinking]
```

**Problems:**
- No context provided
- No understanding of impact
- No validation
- Might distort distribution

---

**✅ GOOD Approach:**
```
You: "I have household income data (HY010) from EU-SILC survey.
     About 3% values are missing.
     Distribution is right-skewed (median=15k, mean=18k).
     I need these values for inequality analysis (quintiles).

     Questions:
     1. Should I drop rows or impute?
     2. If impute, mean or median?
     3. What's the impact on quintile analysis?"

AI: "Good context! Here's analysis:

     1. Drop vs Impute:
        - 3% is low, could drop
        - But imputation preserves sample size

     2. Mean vs Median:
        - Your data is right-skewed
        - Mean (18k) > Median (15k)
        - Median is more robust for skewed data
        - Use median to avoid inflating imputed values

     3. Impact on quintiles:
        - Median imputation: minimal impact
        - Mean imputation: would shift distribution right
        - Dropping: might bias if missingness not random

     Recommendation: Median imputation
     But ALSO try analysis with dropped rows to compare!"

You: "Makes sense! Let me try both approaches and compare."
```

**Why Better:**
- Provided context
- Asked multiple questions
- Got nuanced answer
- Plans to validate with comparison
- Understands trade-offs

---

## 🛡️ SAFETY & ETHICS

### Data Privacy:

**❌ NEVER share:**
- Real names, addresses, IDs
- Sensitive personal data
- Proprietary company data
- Data under NDA

**✅ SAFE to share:**
- Anonymized/synthetic data
- Public dataset samples
- General data structure
- Statistical summaries

### Example:
```
❌ BAD:
"Here's data from our customer database: [pastes real data]"

✅ GOOD:
"I have a DataFrame with structure:
 - customer_id (int)
 - purchase_amount (float)
 - date (datetime)
 Sample (fictional):
 1001, 50.5, 2023-01-15
 How do I calculate monthly totals?"
```

---

### Academic Integrity:

**If using AI for homework:**
- ✅ Use for understanding concepts
- ✅ Use for debugging your code
- ✅ Use for learning syntax
- ❌ Don't submit AI code as your work
- ❌ Don't let AI do the thinking

**Ethical use:**
1. Understand everything you submit
2. Cite AI assistance if required
3. Use AI to learn, not to cheat
4. Be able to explain your code

---

## 📈 WORKFLOW RECOMMENDATIONS

### Ideal AI-Assisted Workflow:

**Step 1: Try Yourself (15-30 min)**
```
- Attempt the problem
- Google pandas documentation
- Try basic approaches
- Note what doesn't work
```

**Step 2: Targeted AI Help**
```
- Ask specific questions on stuck points
- Request explanation, not just code
- Compare AI approach with yours
```

**Step 3: Understand & Modify**
```
- Read AI code line by line
- Change parameters to see effects
- Test on different data
- Break it intentionally to understand
```

**Step 4: Validate**
```
- Check results make sense
- Compare with manual calculation
- Test edge cases
- Review with domain knowledge
```

**Step 5: Document**
```
- Add comments explaining "why"
- Note assumptions
- Document validation steps
```

---

## 🎯 PROMPT QUALITY MATTERS

### Improving Prompt Quality:

**Level 1 (Beginner):**
```
"help with pandas"
→ Too vague, will get generic response
```

**Level 2 (Better):**
```
"how to filter dataframe"
→ More specific, but still generic
```

**Level 3 (Good):**
```
"how to filter pandas dataframe where column A > 5"
→ Specific operation, clear goal
```

**Level 4 (Excellent):**
```
"I have a pandas DataFrame with columns 'income' (float) and 'region' (str).
 I want to filter rows where income > 5000 AND region is 'urban'.
 Show code and explain the logic of combining conditions."
→ Context, goal, input types, specific request
```

---

## 💡 PRO TIPS

### 1. Iterate and Refine
```
First prompt: Get basic code
Follow-up 1: "Can this be more efficient?"
Follow-up 2: "How does this handle missing values?"
Follow-up 3: "Show me a test case"
```

### 2. Ask for Alternatives
```
"Show me 3 ways to do this, with pros/cons of each"
→ Helps you learn different approaches
```

### 3. Request Explanation First
```
"Before showing code, explain the concept of groupby and when to use it"
→ Understand before implementing
```

### 4. Use AI for Code Review
```
"Review this code for potential issues:
 [paste your code]
 Check for: efficiency, edge cases, pandas best practices"
→ Learn from AI's critique
```

### 5. Learn Incrementally
```
"Start with basic groupby, then add multiple aggregations, then add filtering"
→ Build understanding step by step
```

---

## 🎓 SELF-ASSESSMENT

### Check Your AI Usage Health:

**Healthy Signs** ✅
- You can explain AI-generated code
- You modify code to fit your needs
- You catch AI errors
- You learn new concepts from AI
- You use AI less over time (for same tasks)

**Warning Signs** ⚠️
- You copy-paste without reading
- You don't understand the code
- You can't modify it when needed
- You depend on AI for every task
- You never verify results

**If you see warning signs:**
1. Slow down
2. Focus on understanding
3. Practice without AI
4. Review fundamentals
5. Ask "why" more often

---

## 📋 QUICK REFERENCE

### The 5 Commandments of AI Usage:

1. **Understand Before Using**
   - Read every line
   - Explain in your own words
   - Test on simple data

2. **Verify Everything**
   - Check documentation
   - Test edge cases
   - Validate logic

3. **Learn, Don't Copy**
   - Ask for explanations
   - Try modifications
   - Practice similar problems

4. **Context is King**
   - Provide data structure
   - State your goal clearly
   - Include constraints

5. **AI is a Tool, Not a Brain**
   - Make decisions yourself
   - Use domain knowledge
   - Trust but verify

---

## 🎉 CONCLUSION

### Remember:

**AI is AMAZING for:**
- ✅ Learning new concepts
- ✅ Getting unstuck
- ✅ Boosting productivity
- ✅ Exploring alternatives
- ✅ Code review

**But YOU are responsible for:**
- 🧠 Understanding the code
- 🔍 Validating results
- 📊 Statistical decisions
- 🎯 Domain expertise
- ✅ Final output quality

---

**Use AI to become a BETTER data scientist, not to AVOID being one!**

*Happy (responsible) AI-assisted coding! 🤖📊*
