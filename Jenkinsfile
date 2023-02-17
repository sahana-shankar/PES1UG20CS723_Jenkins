pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS723 PES1UG20CS723.cpp'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS723'
                echo 'Test Stage Successful'
                
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage Successful'
            }
        }
    }

        post {
            failure {
                echo 'Pipeline Failed'
            }
        }
}
