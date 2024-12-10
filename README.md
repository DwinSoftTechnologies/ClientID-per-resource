# ClientID-per-resource

This repository includes the configuration and necessary setup for a custom connector to integrate with ClientID-per-resource. The project has been upgraded to Java 17, leveraging modern language features, improved performance, and enhanced security.

# Why Upgrade to Java 17?
Long-Term Support (LTS): Java 17 is the latest LTS version, ensuring updates and security patches for the foreseeable future.
Enhanced Performance: Significant improvements in JVM performance for better application efficiency.
Modern Features: Access to new language features such as sealed classes, records, and pattern matching.
Security Improvements: Java 17 includes fixes and enhancements that ensure robust protection against vulnerabilities.
By upgrading, this project stays future-proof and aligns with the latest industry standards.

# How to Use the Configuration
1.Client ID Extraction: 
   To extract the Client ID from incoming API requests, use the following Mule Expression:( attributes.headers['client_id'] ).This expression retrieves the value of the client_id header from the API request attributes.
   
2.Allowed Client IDs: 
   Specify a comma-separated list of Client IDs that are permitted to access the API. For example: (client_id_1,client_id_2,client_id_3).These Client IDs should correspond to the values provided by consumers of your API.

Advanced Options
1. Policy Version:
     The configuration uses Policy version 1.0.1-SNAPSHOT (latest). Ensure you are working with the latest version to utilize the newest features and fixes.

2. Methods and Resource Conditions:
     You can apply the policy to all API methods and resources or limit it to specific ones:
   Apply to All Methods & Resources:
     The policy will be enforced globally across all endpoints of the API.
   Apply to Specific Methods & Resources:
     Restrict the policy to particular HTTP methods (e.g., GET, POST) and resources (e.g., /users, /orders). Specify the conditions in your Mule configuration file.



