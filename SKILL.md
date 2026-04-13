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