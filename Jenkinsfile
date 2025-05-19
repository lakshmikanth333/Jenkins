pipeline {
    agent { label 'slave'}
    environment {
        ENVIRONMENT1 = 'BUILD'
        ENVIRONMENT2 = 'UAT'

    }
    options {
        disableConcurrentBuilds()
        timeout(time:10, unit:'SECONDS')
        retry(3)
    }
    parameters {
        string(name: 'LAKSHMIKANTH', defaultValue: 'he is a devops engineer', description: "He is a genius guy")
        text(name: 'SAI', defaultValue: 'linux admin', description: 'etrade')
        choice(name: 'ENVIRONMENT', choices: ['PROD', 'DEV', 'TEST'], description: 'select the environment')
        password(name: 'JENKINS', defaultValue: '3K3Klks$', description: 'password for the jenkins')
        file(name: 'DATA_FILE', description: 'upload a file')
        booleanParam(name: 'TOGGLE', defaultValue: 'false', description: 'selected value')
    }
    stages {
        stage('Build') {
            steps {
                retry(5) {
                sh """
                echo "This is $ENVIRONMENT1 area"
                echo "the string is: ${params.LAKSHMIKANTH}"
                echo "the text is: ${params.SAI}"
                echo "the choice is: ${params.ENVIRONMENT}"
                echo "the password is: ${params.JENKINS}"
                echo "the file is: ${params.DATA_FILE}"
                echo "the toogle is: ${params.TOGGLE}"
                
     
                """
            }
        }

        }
        stage('UAT') {
            steps {
                sh """
                echo "This is $ENVIRONMENT2 area
                """
            }
        }
    }
    
    post {
        success {
            echo "$ENVIRONMENT1 area &  $ENVIRONMENT2 area got succesed"
        }
        failure {
            echo "$ENVIRONMENT1 area &  $ENVIRONMENT2 area got failed
        }
    }

}


