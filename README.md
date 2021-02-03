## Docker installation instructions for Jira with MySQL

1. Make sure you have Docker and Docker Compose installed.
   If you haven't installed it yet, follow the following links:
   [Install Docker](https://docs.docker.com/get-docker/)
   [Install Docker Compose](https://docs.docker.com/compose/install/)

2. Then write the command on the command line:
   `git clone https://github.com/your-website/docker-for-jira-mysql`

3. In the project folder enter the following command and wait for the installation
   `docker-compose up -d`

4. [Download mysql-connector](https://dev.mysql.com/downloads/connector/j/8.0.html)
   **Unzip the archive and put mysql-connector-java-8.0.23.jar in your project folder**

5. Enter the following commands:
   `docker cp mysql-connector-java-8.0.23.jar jira:/opt/atlassian/jira/lib`
   `docker restart jira`

6. Go to the site http://localhost:8080/ and follow the instructions

##### Note:

To generate a license key follow the link and click on the Generate License button
[Generate a license key](https://my.atlassian.com/license/evaluation?utm_nooverride=1&utm_nooverride=1&ref=prod&product=jira-software.data-center&version=8.15.0&build=815001&sid=BLR7-K013-6S3E-Z468&licensefieldname=setupLicenseKey&callback=http%3A%2F%2Flocalhost%3A8080%2Fsecure%2FSetupLicense%21default.jspa)

**To shutdown the container enter the following command:**
`docker-compose down`
