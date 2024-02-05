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

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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

        stage('check params'){
            steps {
                sh """
                    echo "Hello ${params.PERSON}"

                    echo "Biography: ${params.BIOGRAPHY}"

                    echo "Toggle: ${params.TOGGLE}"

                    echo "Choice: ${params.CHOICE}"

                    echo "Password: ${params.PASSWORD}"
                """
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


   