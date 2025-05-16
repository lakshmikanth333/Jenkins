pipeline {
    agent any 
        stages {
            stage('Build') {
                steps {
                    script {
                        sh """
                          echo "Hello this is build"
                          """
                    }
                }
            }
            stage('Test') {
                steps {
                    script {
                        sh """
                        echo "This is test"
                        """
                    }
                }
            }   
            stage('Run') {
                steps {
                    script {
                        sh """
                        echo "This is RUN"
                        echo "Second run also"
                        """
                    }
                }
            }   
        }
    }
