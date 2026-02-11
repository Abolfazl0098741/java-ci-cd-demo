# Java CI/CD Project with GitLab

This repository demonstrates a complete **CI/CD pipeline implementation** for a Java application using **Maven** and **GitLab CI/CD**. It is designed as a portfolio project to showcase DevOps and automation skills.

---

##  Project Overview

This project automates the build and packaging process of a Java application. Every commit triggers a pipeline that:

* Builds the project using Maven
* Runs automated packaging
* Generates a deployable JAR file
* Stores build artifacts

The pipeline runs inside a Docker-based GitLab Runner for consistency and reliability.

---


## CI/CD Pipeline Workflow

The pipeline is defined in `.gitlab-ci.yml` and consists of the following stages:

### Build Stage

* Cleans previous builds
* Compiles the source code
* Packages the application

Command used:

```bash
mvn clean package
```

### Deploy Stage

* Stores the generated JAR file
* Makes it available as an artifact

Artifacts:

```
target/*.jar
```

---

## Project Structure

```
java-ci-cd/
│
├── src/                # Application source code
├── target/             # Compiled output (generated)
├── .gitlab-ci.yml      # CI/CD configuration
├── pom.xml             # Maven configuration
└── README.md           # Project documentation
```

---

## Download Build Artifact (JAR)

After each successful pipeline run:

1. Open the project in GitLab
2. Go to **CI/CD → Pipelines**
3. Select a successful pipeline
4. Click on **Job → Artifacts**
5. Download the generated `.jar` file

---

##  Run the Application Locally

### Prerequisites

* Java 17+
* Maven 3.8+

### Steps

```bash
git clone <repository-url>
cd java-ci-cd
mvn clean package
java -jar target/your-app.jar
```

---

## Learning Objectives

This project demonstrates:

* Practical usage of GitLab CI/CD
* Automated Java build pipelines
* Artifact management
* Docker-based CI environments
* Professional project documentation

---

## Future Improvements

* Add automated unit testing
* Integrate code quality tools (SonarQube)
* Add deployment to cloud server
* Implement GitHub Actions pipeline
* Add Docker image build stage

---

## Author

**Abolfazl**
Java Developer | DevOps Enthusiast

---

If you find this project useful, feel free to ⭐ star the repository.
