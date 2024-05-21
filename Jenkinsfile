pipeline {
    agent {
    node {
        label 'AGENT-1'
        }
    }

    environment { 
        Name = 'Pavan'
    }

    options {
        timeout(time: 1, unit: 'SECONDS') 
        disableConcurrentBuilds() 
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
                sh """
                    echo 'Here I am writing shell script'
                    echo '$Name'
                """
                // echo 'Deploying....'
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