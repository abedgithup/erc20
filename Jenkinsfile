pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-repo.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean install'  // Modify for Maven: sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'maven test'
            }
        }

        stage('Deploy') {
            steps {
                sh 'scp target/*.jar user@your-server:/deploy/path'
            }
        }
    }
}
