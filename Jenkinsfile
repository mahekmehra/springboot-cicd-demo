pipeline {
    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t springboot-demo .'
            }
        }

        stage('Docker Run') {
            steps {
                bat 'docker run -d -p 8080:8080 springboot-demo'
            }
        }

    }
}
