pipeline {
    agent {
        node {
            label 'agent-1'
        }
    }

    options {
        ansiColor('xterm')
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

        stage('approve') {
            steps {
                input "Shall I proceed?"
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