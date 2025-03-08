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
        sh 'docker build -t my-app .'
        sh 'docker run -d -p 8080:8080 my-app'
    }
}

    }
}
