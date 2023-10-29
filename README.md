# Business Management Web Application

## Project Description
The **Business Management Web Application** is a comprehensive tool designed to streamline various operational aspects for businesses. It offers a user-friendly interface to efficiently manage **customer data, inventory, and orders**, among other crucial business functions.

---

## Features

* **Customer Management**: Easily add, update, and delete customer information.
* **Inventory Management**: Keep precise track of inventory items, including stock levels and pricing.
* **Order Management**: Efficiently manage customer orders, from creation to processing.
* **User Authentication**: Provides secure login and authentication mechanisms for both administrators and staff members.
* **Role-Based Access Control**: Define and assign specific roles and permissions to different user types, ensuring controlled access.
* **Thymeleaf Templates**: Utilizes the Thymeleaf server-side Java template engine for dynamic and responsive HTML generation.
* **Database Integration**: Seamlessly integrated with MySQL for robust data storage and retrieval.

---

## Technologies Used

* **Spring Boot**: The core backend framework for building scalable Java-based web applications.
* **Thymeleaf**: A powerful server-side Java template engine for dynamic HTML rendering.
* **MySQL**: A reliable relational database management system for persistent data storage.
* **IDE/Tool**: Developed using **Spring Tool Suite 4 (Eclipse)**.

---

## Installation

Follow these steps to set up and run the Business Management Web Application:

1.  **Clone the Repository**:
    ```bash
    git clone [https://github.com/dev-amul/Business_Management_Project.git](https://github.com/dev-amul/Business_Management_Project.git)
    ```

2.  **Import the Project into STS/Eclipse**:
    * Open STS/Eclipse.
    * Navigate to `File` > `Import` > `Maven` > `Existing Maven Projects`.
    * Click `Browse`, select the `Business_Management_Project` directory, and then click `Finish`.

3.  **Navigate to Project Directory**:
    * Ensure your command line is in the `Business_Management_Project` directory if performing command-line operations.

4.  **Configure Database Connection**:
    * Edit the `application.properties` file to set up your MySQL database connection details. Refer to the **Database** section below for required properties.

5.  **Run the Project**:
    * Execute the `main` method in `BusinessProjectApplication.java`.
    * Alternatively, right-click on the project in STS/Eclipse, then select `Run As` > `Spring Boot App`.

6.  **Access the Application**:
    * Open your web browser and go to `http://localhost:2330/home`.

7.  **Database Initialization**:
    * Upon first run, the application will create the necessary tables in your configured database.
    * **Important**: You must manually add an administrator user record directly into the database to enable admin login and access.

---

## Database Configuration

**MySQL** is the chosen database for this project. Configure your database connection by editing the `src/main/resources/application.properties` file with the appropriate values:

```properties
spring.datasource.name=[Your Database Name]
spring.datasource.url=jdbc:mysql://localhost:3306/[Your Database Name]
spring.datasource.password=[Your password]
spring.datasource.username=[Your username]
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.hibernate.ddl-auto=update
server.port=2330