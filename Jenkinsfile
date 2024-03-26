pipeline {
    agent {
    node {
        label 'AGENT-1'
    }
}
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
}