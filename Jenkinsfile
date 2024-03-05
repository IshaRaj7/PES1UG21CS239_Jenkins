pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                sh 'g++ non_existent_file.cpp -o output' // Intentional error: compiling a non-existent file
            }
        }
        stage('Test') {
            steps {
                sh './run_tests.sh'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
