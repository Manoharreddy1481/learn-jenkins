pipeline {
    agent {
        label 'AGENT-1'
    }
    stages {
            stage("Build") {
                steps {
                    sh "echo Build Stage"
                }
            }
             stage("Test") {
                steps {
                    sh "echo Test Stage"
                }
            }
            stage("Deploy") {
                steps {
                    sh "echo Deploy stage"
                    //error "Pipeline fail"
                }
            }
    }
    post {
        always {
            echo "This section runs Always"
            deleteDir()
        }

        success {
            echo "This section runs when job got Success"
        }

        failure {
            echo "This section runs when job got Failure"
        }
    }
    
}
