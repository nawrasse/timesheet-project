pipeline {
    agent any

    stages {
        stage('GIT') {
            steps {
                git branch: 'master', url: 'https://github.com/nawrasse/timesheet-project.git'
            }
        }

        stage('COMPILATION') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('DEPLOIEMENT') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}
