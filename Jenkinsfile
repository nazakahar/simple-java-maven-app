pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v C:/Users/nadzaruddin.kahar/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'hostname'
                sh 'mvn -B -e -DskipTests clean package' 
            }
        }
    }
}