pipeline {
    agent {
        label 'AGENT-1'
    }
    options{
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
        retry(2)
    }
    stages {
            stage("Build") {
                steps {
                    sh "echo Build Stage"
                    //sh 'sleep 10'
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
                    error "Pipeline fail"
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
