pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                def ipa = steps.findFiles(glob: "**/**/*.groovy")
                echo "ipa: ${ipa}"
                }
            }
        }
    }
}
