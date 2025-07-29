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
                    '''
                }
            }
            post {
                success {
                    // Linux notification
                    sh 'notify-send "Jenkins Alert" "✅ Deployment successful!"'
                }
            }
        }
    }
}