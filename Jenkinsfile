pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Hello builkd'
            }
        }
         stage('test') {
            parallel{
                stage('unit tst'){
                   steps {
                echo 'Hello unit testing '
            }}
                 stage('integration tst'){
                   steps {
                echo 'Hello integration test'
            }}
            }
        }
        stage('deploy') {
            steps {
                echo 'Hello deply'
            }
        }
    }
}
