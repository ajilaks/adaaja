pipeline {
        
    environment {
       INITIATING_MSG = "Initiate Job...."
        STARTING_MSG = "Starting Job...."
    }
    agent any
    stages {
        stage("Prepare") {
           environment {
                 APP = credentials("userrahasia")
           }
           steps {
               echo("${INITIATING_MSG}")
               echo("HBD User ${APP_USR}")
               echo("Building App Start on Branch ${env.BRANCH_NAME}")
           }
        }
        stage("Build") {
                options {
                        timeout(time:10, unit:'SECONDS')
                }
           steps {
               sleep 20
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
