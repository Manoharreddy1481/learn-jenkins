pipeline {
    agent any
    stages {
            stage("Build") {
                steps {
                    sh "echo Build Stage"
                }
            }
             stage("Test") {
                steps {
                    sh "echo Test Stage"
                    abcd
                }
            }
            stage("Deploy") {
                steps {
                    sh "echo Deploy stage"
                }
            }
    }
    post {
        always {
            echo "This section runs Always"
        }

        success {
            echo "This section runs when job got Success"
        }

        failure {
            echo "This section runs when job got Failure"
        }
    }
    
}
