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
        choice(name: 'Environment', choices: ['PROD', 'DEV', 'TEST'], description: 'select the environment')
        password(name: 'jenkins', defaultValue: '3K3Klks$', description: 'password for the jenkins')
        file(name: 'jenkins_file', defaultValue: 'jenkindfile', description: 'upload a file')
    }
    stages {
        stage('Build') {
            steps {
                sh """
                echo "This is $ENVIRONMENT1 area"
                echo "Hello Mr ${param.LAKSHMIKANTH}
                echo "current choices are ${param.SHIVA}
                echo "guy is ${param.SAI} 
                """
            }

        }
        stage('UAT') {
            steps {
                sh """
                echo "This is $ENVIRONMENT2 area"
                """
            }
        }
    }
    
    post {
        success {
            echo "$ENVIRONMENT1 area &  $ENVIRONMENT2 area got succesed"
        }
        failure {
            echo "$ENVIRONMENT1 area &  $ENVIRONMENT2 area got failed"
        }
    }

}

