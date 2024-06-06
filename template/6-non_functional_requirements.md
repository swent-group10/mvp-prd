# Non-Functional Requirements

## Security, Privacy, and Data Retention Policies

As this application collects and stores Personally Identifiable Information (PII) linked to users' Google accounts, including their email address, full name, and more sensitive data such as their location (should the user opt to include it in their posts), it is subject to the General Data Protection Regulation (GDPR). This is due to the app being designed for operation within the European Union (EU) and its usage by EU residents. The mechanisms built and used in the application must be understood through the lenses of this regulation.

### Privacy

#### Firebase Authentication

To streamline the login process and ensure compliance with EU regulations, the authentication system employs Firebase Authentication with Google accounts. As a consequence of this service being used, passwords, email addresses, phone numbers, user agents, and IP addresses are collected and stored on the Firebase Cloud. Information linked to the user's account is deleted when the account is deleted, while the IP address is retained for 180 days. To be in accordance with Article 17 of the GDPR ("Right to erasure"), users can delete their accounts within the application, initiating the automatic deletion of data stored by the Firebase Authentication mechanism.

#### Firebase Databases (Database, Storage, and Geolocation)

The application employs three databases: one for information, one for images, and one for geolocation. All database connections are transmitted via HTTPS, ensuring they remain isolated from other customers' data. Furthermore, all data is encrypted at rest, guaranteeing it is always processed and stored in secure cloud environments.

#### Data Segregation

Separate tables are maintained for personal user information and application-related data to improve data separation and security. The two sets of data are linked by a randomly generated user ID. This approach ensures that sensitive user data and operational data are separated, reducing the risk of unauthorized access and simplifying data management. Personal information is stored on a server controlled by us, while operational data is stored on a server controlled by Firebase. This segmentation reduces the risk of exposing sensitive information in a data breach.

#### APIs

The PoC relied on two APIs for its functionality: Spoonacular for food recognition and Open Food Facts for barcode-related product information. Using the Spoonacular API required sending an image stripped of all metadata to their server, which could later be used to fine-tune their model. To better control image use and retention time, both APIs have been implemented in-house. This change enhances security and allows for customization tailored to the application's specific needs.

#### Data Retention

Data is retained for as long as the user has an account. When a user deletes their account, all data associated with that account is deleted. To comply with GDPR, the application retains data for 180 days after the account is deleted. During this period, the data is stored in a secure, encrypted state and is only accessible for compliance purposes. After this period, the data is permanently deleted from the Firebase servers and the server that stores the personal data.

Additionally, due to the sensitive nature of posts from the social media feature (which may include the location where the post was made), the information is only retained for 30 days after the post is made.

## Data Protection and Information Security Policies

### Appointment of a Data Protection Officer

To ensure compliance with the GDPR and oversee our data protection strategy, we will appoint a Data Protection Officer (DPO). The DPO will be responsible for monitoring compliance, managing data protection activities, advising on data protection impact assessments, and acting as a point of contact for data subjects and supervisory authorities. The DPO will be responsible for creating documentation that explains the reasons for collecting and processing personal information, details the types of information held, specifies retention periods, and describes the technical security measures implemented. While this is only required by Article 30 of the GDPR for companies with more than 250 employees, we believe it demonstrates our commitment to data protection and privacy.

### Analytics Data Stripping

All data used for analytics is stored in the Firecloud. This ensures that data collected for analytics purposes cannot be traced back to individual user as no PII is stored. By anonymizing this data, we can analyze usage patterns and improve the application without compromising user privacy.

### Development of a Data Breach Response Plan

We have developed a comprehensive data breach response plan to effectively manage any potential security incident. This plan includes:

- Immediate containment and assessment of the breach to determine its scope and impact.
- Notification procedures to promptly notify affected users and relevant authorities, as required by GDPR.
- Measures to mitigate the impact of the breach and prevent future occurrences.
- Detailed documentation of the breach and response actions taken to improve our security posture and compliance.

By implementing these measures, we aim to maintain the highest level of data protection and ensure that our users' information is handled responsibly and securely.

## Adoptions, Scalability, and Availability

### Adoption

#### User Acquisition Strategy

- **Freemium Model**: Implement a freemium model to attract a broad user base, allowing them to try basic features for free while offering premium features for a subscription fee. This approach lowers the barrier to entry and encourages users to upgrade for additional benefits. The model is structured as follows:
  - **Basic Plan**: Free access to basic features such as meal tracking, recipe search, and community contributions.
  - **Premium Plan**: Paid subscription offering advanced features such as meal recognition from a picture, personalized meal recommendations, and exclusive content.

- **Marketing Strategies**: Multi-frontal marketing strategies will be used to attract users to the application. These include social media campaigns, influencer partnerships, email marketing, and search engine optimization (SEO) to increase app visibility and user engagement.

#### User Onboarding

- Provide a seamless onboarding experience with step-by-step tutorials to familiarize users with the app's features. This includes walkthroughs, video tutorials, and a FAQ section.

#### User Retention

- **Push Notifications**: Implement personalized push notifications to remind users to log their meals, encourage them with their chosen goals (daily intakes), and notify them of new features or updates.
- **Personalized Recommendations**: Leverage machine learning algorithms to provide personalized meal recommendations based on users' dietary preferences, health goals, and past meal history.
- **New Features**: Regularly introduce new features and updates to keep users engaged and encourage them to continue exploring the app.

### Scalability Criteria

1. **Load Handling Capacity**:
   - The system should be able to handle a 200% increase in traffic during peak meal times.
   - The application must support at least 15,000 concurrent users without performance degradation.

2. **Performance Metrics**:
   - Response time should not exceed 2 seconds for 95% of requests during peak hours.
   - Server CPU utilization should remain below 70% during peak traffic periods.

3. **Auto Scaling**:
   - Implement auto-scaling policies to dynamically allocate resources based on real-time traffic.
   - Ensure that auto-scaling is triggered when traffic increases by 30% within a 5-minute window.

### Availability

#### System Resilience

1. **Redundancy and Backups**:
   - Implement redundant server architectures to eliminate single points of failure.
   - Perform hourly incremental backups and daily full backups of all critical data.

2. **Geographical Distribution**:
   - Utilize multiple data centers in different geographical locations to ensure service continuity in case of localized disruptions.
   - Implement automated failover mechanisms to switch to backup data centers in case of primary data center failure.
   - Regularly test and validate the failover processes to ensure seamless transition during actual incidents.

#### Data Protection

1. **Regular Backups**:
   - Schedule daily backups of all vital data with retention periods aligned with business continuity requirements.
   - Store backups in multiple secure locations, including off-site storage facilities.
   - Implement encryption for both in-transit and at-rest backup data to prevent unauthorized access.

2. **Encryption and Security**:
   - Use advanced encryption standards (AES-256) for data at rest.
   - Regularly update encryption keys and rotate them according to industry best practices.

#### Recovery Strategy

1. **Disaster Recovery Plan**:
   - Develop a detailed disaster recovery plan outlining steps for service restoration, including system reconfiguration and data recovery procedures.
   - Ensure the disaster recovery plan includes roles and responsibilities, communication protocols, and escalation procedures.

2. **Routine Testing**:
   - Conduct bi-annual disaster recovery drills to simulate various failure scenarios and test the effectiveness of the recovery plan.
   - Review and update the disaster recovery plan based on drill outcomes and changes in the infrastructure.
