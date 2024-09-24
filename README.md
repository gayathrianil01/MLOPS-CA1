
Nutrition Data
This Python script generates a random CSV file with user data, including columns for `User id`, `Age`, `Weight`, `Dietary Preferences`, and `Recommended Calories`.

- Randomly generates user IDs with the format `UID0001`, `UID0002`, etc.
- Randomly assigns ages between 18 and 65.
- Randomly assigns weights between 50 kg and 120 kg.
- Randomly assigns dietary preferences (Vegan, Vegetarian, Non-Vegetarian, Keto, Paleo).
- Randomly assigns recommended calories between 1500 and 3000.


Features
1. User ID Generation
Each user is assigned a unique identifier (User ID) in the format UIDxxxx, where xxxx is a zero-padded number starting from 0001. This ensures that every user has a distinct and easily recognizable ID.

Purpose:
Acts as a unique identifier for each record.
Ensures that no two users have the same ID.
Makes it easier to reference and track individual users in the dataset.
Example:
UID0001, UID0002, UID0003, etc.
2. Age Generation
A random integer value between 18 and 65 is generated for each user, representing their age.

Purpose:
Simulates a user’s age to reflect a realistic distribution for adults.
Provides variability in the dataset to help with analysis or testing.
Example:
24, 35, 61, etc.
3. Weight Generation
The weight of each user is randomly generated as a floating-point value between 50.0 kg and 120.0 kg, representing a realistic range for adult body weights.

Purpose:
Mimics real-world data for a user’s body weight, which is often used in health and fitness analyses.
Provides variability for testing algorithms that may need numerical data.
Example:
67.3, 82.5, 59.1, etc.
4. Dietary Preferences
Each user is randomly assigned a dietary preference from one of the following categories: Vegan, Vegetarian, Non-Vegetarian, Keto, or Paleo.

Purpose:

Adds categorical variety to the dataset by simulating different dietary habits or preferences.
Useful for testing how models handle categorical data and analyzing trends based on preferences.
Categories:

Vegan: Excludes all animal products.
Vegetarian: Excludes meat, but may include dairy and eggs.
Non-Vegetarian: Includes meat and animal products.
Keto: Focuses on a high-fat, low-carb diet.
Paleo: Includes foods that were available during the Paleolithic era, such as meat, fish, fruits, and vegetables.
Example:

Vegan, Keto, Non-Vegetarian, etc.
5. Recommended Calories
A floating-point value is generated to represent the number of daily recommended calories for each user, with a range between 1500 and 3000 calories.

Purpose:
Simulates personalized calorie recommendations for users based on factors such as age, weight, and dietary preferences.
Can be useful in health or nutrition-based applications and models that require numeric data for analysis.
Example:
1892.5, 2450.2, 2756.9, etc.
The script uses np.random.uniform() to generate random calorie values between 1500 and 3000
Additional Customization Features:
The script allows for easy customization to generate different kinds of data:

Number of Records:

You can adjust the number of rows (or records) generated by modifying the num_rows variable at the top of the script. For example, to generate 500 records, change:
num_rows = 500
Change Data Ranges:

If you need a different range of values (e.g., a wider age range or a higher weight range), you can modify the respective functions:
'Age': np.random.randint(min_age, max_age, size=num_rows)
'Weight': np.random.uniform(min_weight, max_weight, size=num_rows)
