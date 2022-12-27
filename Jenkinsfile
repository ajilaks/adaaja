pipeline {
    agent any
    stages {
        stage("Build") {
           steps {
               echo("BUILDING APP")
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
