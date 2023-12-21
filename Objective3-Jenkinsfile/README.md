# Jenkinsfile Summary

This Jenkinsfile contains a pipeline that automates several stages:

## Stages:
1. **Prehook:**
    - Checks GitHub, JDK version, Docker, and MicroK8s installations.

2. **Pull Code:**
    - Clears workspace directory and fetches code from a GitHub repository.

3. **Build Application:**
    - Moves to a specific directory and builds a Maven project.

4. **Build Docker Image:**
    - Builds a Docker image from the application and lists Docker images.

5. **Push Docker Image:**
    - Logs in to DockerHub and pushes the Docker image.

6. **Deploy Helm Chart:**
    - Installs a Helm chart using MicroK8s.

7. **Helm Chart Deployment Status:**
    - Checks the status of Helm chart deployment and lists running objects.

8. **Test API Call:**
    - Makes an API call to test the deployed application.

### Prerequisites for Running Jenkinsfile:

1. **Jenkins Installation:**
   - Ensure Jenkins is installed and running.
   - Make sure Jenkins has appropriate plugins installed for the tools used in the pipeline (GitHub, Docker, Helm, etc.).

2. **Jenkins Pipeline Configuration:**
   - Set up a Jenkins pipeline job.
   - Configure the pipeline job to use the provided Jenkinsfile.

3. **Credentials Configuration:**
   - Create DockerHub credentials in Jenkins to authenticate for Docker image push/pull.
   - Ensure credentials for accessing GitHub repositories are set up if required.

4. **Tools and Environments:**
   - **Java Development Kit (JDK):**
     - JDK should be installed and configured on the Jenkins environment.
   - **Docker:**
     - Docker should be installed and accessible on the Jenkins server.
   - **Helm:**
     - Helm should be installed and configured in the Jenkins environment.
   - **MicroK8s:**
     - MicroK8s should be installed and configured for Kubernetes operations if used in the pipeline.

5. **Workspace Setup:**
   - Ensure the Jenkins workspace has appropriate permissions and space to execute the pipeline.
   - Make sure the pipeline can access and interact with the necessary directories and repositories.

6. **Project Configuration:**
   - Verify that the paths, URLs, and names specified in the Jenkinsfile match the project's structure and configurations.
   - Adjust global variables like `app_docker_image` and `helm_chart_name` as per your project's specifications.

7. **Networking and Permissions:**
   - Ensure proper network connectivity for accessing external resources like GitHub, DockerHub, and any required APIs.
   - Permissions should be set up to allow Docker commands, Helm installations, and other necessary operations within Jenkins.

### Prerequisites for Running Jenkinsfile:

- **Step 1:** Ensure Jenkins is installed and running with necessary plugins
- **Step 2:** Create a Jenkins pipeline job.
- **Step 3:** Set up DockerHub credentials in Jenkins for image push/pull.
- **Step 4:** Configure the pipeline job using the provided Jenkinsfile.
- **Step 5:** Validate each stage individually before running the full pipeline.