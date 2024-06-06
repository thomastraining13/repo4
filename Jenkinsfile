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
        

        stage('deploy') {
            steps {
                execute_stage('deploy',params.skip_test)
            }
        }
    }
}

def execute_stage(stage_name,skip){
stage(stage_name){
if(skip)
{
echo "skippping ${stage_name} stage"
return
}


}
}
