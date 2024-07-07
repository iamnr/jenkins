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
    }
}