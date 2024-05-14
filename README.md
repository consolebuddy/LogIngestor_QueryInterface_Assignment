Introduction
This React application provides a user-friendly interface for querying and displaying log data. It enables users to filter and search log entries based on various criteria, presenting the results in a clear and organized manner.

Project Structure Overview
The project structure for the React Log Query Application is organized into two main folders: LogIngestor and QueryInterface. This structure separates the application's server-side code and client-side interface, promoting modularity and maintainability.

LogIngestor Folder
The LogIngestor folder houses the server-side code responsible for handling log data ingestion and processing. This folder contains the following components:

Server Code: The server code is responsible for receiving log data from various sources, such as files, APIs, or network streams. It also processes the log data, extracting relevant information and preparing it for storage and retrieval.

Database Integration: The server code integrates with the MongoDB database to store and manage log entries. It establishes a connection to the database, performs data operations such as insertion, updating, and querying, and ensures data integrity and security.

Data Processing and Transformation: The server code performs data processing tasks to transform the incoming log data into a standardized format suitable for storage and analysis. This may involve cleaning, filtering, and normalizing the data to enhance its usability.

QueryInterface Folder
The QueryInterface folder contains the client-side code responsible for building and rendering the user interface (UI). This folder includes the following components:

• React Components: The React components are the building blocks of the UI, defining the visual elements and their interactions. They provide a declarative way to represent the UI and handle user input.

Benefits of Separating Server and Client Code
Separating the server-side code into the LogIngestor folder and the client-side code into the QueryInterface folder offers several advantages:

Modularity: Each folder focuses on a specific aspect of the application, promoting modularity and making the code easier to understand and maintain.

Scalability: The separation allows for independent scaling of the server and client components, enabling the application to handle increasing data volumes and user requests.

Testability: The separation facilitates unit testing of individual components, ensuring the correct functioning of both the server-side data processing and the client-side UI.

Deployment: Independent deployment of server and client components can be beneficial for production environments, allowing for updates and maintenance without affecting the entire application.

Running the Application
Prerequisites:
• Node.js and npm installed on your system

• MongoDB database

• Postman

Instructions:
Clone the project repository: https://github.com/itssouray/Log-Ingestor-and-Query-Interface

Navigate to the project directory

Install dependencies on both folders

Start the server side script:

i. cd LogIngestor/log_ingestor.js

ⅰⅰ. nodemon log_ingestor

Start the client side script:

ⅰ. cd QueryInterface

ⅰⅰ. npm start

System Design
The application utilizes a client-server architecture, with the React UI component running on the client-side and a backend server responsible for fetching and processing log data. The components communicate through RESTful API calls.

Features

Log Query Form: Users can enter search terms and select filters to refine the log entries they wish to view.

Log Entry List: The application displays a filtered list of log entries, each including the timestamp, log level, message, and metadata.

Log Entry Details: Clicking a log entry expands its details, providing access to the timestamp, log level, message, metadata, and stack trace (if available).

Log Entry Selection: Users can select individual log entries to highlight them and easily identify them in the list.

Responsive Design: The application adapts its layout to different screen sizes, ensuring a consistent user experience across various devices.

Data Source
The application retrieves and displays log data from a MongoDB database. The data can be imported into the database using various methods, including manual data entry, automated scripts, or third-party data sources.

Identified Issues for Improvement
Limited Search Capabilities: The current search functionality supports basic text matching. Implementing advanced search options, such as regular expressions and proximity searches, would enhance the search experience.

Real-time Updates: The application currently relies on periodic updates to fetch new log entries. Integrating real-time updates using WebSockets or similar technologies could provide a more dynamic experience.

Error Handling and Logging: Incorporating comprehensive error handling and logging mechanisms would improve the application's stability and provide valuable insights for debugging and performance optimization.

Testing Coverage: Implementing a comprehensive test suite, including unit tests, integration tests, and end-to-end tests, would enhance the application's reliability and ensure the integrity of its features.
