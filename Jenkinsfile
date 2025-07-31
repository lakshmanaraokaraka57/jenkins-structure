pipeline {
    agent any

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Lakshman', description: 'Please enter your good name')
    }

    stages {
        stage('Build') {
            steps {
                script {
                  
                    bat "Hello Lakshman this is build"
                    bat "${PERSON}"
                   
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    
                   bat "Hello Lakshman this is Test"
                 
                }
            }
        }

        stage('Deploy') {
                    input {
            message 'Should we continue?'
            ok 'Lakshman'
            parameters {
                string(name: 'PERSON', defaultValue: 'Mr Lakshman', description: 'Please enter your good name')
            }
        }

            steps {
                script {
                   
                    bat "Hello Lakshman this is Deploy"
                    
                }
            }
        }
    }

    post {
        always {
            bat 'Deployment successfully completed'
        }
        failure {
            bat 'Please check your deployment pipelines, there is an error'
        }
        success {
            bat 'Your Deployment is successfully completed'
        }
    }
}