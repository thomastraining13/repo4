pipeline {
    agent any
    parameters{
booleanParam defaultValue: false, name: 'skip_test'
    }
    stages {
        stage('build') {
            steps {
                echo 'Hello builkd'
            }
        }
         stage('test') {
             when{expression {params.skip_test!= true}}
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
