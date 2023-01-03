@Library("jenkins-automation-alpha@main") _

pipeline {
   parameters {
       choice(name:"BUILD_TYPE", choices:['BUILD', 'SNAPSHOT', 'RELEASE'])
   }

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
               script {
                    hello.world()
                    maven.build("clean compile")
               }
               echo("Building App Start on Branch ${env.BRANCH_NAME}")
           }
        }
        stage("Build") {
           steps {
               sleep 20
               echo("${STARTING_MSG}")
               echo("Build type: ${params.BUILD_TYPE}")
               echo("Building App Start on Branch ${env.BRANCH_NAME}")
           }
        }

        stage("Release") {
           when {
              expression{
                 return params.BUILD_TYPE == 'RELEASE'
              }
           }
           steps {
               echo("EXECUTING RELEASE....")
               sleep 20
               echo("VERSION RELEASED")
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
