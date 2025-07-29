pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh ''' 
                    echo "Hello Lakshman this is build" 
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
            steps {
                script {
                    sh ''' 
                    echo "Hello Lakshman this is Deploy" 
                    jjhk
                    '''
                }
            }
        }
    }
        post{
            always{
                echo ' Deployment successfully completed'
            }
            failure{
                echo 'Please check your deployment pipelines there is an error'
            }
            success{
                echo 'Your Deployment is successfully completed'
            }
        }
}