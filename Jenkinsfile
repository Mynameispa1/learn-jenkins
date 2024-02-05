pipeline {
    agent {
    node {
        label 'Agent-1'
        }
    }

     environment { 
        GREETING = 'Hello Pavan'
    }    

     options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds() 
    }
  // Build stage
    stages {
        stage('Build') { 
            steps {
                echo 'building..'
            }
        }
        stage('Test') { 
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') { 
            steps {
                sh """
                echo "Here I wrote shell script"
                echo "$GREETING"
                env
                """ 
                // echo 'Success..'
            }
        }
    }
    //post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }

        failure { 
            echo 'This is Failed...!'
        }

        success {
            echo 'This is success...!'
        }
    }
}    


   