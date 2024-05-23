# Design and Implementation

## Frontend

*List the key libraries, languages, components used by the MVP.*

Languages: Kotlin, Android Jetpack Compose, Material3

*If applicable, describe essential screens.*

Login Screen: Users can log in to their account.
Home Screen: Users can view their daily calorie intake and track their meals.
Meal Creation Screens: Users can create a meal by taking a picture or manually inputting the meal.
Post Creation Screen: Users can share their meals with friends.
Recap Screen: Users can view a recap of their daily calorie intake.
Graph Screen: Users can view a graph of their calorie consumption over time.
Map Screen: Users can view nearby friends and their meals.

## Backend

*Decompose the MVP into functional blocks.*

- Hilt, Room, Dagger, JaCoCo, SonarQube, JUnit, Mockito, Espresso, Firestore, Firebase Auth



## Data Model

*What data are you collecting / managing?*

- User Data: User information, preferences, and settings.
- Meal Data: Meal information, ingredients, and calorie content.
- Post Data: Shared posts, their content, and associated meals.

*How is it organised?*

All data is stored in a NoSQL database, with separate collections for users (and their meals) and for posts.

*Where is it stored?*

Firebase Firestore

*How is it shared/copied/cached?*

Data is shared between the frontend and backend using Firebase's `FirebaseFirestore` class. Data is cached locally using Room, in a SQL database for offline access.

## Security Considerations

## Infrastructure and Deployment

*How is the application developed, tested and deployed?*

The application is developed using Android Studio and tested using JUnit, Mockito, and Espresso. The application is not yet deployed.

*Any special infrastructure requirements.*

No

## Test Plan

*How is the application developed, tested and deployed?*

*Any special infrastructure requirements.*

