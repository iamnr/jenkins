pipeline {
    agent {node {label 'AGENT-1'}}

    stages {
        stage('Build') {
            steps {
                echo 'Building..'

                sh 'echo "hello there" > /tmp/hello.txt'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }

    post {
        always {
            echo 'runs always'
        }

        success {
            echo 'Runs only when sucess'
        }

        failure {
            echo 'Runs when failed'
        }
    }
}