pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'g++ -o PES1UG20CS723 PES1UG20CS723.cpp'
            }
        }
        stage('Test') { 
            steps {
                sh 'PES1UG20CS723 PES1UG20CS723.cpp'
            }
        }
        stage('Deploy') { 
            steps {
                error 'Pipeline Failed' 
            }
        }
    }
    post{
        success{
            echo 'Pipeline Success'
        }
    	failure{
    		echo 'Pipeline Failed'
    	}
    }
}
