pipeline {
    agent any
    stages {
        stage("Build") {
           steps {
               ./mvnw clean
           }
        }
    }
    
    post {
        always {
            echo "BUILD ADAAJA"
        }
        success {
            echo "BUILD SUCCESS"
        
        }
    }
}
