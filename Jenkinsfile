pipeline {
    agent {
        docker {
            image 'maven:3.6-jdk-8-slim' 
            args '--network jenkins -v maven-repo:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -e -DskipTests clean package' 
            }
        }
    }
}