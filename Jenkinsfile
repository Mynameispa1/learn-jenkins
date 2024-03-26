pipeline {
    agent {
    node {
        label 'AGENT-1'
    }
}
    environment { 
        Greeting = 'Hello Jenkins'
    }
   //   build
    stages {
        stage('Build') { 
            steps {
                echo 'Buiulding..'
            }
        }
        stage('Test') { 
            steps {
                echo 'Testing...' 
            }
        }
        stage('Deploy') { 
            steps {
                sh '''
                    echo "Here I am writing shell script"
                    env
                '''
            }
        }
    }
  //post build
  post { 
        always { 
            echo 'I will always say Hello again!'
        }

    failure {  
            echo 'This run is the pipepline get fail...'
        }
    success {
        echo 'This run if the pipeline success...'
    }    
  }
}