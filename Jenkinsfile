pipeline {
    agent {
    node {
        label 'AGENT-1'
        }
    }
    // build
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    // post
     post { 
        always { 
            echo 'I will always say Hello again!'
        }

         failure { 
            echo 'This run when pipeline failed!'
        }

         success { 
            echo 'This will run when pipeline is success'
        }
    }
}