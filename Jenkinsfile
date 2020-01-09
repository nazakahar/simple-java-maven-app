pipeline {
    agent {
        docker {
            image 'maven:3.6.3-jdk-8' 
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