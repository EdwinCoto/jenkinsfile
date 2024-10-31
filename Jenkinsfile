pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                def files = steps.findFiles(glob: "${env.WORKSPACE}/**/*.groovy")
echo """${files[0].name} ${files[0].path} ${files[0].directory} ${files[0].length} ${files[0].lastModified}"""
                }
            }
        }
    }
}
