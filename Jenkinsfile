pipeline {
    agent {
        docker {
            image 'maven:3.6-jdk-8-slim' 
            args '-v C:/Users/nadzaruddin.kahar/.m2:/root/.m2' 
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