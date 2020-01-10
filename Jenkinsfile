node {
    
    docker.image('maven:3.6-alpine').inside('--network host -v maven-repo:/root/.m2') {
    
        stage('Email Notification') {
            // sh 'mvn -B -DskipTests clean package'
            mail mimeType: 'text/html',
                 subject: "[Jenkins] Approval Request",
                 to: "nazakahar@gmail.com",
                 body: '''<a href="${BUILD_URL}input">click to approve</a>'''
        }
        
        // try{
        //     stage('Test') {
        //         sh 'mvn test'
        //     }
        // }
        // finally {
        //     junit 'target/surefire-reports/*.xml'
        // }
        
        // stage('Deliver') {
        //     sh './jenkins/scripts/deliver.sh'
        // }
    }
}