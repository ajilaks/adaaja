pipeline {
    agent any
    stages {
        stage("Helo") {
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
