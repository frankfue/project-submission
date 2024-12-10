# project-submission

This documentation provides an overview of the "My Web Application" project, its technical components, and its functionality. This web application is built using Spring Boot with Thymeleaf for view rendering. It includes various features such as user authentication, a responsive UI with sliders, and dynamic content updating using JavaScript.

Architecture Overview
Technology Stack:

Frontend: HTML, CSS, JavaScript, jQuery
Backend: Spring Boot, Spring Web, Spring Thymeleaf

Database: Not directly connected to a database in this project, but the architecture is designed to support it with the addition of a JPA repository or similar.

Testing: JUnit for unit testing

Features
User Authentication:
Users can log in using session storage to maintain authentication state.
Login and logout functionality with messages displayed based on authentication status.

Dynamic Content:
About me and blog sliders implemented using Slick.js for a responsive and interactive experience.
A counter that animates numbers as the user scrolls down the page.

Responsive Design:
The project is optimized for mobile and desktop views with breakpoints set for different screen sizes.

Flowchart for User Authentication:
Steps:
User lands on the home page.
If authenticated, the session is checked using sessionStorage.
If authenticated, welcome message is displayed.
If not authenticated, a logout message is shown.
On clicking login, the user is authenticated and session data is updated.
On clicking logout, the session is invalidated and the state is updated.

Technical Details of Pages

Home Page (index.html):
Contains navigation menu and welcome message.
Uses JavaScript/jQuery for client-side interactivity (toggle navigation, show/hide elements).
Includes links to about-me, blog, and other sections.

About Me Slider (about-me.html):
Implements a responsive slider for personal information.
Customizable with additional slides as needed.

Blog Section (blog.html):
Blog posts are displayed in a slider format with two visible posts at once.
Slider adjusts based on screen size using responsive settings.

Counter Section:
Scroll-triggered animation for numbers, showing statistics as the user scrolls down.
Uses jQuery to detect scroll position and trigger animations.

User Interaction
Login:
Users enter credentials and click login.
If successful, a welcome message is displayed with the user's name.
Logout:
Users can log out by clicking a button, which invalidates the session.
A goodbye message is displayed.

1. Clone the GitHub Repository
To get started with the project, follow these steps:

Open your terminal.
Navigate to the directory where you want to clone the repository:
bash
cd /path/to/your/projects

Clone the repository using Git:
bash
git clone https://github.com/your-username/my-web-app.git

Navigate into the project directory:
bash
cd my-web-app

2. Project Structure
The project is organized with the following directory structure for better readability and ease of use:

plaintext
my-web-app/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   ├── com/
│   │   │   │   └── example/
│   │   │   │       └── mywebapp/
│   │   │   │           ├── MyWebAppApplication.java
│   │   │   │           ├── controller/
│   │   │   │           │   └── WebController.java
│   │   │   │           ├── MyWebAppApplicationTests.java
│   │   │   │           └── ... (other classes as needed)
│   │   ├── resources/
│   │   │   ├── static/
│   │   │   │   └── js/ (JavaScript files)
│   │   │   ├── templates/
│   │   │   │   ├── index.html
│   │   │   │   ├── about-me.html
│   │   │   │   ├── blog.html
│   │   │   │   └── ... (other Thymeleaf templates)
│   │   └── application.properties (Spring Boot configuration file)
├── target/ (compiled classes and artifacts)
└── .gitignore
Java Files:

MyWebAppApplication.java – Main entry point for the application.
MyWebAppApplicationTests.java – Unit tests for the application context.
WebController.java – Controller handling routing to Thymeleaf templates.
Templates:

index.html, about-me.html, blog.html, etc., located in src/main/resources/templates/, serve as the view components for the application.
These files use Thymeleaf for templating, allowing for dynamic content rendering and variable interpolation.
Static Resources:

JavaScript files for client-side interactivity are located in src/main/resources/static/js/.
This includes jQuery and any additional scripts necessary for the web application’s functionality.
3. How to Run the Application
To run the "My Web Application" locally:

Ensure you have Java 17 installed (required by Spring Boot):

Check your Java version with:
bash
java -version
If you need to install or update Java, refer to this guide.
Run the Spring Boot application:

bash
./mvnw spring-boot:run
Access the application in your browser:

Open a web browser and go to http://localhost:8080.
This will take you to the home page as defined by the WebController’s @GetMapping("/") method.
4. Directory Structure and Code Organization
The project’s directory structure has been organized for clarity and maintenance:

src/main/java/com/example/mywebapp/:

MyWebAppApplication.java – Main class that launches the Spring Boot application.
MyWebAppApplicationTests.java – JUnit tests to verify application context loads.
controller/:
WebController.java – Handles the main routes and map them to Thymeleaf templates (e.g., home page, about me page).
src/main/resources/:

static/:
js/ – Contains custom JavaScript files such as main.js, which handles navigation, sliders, and scroll animations.
templates/:
index.html, about-me.html, blog.html, etc., are Thymeleaf templates that define the HTML structure and dynamically populate content based on user actions and session state.
These templates utilize Thymeleaf’s tag attributes (th:text, th:href, etc.) to bind data from the backend.

VIDEO AND SCREENSHOTS HAVE BEEN PROVIDED
