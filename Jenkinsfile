pipeline {
    agent {
    node {
        label 'Agent-1'
        
    }
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
                // sh """
                // echo 'Here I wrote shell script'
                // echo "$GREETING"
                // """ 
                echo 'Success..'
            }
        }
    }
}
    //post build
    post { 
        always { 
            echo 'I will always say Hello again!'
        }

        failure { 
            echo 'This is Failed!'
        }
    }


   