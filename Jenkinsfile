pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o pes2ug20cs488-1 task5.cpp'
                echo "Build Successful"
            }
        }
        stage('Test') {
            steps {
                sh './pes2ug20cs488-1'
                sdubcold
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
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
