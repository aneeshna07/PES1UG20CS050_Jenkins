pipeline {
    agent any
    stages {

        stage('Build') {
            steps {
                sh 'g++ PES1UG20CS050.cpp'
                build job:'PES1UG20CS050-1'
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps{
                sh './a.out'
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps{
                echo 'Deployment Successful'
            }
        }

    }

    post{
        failure{
            echo 'Pipeline failed'
        }
    }
}
