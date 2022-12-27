pipeline {
        
    environment {
        STARTING_MSG = "Starting Job...."
    }
    agent any
    stages {
        stage("Build") {
           steps {
               echo("${STARTING_MSG}")
               echo("Building App Start on Branch ${env.BRANCH_NAME}")
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
