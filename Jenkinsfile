pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v c:/docker-data/jenkins-data:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}