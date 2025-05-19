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
        string(name: 'LAKSHMIKANTH', defaultvalue: 'he is a devops engineer', description: "He is a genius guy")
        text(name: 'SAI', defaultvalue: 'linux admin', description: 'etrade')
        choice(name: 'SHIVA', choices: ['one', 'thirteen', 'three'], description: 'years of exp')
    }
    stages {
        stage('Build') {
            steps {
                sh """
                echo "This is $ENVIRONMENT1 area"
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

