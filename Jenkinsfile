pipeline {
    agent {
           label 'zip-job-docker'
    }
    stages{
      stage('Checkout Source') {
         steps {
            git branch: 'main', url: 'https://github.com/ragdevops/Radwaretest.git'             
      }
    }
        stage('Build') {
            steps {
                sh 'python3 zip_job.py'
            }
        }
    }
}
