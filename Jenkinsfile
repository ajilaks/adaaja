pipeline {
    agent any
    stages {
        stage("Build") {
           steps {
               echo("Building App Start on Branch ${env.BRANCH_NAME}")
               sh("chmod +x mvnw")
               sh("./mvnw clean")
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
