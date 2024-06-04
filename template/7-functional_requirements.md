# Functional Requirements

## Key Features of the MVP

### 1. Registration

**Motivation**
To provide a seamless and secure user experience, the app must support user registration and login via a reliable and widely-used authentication method. Using Google account authentication simplifies the process for users and leverages existing security protocols.

**Proposed Solution**
- Implement Google Sign-In for Android to allow users to authenticate using their Google account.
- Ensure that the authentication process is secure and user data is protected.
- Leverage Firebase Authentication to manage user sessions and simplify integration.

### 2. Core Functionality

#### Scan with Camera

**Motivation**
The ability to scan food items using the camera is essential for determining the composition of the food, which is the primary function of the app. This feature allows users to quickly and easily get nutritional information without manually entering data.

**Proposed Solution**
- Integrate a barcode and image recognition API (such as Spoonacular and OpenFoodFacts) to enable the camera to scan and identify food items.
- Use the MealViewModel to handle the initialization and updates of meal data from camera scans.
- Store the results in the LocalDB and sync with Firebase.

#### Register Consumption

**Motivation**
Logging food intake is crucial for users to track their diet and nutrition over time. Providing an easy way to register meals and snacks ensures users can maintain accurate records.

**Proposed Solution**
- Develop a user-friendly interface for logging food intake, categorized by meal type (breakfast, lunch, dinner, snack).
- Utilize the MealViewModel to initialize default values or use picture results.
- Store the logged data locally and sync it with Firebase for access across devices.

#### Track Consumption and Goals

**Motivation**
Users need to visualize their consumption patterns and progress towards their nutritional goals. Graphs and charts provide an intuitive way to track and analyze dietary habits.

**Proposed Solution**
- Implement a dashboard that displays user data through various graphs and charts.
- Use the GraphViewModel to get data from the MealRepository and format it for display.
- Ensure the data is updated in real-time as users log their intake.

#### Scan Product Barcodes

**Motivation**
Allowing users to scan barcodes of final products provides a quick and efficient way to get detailed nutritional information, saving time and effort.

**Proposed Solution**
- Use a barcode scanning API to read product barcodes.
- Connect to external APIs like OpenFoodFacts for barcode information retrieval.
- Use the BarcodeViewModel to handle barcode scans and display nutritional information.

#### Recipe Suggestions

**Motivation**
Based on the user’s scanned items and dietary preferences, suggesting recipes helps users make better food choices and utilize available ingredients effectively.

**Proposed Solution**
- Develop an algorithm to match scanned items with potential recipes using the Spoonacular API.
- Integrate a recipe database for filtering based on user preferences and available ingredients.
- Provide step-by-step instructions and nutritional information for suggested recipes.

#### Nutritional Analysis

**Motivation**
Providing detailed nutritional information for scanned items is essential for users to understand their dietary intake and make informed choices.

**Proposed Solution**
- Retrieve and display macronutrient and micronutrient information using the Spoonacular Nutrition Analysis API.
- Allow users to view detailed breakdowns of their daily, weekly, and monthly intake.
- Use a standardized nutritional database to ensure accuracy and consistency.

#### Create and Share Posts (Optional)

**Motivation**
Creating and sharing posts allows users to interact with the community, share experiences, and gain insights from others. This feature can enhance user engagement.

**Proposed Solution**
- Develop a social feature that allows users to create posts with text, images, and location tags using the CreatePostViewModel.
- Implement privacy controls to let users manage who can see their posts.
- Use Firebase for post storage and retrieval, handled by the PostRepository.

#### View Posts within a Radius (Optional)

**Motivation**
Viewing posts within a specific radius helps users connect with others nearby, fostering a sense of community and local support.

**Proposed Solution**
- Implement location-based filtering to show posts from users within a specified radius using the MapViewModel.
- Use geolocation services to determine user locations and calculate distances.
- Ensure user privacy by allowing location sharing only with explicit consent.

### 3. User Interface

**Motivation**
A consistent and intuitive user interface ensures a positive user experience and easy navigation throughout the app.

**Proposed Solution**
- Utilize Material Design 3 (M3) elements to create a cohesive and modern UI.
- Conduct user testing to refine the interface and improve usability.
- Ensure accessibility standards are met to make the app usable for everyone.

### 4. Data Storage

**Motivation**
Storing user data locally ensures quick access and offline functionality, while syncing with Firebase Firestore provides data backup and multi-device access.

**Proposed Solution**
- Implement local storage using Room for offline access.
- Use Firebase Firestore for cloud synchronization and backup.
- Ensure data consistency and handle conflict resolution during sync.

### 5. Multi-Device Sync

**Motivation**
Allowing users to access their data across multiple devices enhances convenience and ensures a seamless experience.

**Proposed Solution**
- Utilize Firebase Authentication to manage user sessions across devices.
- Implement real-time data sync using Firebase Firestore to keep data consistent.
- Ensure that the user experience is seamless when switching between devices, meaning the user should be able to start a session on one device and continue on another without losing data or functionality.

## Architectural Diagram

![Architecture Diagram](Architecture.png)



*Describe key internal functionality.*

