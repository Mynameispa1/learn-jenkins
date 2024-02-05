pipeline {
    agent any
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
                echo 'Here I wrote shell script'
                echo "$GREETING"
                """ 
            }
        }
    }
}

   