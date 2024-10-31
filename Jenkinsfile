pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                script {
                def ipa = steps.findFiles(glob: "**/**/*.groovy").collect { it.path }
                echo "ipa: ${ipa}"
                }
            }
        }
    }
}
