# Job Portal

A web based, full-stack job portal designed to connect job seekers and employers through a seamless, modern interface.
It allows employers to post job listings, and job seekers can search, filter, and apply for jobs.
Built with Java, Spring Boot, and MySQL, the platform focuses on scalability, speed, and security.

🔐 ## Key Features

- 🔐 **Secure Authentication** – Role-based login for employers & job seekers.  
- 📝 **Job Postings** – Employers can create, edit, and manage job listings.  
- 🔍 **Advanced Job Search** – Filter by title, location, skills, and salary.  
- 📄 **Resume Uploads** – Job seekers can attach resumes directly.  
- 📊 **Application Tracking** – Employers manage received applications.  
- 📱 **Responsive UI** – Works across mobile, tablet, and desktop.  
- 🌐 **RESTful APIs** – Exposes endpoints for jobs, users, and applications.

## Technologies Used
- **Java**: Core programming language (version 17 recommended)
- **Spring Boot**: Framework for building the application
- **Spring MVC**: For handling web requests and responses
- **Spring Data JPA**: For database interactions
- **Hibernate**: ORM for mapping Java objects to database tables
- **MySQL**: Relational database (can be swapped with other databases)
- **Thymeleaf**: Templating engine for server-side rendering
- **Maven**: Dependency management and build tool
- **HTML/CSS/JavaScript**: Frontend technologies
- **Git**: Version control

## Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Charitha-08/JobPortal.git
   cd JobPortal
   ```

2. **Set up the database**:
   - Create a MySQL database (e.g., `job_portal_db`).
   - Update the database configuration in `src/main/resources/application.properties` (see [Configuration](#configuration)).

3. **Install dependencies**:
   Run the following command to download all required Maven dependencies:
   ```bash
   mvn clean install
   ```

## Configuration
Edit the `application.properties` file located in `src/main/resources/` with your database credentials and other settings:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/job_portal_db
spring.datasource.username=JobPortal
spring.datasource.password=JobPortal
spring.jpa.hibernate.ddl-auto=update
spring.thymeleaf.cache=false
server.port=8080
```

- `spring.datasource.url`: URL of your database
- `spring.datasource.username`: Your MySQL username
- `spring.datasource.password`: Your MySQL password
- `spring.jpa.hibernate.ddl-auto`: Set to `update` for automatic schema updates or `create` for a fresh database
- `server.port`: Port where the application will run (default is 8080)

## Running the Application
1. Build and run the project using Maven:
   ```bash
   mvn spring-boot:run
   ```
2. Alternatively, run it from your IDE by executing the `JobPortalApplication` class.

3. Open your browser and navigate to:
   ```
   http://localhost:8080
   ```

## Project Structure
```
job-portal/
│
├── src/
│   ├── main/
│   │   ├── java/com/example/JobPortal/
│   │   │   ├── controller/      # Spring MVC controllers
│   │   │   ├── entity/          # JPA entities (e.g., Job, User)
│   │   │   ├── repository/      # Spring Data JPA repositories
│   │   │   ├── service/         # Business logic
│   │   │   └── JobPortalApplication.java  # Main Spring Boot application class
│   │   └── resources/
│   │       ├── static/          # CSS, JS, and other static assets
│   │       ├── templates/       # Thymeleaf HTML templates
│   │       └── application.properties  # Configuration file
│   └── test/                    # Unit and integration tests
├── pom.xml                      # Maven configuration file
└── README.md                    # This file
```

## Usage
- **Employers**: Register/login, post jobs, and manage applications.
- **Job Seekers**: Register/login, search for jobs, and apply with a resume.

Explore the application at `http://localhost:8080` after starting it.

## Contributing
Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your message"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a Pull Request.