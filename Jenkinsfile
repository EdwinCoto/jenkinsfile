pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo ( "hello world 2")
            }
        }
        stage('Deploy') {
            steps {
                script {
                    multiDeployToProd([:])
                }
            }
        }
    }
}


    void multiDeployToProd(Map opts = [:]){

        def stages = [:]

        stages["CA"] = {
            input "Deploy to 'CA Production'?"
            firstStage("ca")
            secondStage("ca")

        }

        stages["CO"] = {
            input "Deploy to 'CO Production'?"
            firstStage("co")
            secondStage("co")

        }

        stage("Production Deployment"){
            parallel stages
        }
    }

void firstStage (String center){
    echo "First Stage : ${center}"
}
void secondStage (String center){
    echo "Second Stage : ${center}"
}
