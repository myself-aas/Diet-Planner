---
name: Diet-Planner
description: Generates a personalized diet plan with calorie target, macronutrient split, and sample meals based on user profile.
author: Ashif Ahmed Shuvo
version: 1.0.1
---

# Diet Plan Designer

## Instructions
When the user provides a profile or asks for a diet plan:

1. **Extract the following parameters** from the user profile and use defaults if missing:
   - `age` (years, default 30)
   - `weight` (kg, default 70)
   - `height` (cm, default 170)
   - `gender` (`male` or `female`, default `male`)
   - `activity` (`sedentary`, `light`, `moderate`, `active`, `very active`, default `moderate`)
   - `goal` (`lose`, `maintain`, `gain`, default `maintain`)

2. **Call the `run_js` tool** with the following exact parameters:
   - `script name`: `index.html`
   - `data`: A JSON string containing only the fields below:
     ```json
     {
       "age": 30,
       "weight": 70,
       "height": 170,
       "gender": "male",
       "activity": "moderate",
       "goal": "maintain"
     }
     ```

   > ⚠️ Important: Do not include extra wrapper fields such as `skill_name`, `tool`, or any metadata. The skill should receive only the user profile parameters.

3. **Return a short confirmation** that the diet plan is being generated.

The skill returns an interactive webview displaying a macronutrient pie chart and a sample meal plan.

## Overview
The Diet-Planner project assists users in planning and maintaining a healthy diet based on their nutritional requirements and preferences. The application provides recommendations for meals, calculates nutritional information, and tracks dietary habits.

## Advanced Features
1. **Personalization**: Users can input dietary restrictions, preferences, and goals (like weight loss, muscle gain, etc.) to receive tailored meal plans.
2. **Nutritional Calculator**: This feature calculates daily caloric and macronutrient requirements based on individual profiles that include age, weight, height, activity level, and goals.
3. **Meal Recommendations**: The system suggests meals that align with the user's nutritional needs and taste preferences, utilizing a comprehensive database of recipes.
4. **Integration with External APIs**: The application can integrate with various food databases to fetch updated nutritional information for a vast range of ingredients.
5. **User Tracking**: Users can log their meals and snacks, track their progress towards dietary goals, and receive insights into their eating habits.

## Calculation Methods
- **Caloric Needs**: Utilizes the Mifflin-St Jeor Equation to estimate BMR (Basal Metabolic Rate), adjusted by the activity factor to calculate Total Daily Energy Expenditure (TDEE).
- **Macronutrient Split**: Based on user goals, the application calculates the percentage of calories coming from carbohydrates, proteins, and fats. Recommended splits can vary by goal:
   - Weight Loss: 40% Carbs - 30% Protein - 30% Fat
   - Muscle Gain: 50% Carbs - 30% Protein - 20% Fat
   - Maintenance: 45% Carbs - 25% Protein - 30% Fat

## Output Specifications
- **Meal Plans**: Outputs a structured list of recommended meals and snacks for the week, including portion sizes and caloric values.
- **Nutritional Summary**: Provides a daily breakdown of nutrients consumed, comparing them against user goals and recommendations.
- **Progress Reports**: Generates weekly reports that track weight changes and adherence to dietary recommendations, allowing users to visualize their progress over time.

## Conclusion
The Diet-Planner project not only helps users to plan meals but also empowers them with the knowledge needed to make healthier food choices in accordance with their individual lifestyle and goals.