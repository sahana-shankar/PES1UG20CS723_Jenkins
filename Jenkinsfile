pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS723-1 hello.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS723-1'
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
