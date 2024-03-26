pipeline {
    agent {
    node {
        label 'AGENT-1'
    }
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
                echo 'Deploy.'
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
        echo 'This run if thw pipeline success...'
    }    
  }
}