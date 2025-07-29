pipeline {
    agent any

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Lakshman', description: 'Please enter your good name')
    }

    stages {
        stage('Build') {
            steps {
                script {
                    sh '''
                    echo "Hello Lakshman this is build"
                    echo "${PERSON}"
                    '''
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh '''
                    echo "Hello Lakshman this is Test"
                    '''
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
                    sh '''
                    echo "Hello Lakshman this is Deploy"
                    '''
                }
            }
        }
    }


    post {
        always {
            echo 'Deployment successfully completed'
        }
        failure {
            echo 'Please check your deployment pipelines, there is an error'
        }
        success {
            echo 'Your Deployment is successfully completed'
        }
    }
}