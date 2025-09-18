pipeline {
    agent any

    tools {
        jdk 'Java 17' // The JDK you configured in Jenkins
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                bat '.\\mvnw.cmd clean package -DskipTests'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests...'
                bat '.\\mvnw.cmd test'
            }
        }
    }
}
