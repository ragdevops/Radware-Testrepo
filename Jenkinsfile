pipeline {
    agent {
        dockerfile {
            filename 'Dockerfile'
            label 'zip-job-docker'
            additionalBuildArgs '--privileged' 
        }
    }
    environment {
        ARTIFACTORY_URL = 'https://http://ec2-52-23-177-246.compute-1.amazonaws.com:8081/artifactory/webapp/#/home/
        ARTIFACTORY_USER = 'superman'
        ARTIFACTORY_PASSWORD = 'P@ssw0rd123$'
        REPO_PATH = "store-artifacts/${env.VERSION}"
    }
    stages{
        stage ('checkout stage') {
          steps {
             git url:'https://github.com/ragdevops/Radwaretest.git'
             }
      }
   }
}