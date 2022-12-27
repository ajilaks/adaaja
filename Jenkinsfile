pipeline {
    agent any
    stages {
        stage("Helo") {
           steps {
                echo("Hi There")
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
