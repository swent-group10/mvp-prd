# Design and Implementation

## Frontend

To build our frontend, we used Kotlin and leveraged Android Jetpack Compose for UI development. We also used Material3 for design components.

Within our app, we have the following essential screens:

1. Login Screen: Users can log in to their account.
2. Home Screen: Users can view their daily calorie intake and track their meals.
3. Meal Creation Screens: Users can create a meal by taking a picture or manually inputting the meal.
4. Post Creation Screen: Users can share their meals with friends.
5. Recap Screen: Users can view a recap of their daily calorie intake.
6. Graph Screen: Users can view a graph of their calorie consumption over time.
7. Map Screen: Users can view nearby friends and their meals.
8. Recipe Suggestions Screen: Users can view recipe suggestions based on selected ingredients.

## Backend

<!-- *Decompose the MVP into functional blocks.* -->

1. Authentication
    - Firebase Auth: Manage user authentication, including sign-up, login, and password management.
2. Remote Database Management
    - Firestore: Store user data, meal entries, and posts.
3. Dependency Injection
    - Hilt: Manage dependencies and provide objects to classes.
4. Local Database Management
    - Room: Cache data locally for offline access.
5. Image Recognition
    - Spoonacular API: Recognize ingredients in images and provide nutritional information.
    - For the MVP, plan to move to an in-house solution for higher accuracy.

- Hilt, Room, Dagger, JaCoCo, SonarQube, JUnit, Mockito, Espresso, Firestore, Firebase Auth

## Data Model

<!-- *What data are you collecting / managing?* -->

- User Data:
    - Display/First/Last Name
    - DOB
    - Email
    - Preferences & Info
        - Dietary Restrictions
        - Calorie Goals
        - Weight
        - Height
- Meal Data:
    - Name
    - Occasion (Breakfast, Lunch, Dinner, Snack)
    - Tags (Vegan, Vegetarian, etc.)
    - Ingredients
        - Nutritional Information
- Post Data:
    - Meal to be shared
    - Location
    - Description
    - Pictures
    - User who posted


### How it is stored

All data is stored in a NoSQL database. We have a collection for users, which contains their meals.

For posts, we have a second collection that contains all post data.

### Where is it stored

Our app data is stored in Firebase Firestore. For static data, we use Firebase Storage.

### How is it accessed

Data is shared between the frontend and backend using Firebase's `FirebaseFirestore` class. Data is cached locally using Room, a SQL database for offline access.

<!-- *How is the application developed, tested and deployed?* -->

## Testing

We use JUnit and Mockito for unit testing and Espresso for UI testing. We also use JaCoCo for code coverage and SonarQube for static code analysis.

## Deployment

Our app will be deployed through the Google Play Store. Our backend is hosted on Firebase already. We have no special infrastructure requirements. One step we will need before the MVP is a separate development and production environment.