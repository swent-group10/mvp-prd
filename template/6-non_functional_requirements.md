# Non-Functional Requirements

## Security, privacy, and data retention policies


As this application collects and stores Personally Identifiable Information (PII) linked to users' Google accounts, such as their email address, full name, and more sensitive data like their location (when they choose to share it in their posts), it is subject to the General Data Protection Regulation (GDPR). This is because the app operates within the European Union (EU) and will be used by EU residents. The mechanisms built and used in the application need to be understood through this article.


### Privacy



#### Firebase Authentification
 
To avoid the hassle of implementing a custom login framework and to comply with EU regulations, the authentication system uses Firebase Authentication with Google accounts, which is GDPR compliant. Due to the usage of this service, passwords, email addresses, phone numbers, user agents, and IP addresses are collected. Information linked to the user's account is deleted when the account is deleted. The IP address is retained for a period of 180 days. To comply with Article 17 of the GDPR ("Right to erasure"), users have the option to delete their accounts, which triggers the automatic deletion of data stored by the Firebase Authentication mechanism.


#### Firebase Databases (database, storage, and geolocation)
The application uses three databases: one for information, one for images, and one for geolocation. All connections to the databases are sent using HTTPS and are isolated from other customers' data. Additionally, all data is encrypted at rest to provide maximum protection. ensuring that data is always processed and retained in secure cloud environments.

#### Data Segregation

Separate tables are maintained for user personal information and application-related data to enhance data segregation and security. The two sets of data are linked using a user ID. This approach ensures that sensitive user data and operational data are compartmentalized, reducing the risk of unauthorized access and simplifying data management. The personnal information will be stored on a server controlled by us and the operational data will be stored on a server controlled by Firebase. Giving us more data segmentation to reduce the risk of exposing sensitive information in case of a data breach.


#### APIs

The first version of the application depended on two APIs for its functionality: Spoonacular for anything related to food recognition and Open Food Facts for information about a product given a barcode. Using the Spoonacular API required sending an image, which was stripped of all its metadata, to their server. To have better control over the granularity of the use of the picture (e.g., the picture sent could be used to fine-tune their model) and to have a better grasp of the retention duration, both APIs are implemented in-house.


#### Data Retention


The application retains user data for as long as the user has an account. When a user deletes their account, all data linked to that account is deleted. The application retains data for a period of 180 days after the account is deleted to comply with the GDPR. During this period, the data is kept in a secure, encrypted state and is only accessible for regulatory compliance purposes. After which the data is permanently deleted from the firebase servers and the sever storing the personal information.

Additionnaly due to the sensitive  nature of the post data (which can inclue the location where the post was made) the post data is only kept for 30 days after the post was made. 

## Data Protection and Information Security Policies

### Appointment of a Data Protection Officer

To ensure compliance with GDPR and to oversee data protection strategies, we will appoint a Data Protection Officer (DPO). The DPO will be responsible for monitoring compliance, managing data protection activities, advising on data protection impact assessments, and acting as a point of contact for data subjects and supervisory authorities. They will be responsibel for creating documentation explaining the reasons for collecting and processing personal information, detailing the types of information held, specifying the retention periods, and describing the technical security measures implemented. Even if this is onyl required by Article 30 of the GDPR for companies o fmore the 250 employees, we believe this demosntrates our commitment to data protection and privacy.

### Analytics Data Stripping

All the data used for analytics will be the data from fireclouds. This ensures that any data collected for analytical purposes cannot be traced back to individual users as no PII is stored. By anonymizing this data, we can analyze usage patterns and improve the application without compromising user privacy.

### Development of a Data Breach Response Plan

We have developed a comprehensive data breach response plan to handle any potential security incidents effectively. This plan includes:
- Immediate containment and assessment of the breach to determine its scope and impact.
- Notification procedures to inform affected users and relevant authorities promptly, as required by GDPR.
- Measures to mitigate the effects of the breach and prevent future occurrences.
- Detailed documentation of the breach and the response actions taken, to improve our security posture and compliance.

By implementing these measures, we aim to maintain the highest level of data protection and ensure that our users' information is handled responsibly and securely.


## Adoptions, Scalability and Availability

### Adoption:

This refers to how your app will attract and retain users. You should outline strategies for user acquisition, onboarding, and retention. You might also discuss how you plan to measure user engagement and satisfaction.

### Scalability:

The most significant bursts of traffic are anticipated during key meal times (breakfast, lunch, and dinner). Additionally, a general increase in traffic is expected around the New Year, as people are more likely to start dieting during this period.

#### Scalability Criteria:

1. **Load Handling Capacity**:
    - The system should be capable of handling a 200% increase in traffic during peak meal times.
    - The application must support at least 10,000 concurrent users without performance degradation.

2. **Performance Metrics**:
    - Response time should not exceed 2 seconds for 95% of requests during peak times.
    - Server CPU usage should remain below 70% during high traffic periods.

3. **Auto-Scaling**:
    - Implement auto-scaling policies to dynamically allocate resources based on real-time traffic.
    - Ensure that auto-scaling triggers when traffic increases by 30% within a 5-minute window.

By adhering to these criteria, the application can effectively manage scalability challenges and ensure a smooth user experience during periods of high traffic.



### Availability:

This refers to your app's uptime. You should discuss how you plan to ensure that your app is always available to users. This might include details about your app's redundancy, backup, and disaster recovery strategies.

all available besides thse

- *What kind of traffic patterns do you expect to see?*