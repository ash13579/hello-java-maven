# Jenkins CI/CD Build for a Simple Java Maven Project

This project demonstrates a fundamental Continuous Integration (CI) workflow. A Jenkins Freestyle job was configured to automatically fetch, build, and package a simple "Hello World" Java application using Apache Maven.

## Summary of Accomplishments

We successfully set up a complete CI pipeline from scratch. This involved installing and configuring all necessary tools, creating a Java project, connecting Jenkins to a Git source code repository, and troubleshooting common configuration issues to achieve a successful, automated build.

---

## Steps Completed

1.  **Environment Setup**:
    * Installed **Java Development Kit (JDK) 11** and configured the `JAVA_HOME` system environment variable.
    * Installed **Apache Maven** and configured the `MAVEN_HOME` and `Path` system environment variables to make it accessible from the command line.
    * Launched a **Jenkins LTS** instance using a Docker container for a clean and isolated environment.

2.  **Jenkins Tool Configuration**:
    * Navigated to `Manage Jenkins` > `Global Tool Configuration`.
    * Configured a Maven installation to be automatically downloaded and managed by Jenkins, resolving path issues between the Windows host and the Linux-based Docker container.

3.  **Source Code Management**:
    * Created a simple "Hello World" Java application with its corresponding `pom.xml` file.
    * Pushed the project code to a new **GitHub repository**.

4.  **Jenkins Job Creation & Configuration**:
    * Created a new **Freestyle project** in Jenkins.
    * Configured the **Source Code Management** section to connect to the GitHub repository.
    * Updated the branch specifier from the default `master` to `main` to match the GitHub repository's branch.
    * Added a **Build Step** to "Invoke top-level Maven targets" with the goal `clean package`.

5.  **Successful Build**:
    * Triggered the build and monitored the console output. After resolving initial configuration errors related to paths and branch names, the job executed successfully, cloning the repository and compiling the Java code.

---

## Build Evidence

Below are screenshots documenting the final configuration and the successful result.

### 1. Jenkins Job Configuration

This screenshot shows the core configuration of the Jenkins job, including the GitHub repository URL and the Maven build command.

![Jenkins Job Configuration](https://placehold.co/800x400/2d333b/ffffff?text=Your+Screenshot+of+Jenkins+Job+Configuration+Here)

### 2. Successful Console Output

This screenshot displays the end of the console output for the final build, confirming that the process completed with a `BUILD SUCCESS` message.

![Successful Console Output](https://placehold.co/800x400/2d333b/ffffff?text=Your+Screenshot+of+Successful+Console+Output+Here)
