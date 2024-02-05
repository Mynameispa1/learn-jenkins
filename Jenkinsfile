pipeline {
    // agent {
    //     node {
    //         label 'AGENT-1'
        
    //     }
    // } 

    // environment { 
    //     GREETING = 'Hello Jenkins'
    // }

    // options {
    //     timeout(time: 1, unit: 'HOURS') 
    //     disableConcurrentBuilds()
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
                echo 'Here I wrote shell script'
                echo "$GREETING"
                """ 
            }
        }
    }

    // post build 
    // post { 
    //     always { 
    //         echo 'I will always say Hello again!'
    //     }
    //     failure {
    //         echo 'This block will execute if the pipeline failed..'
    //     }
    //     success {
    //         echo 'It is successful'
    //     }
    // }
// }
