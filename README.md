# Java Maven Build with Jenkins

This project demonstrates how to set up a **Java Maven** build in **Jenkins**. It contains a simple "Hello World" Java application, which is built using Maven, integrated with Jenkins for continuous integration.

## Prerequisites

Before running the project, ensure you have the following installed:

- **Java 8 or 11** (OpenJDK or Oracle JDK)
- **Maven 3.x**
- **Git** (for version control)
- **Jenkins** (can be set up locally or on a server)
- **GitHub Repository** (for version control and integration)

## Setup Instructions

### Clone the Repository

First, clone the repository to your local machine or server:

```bash
git clone https://github.com/tharunkatta10/java-maven-build.git
cd java-maven-build
```

### Build with Maven

To build the project using Maven, run the following command:

```bash
mvn clean package
```

This command will clean any previously compiled files and create a new build of the project.

### Jenkins Setup

1. **Install Maven in Jenkins:**
   - Go to **Manage Jenkins** → **Global Tool Configuration**.
   - Add Maven with the version **3.8.6** (or any version you prefer).

2. **Create a Freestyle Project:**
   - In Jenkins, click on **New Item** → Select **Freestyle Project**.
   - Under **Source Code Management**, choose **Git** and add your repository URL:
     ```
     https://github.com/tharunkatta10/java-maven-build.git
     ```

3. **Build the Project:**
   - In the **Build** section, select **Invoke top-level Maven targets**.
   - Set the goal as:
     ```
     clean package
     ```

4. **Run the Build:**
   - After configuring the job, trigger the build manually or set up automatic builds using GitHub webhooks.

### Continuous Integration with GitHub Webhook (Optional)

You can set up a **GitHub webhook** to automatically trigger the Jenkins build whenever you push changes to GitHub.

#### Steps:
1. Go to **GitHub Repository** → **Settings** → **Webhooks**.
2. Add the webhook URL from your Jenkins server.

## Project Structure

The project includes the following key components:

```
java-maven-build/
├── pom.xml                # Maven configuration file
├── src/                   # Java source code
│   └── main/
│       └── java/
│           └── HelloWorld.java  # Hello World Java class
├── screenshots/           # Folder to store build-related screenshots (optional)
│   └── .gitkeep           # Keeps the screenshots folder tracked
└── README.md              # This file
```


## Author

**Tharun Katta**  
- [GitHub Profile](https://github.com/tharunkatta10)  
- [LinkedIn Profile](https://www.linkedin.com/in/tharunkatta)  
- Email: [tharunkatta10@gmail.com](mailto:tharunkatta10@gmail.com)

---
