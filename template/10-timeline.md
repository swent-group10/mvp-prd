# Timeline/Resource Planning

## Execution Roadmap

We plan to implement the MVP deployment over a period of 18 weeks. This process will include the setup, development, testing, rollout, integration of added components to the app, and refactoring of the current project. We will be setting up multiple intermediate milestones to get an assessment of the current progress and be able to identify and solve potential issues that arise.



### Milestone 1: Documentation and Refining

- Write documentation on all current features of the app.
- Redesign the UI to adapt UX concepts to make the app more user-oriented.
- Adapt the code to the newly defined Figma screens and wireframes.
- Implement our own graph library rather than using an open-source library. This would allow us to have more control over the graphs and would lighten the memory load on the app.

|Sprint/Week number | Objective  | Outcomes    |
| :---------------: | :--------: | :---------: |
|Week 1 | Documentation | Adding intermediate Readme Files and commenting code|
|Week 2 | Redesign | Streamline the UI and configure reusable components as well as implementing UX concepts for better usability|
|Week 3 | Refactoring Code| Update the code to adapt to the new Figma mockups and integrate it|
|Week 4 | Graph Design | Fully designed graphs depending on the needs of the app that would be lighter and wouldn't interfere with UI testing |

### Milestone 2: API Creation
Transitioning from Spoonacular API to our own food recognition AI model.

- Setting up the foundation of the AI
- Gathering a quality data training set
- Preprocessing the data
- Choosing a model and training it
- Evaluating the model
- Deploy the AI to our personal cloud, used for the application.

|Sprint/Week number | Objective  | Outcomes    |
| :---------------: | :--------: | :---------------: |
| Week 1             | Setup and Data Gathering      | Acquiring a large set of qualitative data for training purposes                       |
| Week 2             | Preprocessing the Data        | Cropping and modifying the data to have the optimal format before usage               |
| Week 3             | Choosing and Training Model   | Selecting a model (e.g., DnCNN) and training it, fine-tuning the hyperparameters as we go |
| Week 4             | Evaluating and Deploying Model | Splitting data into test and validation sets, measuring performance, then deploying the model to the chosen cloud service |



This step would be conducted by hiring a team of highly efficient ML and computer vision engineers along with one or more data scientists. This would allow to have a food recognition AI model tailored to the needs of our app.

### Milestone 3: Setting up Barcode Database
Transitioning from the OpenFoodFacts API to our own.

- Gathering data about barcodes used on different food items around the world
- Setting up a cloud database with all the needed information about each product
- Integrating the database into our project to replace the use of the OpenFoodFacts API


|Sprint/Week number | Objective  | Outcomes    |
| :---------------: | :--------: | :---------: |
|Week 1| Gathering Data| Scouring databases to gather as much data about barcodes linked to food items and selecting target information about those food items|
|Week 2| Setting Up Database | Using the gathered data, create a database in the used cloud service that will hold the barcode and information about the specific food item|
|Week 3| Integration | Integrate the use of the database to replace the OpenFoodFacts API|

### Milestone 4: Health App Integration

- Implement seamless integration with popular health apps to sync user data.
- Allow users to view their health data within the app.
- Provide personalized insights and recommendations based on the aggregated health data.

|Sprint/Week number | Objective  | Outcomes    |
| :---------------: | :--------: | :---------: |
|Week 1 | Research and Planning | Identify popular health apps for integration and outline integration requirements |
|Week 2 | Initial Development | Begin development of integration features, focusing on data syncing |
|Week 3 | Continue Development | Extend integration to include viewing health data within the app |
|Week 4 | Testing and Feedback | Conduct testing to ensure seamless integration and gather user feedback |
### Milestone 5 : Deployment
Release version of the app for alpha testers

|Sprint/Week number | Objective  | Outcomes    |
| :---------------: | :--------: | :---------: |
|Week 1| Alpha testing | Deployment of first version of the app to alpha testers and gathering analytics about the app's performances|
|Week 2| Hotfixes and Beta Testing | Identifying issues based on alpha users feedback and fixing them, deploying the app for beta testing and gathering users and feedback from it|
|Week 3| Last fixes and final rollout | Fixing last issues based on analytics and feedback and initiating final rollout along with advertisement to get more users on the app| 

## Development Resources

In our predictions the, primary cost of development for our product will be the developer cost which concerns essentially the team hired to handle the different tasks that pertain to the development of our application. Ideally, on top of a constant team of developers at hand, we would hire part-time team members to handle the UX/UI design and the software testing.

<div align = "center">

|Role           | Number of persons |
| :-----------: | :---------------: | 
| Frontend Developer | 3 | 
| Backend developer | 4 |
| UX/UI Designers (part-time) | 2 | 
| Software Testers (part-time) | 2 | 
| ML engineer | 1 | 
| Computer Vision Developer | 1 |
| Data Scientist | 2 |
| Data Protection Officer | 1 |
</div>

## Deployment Resources

For safe storage we will need capital to acquire a NAS to use as our main physical storage server, and we will also subscribe to a cold storage service (e.g Amazon Glacier S3) for redundancy to store a copy of our server that could be access if a problem arises with the NAS. The amount of cold storage used will be at least 10 TB.

<div align="center">

| Item | Cost/Unit | Units | Total |
| :--: | :-------: | :---: | :---: |
| NAS | 200-600 CHF | 1 | 200 - 600 CHF |
| FireBase | Free Tier | - | 0 |
| Google Analytics | Free Tier | - | 0 | 
| Amazon Glacier S3 | 3500 CHF + 40CHF/Month | 1 | 3500CHF + 40CHF/Month |
| **TOTAL** | - | - | 3700-4100CHF + 40CHF/Month | 

</div>

## Maintenance and Upkeep

We will need to constantly monitor our AI Model to analyze its performance but also take advantage of tha data from the users to be able to improve our model. We will also need to periodically update the Database created for storing Barcodes and information about food products to expand it and keep it up-to-date. 






