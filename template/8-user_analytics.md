# User Analytics and Acceptance

To understand how users are using the app, we will track the following metrics:
- Monthly active users
    - Users that log in to the app
- Monthly new users
    - Users that sign up for the app
- Weekly meals created
    - Number of meals created by users
- Weekly posts shared
    - Number of posts shared by users
- Retention Time
    - How long active users continue to use the app
- Premium Subscription Rate
    - Percentage of users that opt for the premium subscription

We will use a third-party analytics tool, such as Firebase Analytics or Metabase, to track these metrics. Monitoring these metrics will help us understand how users are using the app and what features they are engaging with the most. These analytics also can help identify service outages, bottlenecks, and other issues that may cause a sudden drop in user engagement.

## Analytics Dashboard
In order to track these metrics, we will create an analytics dashboard that will display charts based on the key metrics mentioned above. The dashboard will be updated in real-time and will be accessible to the team to monitor the app's performance. In order to get data into the analytics dashboard, we will add event emitters to the app code that will send data to the analytics tool.

## A/B Testing
We will also conduct A/B testing to test different features and UI/UX changes to see how they impact user engagement and retention.

- Premium price points
    - Test take rates at different price points
    - Test take rates with different discount offers
    - Test take rates with different premium feature bundles

- UI/UX changes
    - Test different home screen layouts
    - Test different recipe card designs

- Image Recognition Models
    - Test different image recognition models, see which one performs better in terms of user satisfaction and accuracy

- Painted Door Tests
    - Test user interest in a feature by showing a "coming soon" button and tracking how many users click on it
