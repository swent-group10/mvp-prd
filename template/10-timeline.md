# Timeline/Resource Planning

## Execution Roadmap

We plan to execute the MVP deployment over a period of 14 weeks. This execution will include the setup, development, testing, rollout, integration of added components to the app as well as a refactoring of the current project. We will be setting up multiple intermediate milestones to get an assesment of the current progress and be able to identify and solve potential problems that will rise up.

### Milestone 1 : Documentation & Refining

- Write Documentation on all current features of the app.
- Redesign UI to adapt UX concepts to make the app more user oriented
- Adapt the code to the newly defined figma screens and wireframes
- Implement our own graphs rather than using open source library (This would allow us to have more control over the graphs and woud lighten the memory load on the app)

|Sprint/Week number | Objective  | Outcomes    |
| :---------------: | :--------: | :---------: |
|Week 1 | Documentation | Adding intermediate Readme Files and commenting code|
|Week 2 | Redesign | Streamline the UI and configure reusable components as well as implementing UX concepts for better usability|
|Week 3 | Refactoring Code| Update the code to adapt to the new Figma mockups and integrate it|
|Week 4 | Graph Design | Fully designed graphs depending on the needs of the app that would be lighter and wouldn't interfere with UI testing |

### Milestone 2 : API Creation
Swapping the Spoonacular API with our own food recognition AI model.

- Setting up the foundation of the AI
- Gathering a quality data training set
- Preprocessing the data
- Choosing a model and training it
- Evaluating the model
- Deploy the AI to our personnal cloud, used for the application

|Sprint/Week number | Objective  | Outcomes    |
| :---------------: | :--------: | :---------: |
|Week 1 | Setup and Data Gathering | Acquring a large set of qualitative data for training purposes|
|Week 2 | Preprocessing the Data | Cropping and modifying the data to have the optimal format before usage|
|Week 3 | Choosing and Training model| Selecting a model (e.g DnCNN) and training it, fine tuning the hyperparameters as we go|
|Week 4 | Evaluating and Deploying the Model | Split data into test and validation and measure performance, then deploy the model to the used cloud service |


This step would be conducted by hiring a team of highly efficient ML and computer vision engineers along with one or more data scientists. This would allow to have a food recognition AI model tailored to the needs of our app.

### Milestone 3 : Setting up Barcode Database

- Gathering data about barcodes used on different food items around the world
- Setting up a cloud database with all the needed information about each products
- Integrating the database into our project to replace the use of the OpenFoodFacts API

| Sprint/Week number | Objective  | Outcomes     |
| :----------------: | :--------: | :----------: |
|Week 1| Gathering Data| Scouring databases to gather as much data about barcodes linked to food items and selecting target information about those food items|
|Week 2| Setting Up Database | Using the gathered data, create a database in the used cloud service that will hold the barcode and information about the specific food item|
|Week 3| Integration | Integrate the use of the database to replace the OpenFoodFacts API|

### Milestone 4 : Deployment

- Release version of the app for alpha testers

| Sprint/Week number | Objective  | Outcomes     |
| :----------------: | :--------: | :----------: |
|Week 1| Alpha testing | Deployment of first version of the app to alpha testers and gathering analytics about the app's performances|
|week 2| Hotfixes and Beta Testing | Identifying issues based on alpha users feedback and fixing them, deploying the app for beta testing and gathering users and feedback from it|
|Week 3| Last fixes and final rollout | Fixing last issues based on analytics and feedback and initiating final rollout along with advertisement to get more users on the app| 







