pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }
    stages {
        stage('Build') {
            steps {
                echo 'building'
                sh '''
                    ls -ltr 
                    pwd
                    echo 'hi'
                '''
            }
        }
        stage('test') {
            steps {
                echo 'testing'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        always {
            echo 'I will run always'
        }
        success {
            echo 'runs only when job is sucess'
        }
        failure {
            echo 'runs only when job failed'
        }
    }
}