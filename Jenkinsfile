node {
    
    docker.image('maven:3.6-alpine').inside('--network host -v maven-repo:/root/.m2') {
    
        stage('Build') {
            sh 'mvn -B -DskipTests clean package'
        }
        
        try{
            stage('Test') {
                sh 'mvn test'
            }
        }
        finally {
            junit 'target/surefire-reports/*.xml'
        }
        
        stage('Deliver') {
            sh './jenkins/scripts/deliver.sh'
        }
    }
}