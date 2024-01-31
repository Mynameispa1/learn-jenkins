pipeline {
    agent {
        node {
            label 'AGENT-1'
        
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
                echo 'Deploying..' 
            }
        }
    }

    // post build 
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure {
            echo 'This block will execute if the pipeline failed..'
        }
        success {
            echo 'It is successful'
        }
    }
}