pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
            sh 'echo Build Step'
        }
        }
        stage('Test') {
            steps {
             sh 'echo Test Step'
            
        }
        }
        stage('Deploy') {
            steps {
            sh 'echo Deploy Step'
            error 'pipeline failed'
        }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success {
            echo 'your job is got succeded'
        }
        failure {
            echo 'your job is got failed'
        }
    }
}
