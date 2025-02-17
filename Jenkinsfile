pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'python --version'  // Modify for your project
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'hello.py/'  // Update as per your test command
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to AWS EC2...'
                sshagent(['EC2-SSH-CREDENTIALS']) {
                    sh 'ssh ec2-user54.90.72.59 "bash /home/ec2-user/deploy.sh"'
                }
            }
        }
    }
    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
