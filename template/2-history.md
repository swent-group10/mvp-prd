# History

<!-- *Maximum 1 page* -->

<!-- *Describe the V1 POC as planned by Sprint 10.* -->
## V1 Proof of Concept

The V1 Proof of Concept (PoC) for Polyfit, as planned by Sprint 10, focused on creating a basic yet functional calorie tracking app utilizing the phone camera for image recognition. The core functionalities included:

- Calorie Tracking: Users can take a picture of their food to create a meal with an estimation of calorie content, with detailed nutritional breakdowns.
- Manual Meal Creation: A process to create and log new meals without using image recognition.
- Manual Adjustments: Users have the ability to edit their meals after and during creation.
- Daily Recaps: The app allows users to log their meals and track their daily calorie intake through daily recaps.
- Graphical Overview: Users can view a graph of their calorie consumption over time.
- Social Features: Basic social media-like features were incorporated, enabling users to share their meals and progress with nearby friends based on GPS location.
- Offline Mode: The app is designed to work offline, with the ability to sync data when the user is back online.
- Barcode Scanning: A feature to scan barcodes for automatic meal creation and calorie tracking.
- Recipe Recommendation: A feature that suggests recipes based on input ingredients.

<!-- *What did you learn?* -->
## Key Insights

From the development and deployment of the V1 PoC, several key insights were gained:

- Image Analysis Challenges: Using image recognition to detect quantities and weights of food items was more complex than anticipated, requiring further refinement. Additionally, the classification of food items by the model used was restricted to a limited set of predefined categories, which limited the app's usefulness to the user.
- Intentionality of code: The importance of writing clean, well-documented code was highlighted to ensure scalability and maintainability.
- Usability: The importance of a user-friendly interface and smooth navigation was underscored by testing/grading feedback.

<!-- *What is missing to bridge from PoC to MVP?* -->
## Bridging to MVP

To bridge from the PoC to the Minimum Viable Product (MVP), some key features and improvements are necessary:

- Improved Image Recognition: Enhance the accuracy, speed and range of image recognition for better meal tracking.
- Improved Data Structuring: Optimize data structure to reduce bloating, especially targeting ingredient data.
- Increased Nutrient Tracking Capabilities: Currently, non-image created ingredients are limited to weights, calories, and macros. We need to expand this to include more detailed nutritional information.
- Health App Integration: Integrate with health apps to monitor user weight and display progress.
- Saving Ingredients And Recipes: Allow users to save ingredients and recipes for future use.