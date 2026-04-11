---
name: Diet Plan Designer
description: Generates a personalized diet plan with calorie target, macronutrient split (protein, fat, carbs), and sample meals based on user profile (age, weight, height, gender, activity level, goal).
author: Ashif Ahmed Shuvo
version: 1.0.0
---

# Instructions
When the user provides their profile or asks for a diet plan:

1. **Extract the following parameters** (use defaults if missing):
   - `age` (years, default 30)
   - `weight` (kg, default 70)
   - `height` (cm, default 170)
   - `gender` ("male" or "female", default "male")
   - `activity` ("sedentary", "light", "moderate", "active", "very active", default "moderate")
   - `goal` ("lose", "maintain", "gain", default "maintain")

2. **Call the `run_js` tool** with the following JSON schema:

```json
{
  "age": 30,
  "weight": 70,
  "height": 170,
  "gender": "male",
  "activity": "moderate",
  "goal": "maintain"
}