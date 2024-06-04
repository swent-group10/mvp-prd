# Non-Functional Requirements

## Security, privacy, and data retention policies

### General -> small intro

As this application collects and store Personnal Indentifiable Infromation (PII) linked to their Google accound such as their email address and full name and more sensitive such as their location when they choose to share their location in their post, because this app is in the jurritection of the European Union (EU) and will be used by residents of the Europeon Union, the General Data Protection Regulation apllies. The mechanism built and used in the application need tto be understood through this aritcle.


## Privacy



### Firebase Authentification
 
To avoid the hassle of implementating a custom login framework and complying with the EU regulations , the authentification system uses the Firebase Authentification with Google accounts, which is GDPR complient. Due to the usage of this service, the password, email address, phone numbers, User agents, and IP addresses. The information linked to the user's account are delete when the account is deleted. The IP address is retained for a period of 180. To order to comply with Article 17 of the GDPR ("Right to erasure"), the user has the option to delte their accounts which trigers automatic deletion of the data store by the Firebase Authentification mechanism.


### Firebase Databases (database, storage, and geolocation)
The application makes use of 3 database, one for information, one for images and one for geolocation. All connection to the database are sent using HTTPS and isolated for other customers data. In addition all data is encrypted at rest to provide maximal protection. 



Users data is never stored locally on our sever, it is al >>>>>>

seperatate table for both user and user ui


### APIs

The version one of the application was dependent on two APIs for its functionnality, Spoonacular for anything related to food recognition and Open Food Facts for infomartion about a productin given a barcode. Using the Spoonacular API required sending a image, which was stiped of all its metadata, to their server. In order to have better control of the granulatiy of the use of the picture (for example, the picture sent could be used to fine tune their model) and to have a better grapse of the rettention durration, both APIs are implemented inhouse.


### Data Retention

privacy policy

record of preocessing activity

strip al of analatics


- *What are your internal policies?*

● Data controller determines the purpose and means of personal data -> highest level of security possible

Appoint a Data Protection officier

information security principe

only keep current user position locally the device

define dtat reteention

develop a data brea response

- *Which privacy features do you need from the phone?*
- Camera access
- Location access

## Adoptions, Scalability and Availability

### Adoption:

This refers to how your app will attract and retain users. You should outline strategies for user acquisition, onboarding, and retention. You might also discuss how you plan to measure user engagement and satisfaction.

### Scalability:

This refers to your app's ability to handle growth. You should discuss how your app will perform as the number of users increases. This might include details about your app's architecture, infrastructure, and any strategies you have for managing increased demand.

- 
- *Are there known periods of bursty traffic that the MVP must be designed to support?*
- We can expect to see bursts of traffic during key meal times (breakfast, lunch, dinner).

### Availability:

This refers to your app's uptime. You should discuss how you plan to ensure that your app is always available to users. This might include details about your app's redundancy, backup, and disaster recovery strategies.

all available besides thse

- *What kind of traffic patterns do you expect to see?*