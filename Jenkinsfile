pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS448-Pipeline PES1UG20CS448.cpp'
                build job: 'PES1UG20CS448-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS448-Pipeline'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
