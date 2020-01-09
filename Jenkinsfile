pipeline {
    agent {
        docker {
            image 'maven:3.6-jdk-8-slim' 
            args '-u root' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -e -DskipTests clean package' 
            }
        }
    }
}