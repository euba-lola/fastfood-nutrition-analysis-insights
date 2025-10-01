# FAST FOOD NUTRITION ANALYSIS 
**EDA Project: From Raw Data → Health Insights**  

---

## Project Overview  

Fast food is cheap, quick, and tasty but also a major driver of excess calories, sodium, saturated fat, and sugar in the modern diet.  
This project uses **Exploratory Data Analysis (EDA)** and **feature engineering** to uncover the hidden nutritional risks of popular menu items.  

As a **data scientist**, I wanted to let the numbers tell the story.  
As a **dietitian**, I wanted to make the story easy for people and policymakers to understand.  

---

 **Goals:**  
- Benchmark fast food against **global dietary guidelines** (WHO/USDA).  
- Show which **restaurants** and **categories** (burgers, pizza, salads, etc.) are most risky.  
- Build a **traffic-light system** (safe, moderate, high risk).  
- Use **PCA** to map foods into a **nutritional universe** (calorie bombs, sugar bombs, sodium bombs).  

---

## Objectives  

1. Benchmark nutrients vs WHO/USDA dietary guidelines.  
2. Engineer risk-related features (high sodium, fat, sugar, calories).  
3. Evaluate risks **by restaurant** and **by food category**.  
4. Visualize with barplots, scatterplots, word clouds, treemaps, pie charts.  
5. Classify foods using a traffic-light system.  
6. Perform PCA to cluster foods into “safe” vs “danger” groups.  
7. Translate findings into **consumer & policy recommendations**.  

---

## Project Workflow  

### 1. Data Cleaning & Prep  
- Loaded dataset → removed unwanted columns (`item`, `food_category`)  
- Split features into **categorical** and **numerical**  
- Checked distributions, missing values, outliers  

---

### 2. Feature Engineering  
- Created binary “red-flag” features for exceeding guidelines:  
  - `high_sodium` ( > 2300 mg )  
  - `high_satfat` ( > 20 g )  
  - `high_sugar` ( > 50 g )  
  - `high_calories` ( > 600 kcal )  
- Built **aggregate risk feature** (`any_redflag`).  
- Designed **traffic light system**:  
  - Green → safe  
  - Yellow → moderate risk  
  - Red → high risk  

---

### 3. Exploratory Data Analysis (EDA)  

- **Categorical variables**  
  - Countplots (vertical & horizontal)  
  - Pie charts (proportion)  
  - Percentage barplots  
  - Word cloud (with black background)  
  - Treemap (sized by counts)  
  - Markdown commentary for insights  

 *Insight:* Mexican, Sandwich, and Burger dominate (~50% of dataset). Seafood and Pizza are rare.  

- **Numerical variables**  
  - Scatterplots for Calories vs Saturated Fat, Calories vs Sugar  
  - Correlation heatmaps  
  - Boxplots of calories, sodium, fat by category  

 *Insight:* As saturated fat ↑, calories ↑ (fat = calorie dense).  
Desserts/drinks = sugar bombs; meals = fat/sodium bombs.  

---

### 4. Nutrient Benchmarking  
- Compared nutrients vs recommended daily intake.  
- % of daily sodium, sugar, fat, fiber per item shown in barplots & radar charts.  

 *Finding:* Avg item = 54% sodium, 40% fat, but only 16% fiber.  

---

### 5. Risk Dashboards  

- **Restaurant-level** → stacked bar charts showing % Green, Yellow, Red foods per chain  
  - Subway & Chick-Fil-A = more Green options  
  - Burger King, Sonic, McDonald’s = more Red flags  

- **Category-level** → heatmaps and bars  
  - Pizza & Burgers = highest calorie + fat risks  
  - Chicken Strips/Nuggets = sodium + fat danger  
  - Seafood & Salads = safest, but watch dressing sodium  

---

### 6. Traffic-Light System  

- Safe → 65%  
- Moderate → 25%  
- High Risk → 10%  

 *BUT:* Meal combos (burger + fries + soda) push even Green → Red territory.  

---

### 7. PCA Nutritional Map  
- Reduced multiple nutrient variables into 2D “nutritional universe.”  
- Clusters emerge:  
  - Pizza & Burgers → far right = Calorie/Fat bombs  
  - Fried strips/wraps → sodium-heavy zones  
  - Desserts &  drinks → sugar clusters  
  - Salads & seafood → center = safest  

---

## Key Takeaways  

- **Sodium = #1 villain** → half daily intake in just one item.  
- **Calories & Sat Fat** = travel together, making burgers/pizzas “double trouble.”  
- **Sugar** mainly from drinks/desserts, but single shake > 3× WHO daily safe limit.  
- **Fiber deficiency** → only ~16% of daily needs per item → nutrient imbalance.  

---

## Health Advice  

- Safer: grilled chicken, seafood, simple salads.  
- Moderate: wraps/sandwiches, careful with sauces/dressings.  
- Limit: pizza, burgers, fried strips, sugary drinks/combo meals.  
- Pair fast food with **fiber-rich foods** at home to balance nutrition.  

**Policy:**  
- Push for **clear menu labeling (traffic-light style)**.  
- Restructure menus to encourage lower sodium/fat items.  
- Reformulate items to cut sodium and unhealthy fats.  

---

## Tools & Libraries  

- Python (Pandas, NumPy)  
- Visualization: Matplotlib, Seaborn  
- Special Plots: WordCloud, Squarify  
- Feature Engineering/ML: Scikit-learn (PCA)  

---

## Visual Gallery  

*(examples: replace these with your saved `.png`s in an `/images` folder)*  

```markdown
![Food Categories Count](images/food_categories_countplot.png)  
![Percentage Barplot](images/food_categories_percentage_barplot.png)  
![Word Cloud](images/food_categories_wordcloud.png)  
![Treemap](images/food_categories_treemap.png)  
![Calories vs Saturated Fat](images/calories_vs_satfat.png)  
![Calories vs Sugar](images/calories_vs_sugar.png)  
![Traffic Light Pie](images/traffic_light_pie.png)  
![PCA Nutritional Map](images/pca_map.png)

---
