pipeline {
    agent any
    tools {
        maven "M3"
    }
    stages {
        stage('Build') {
            steps {
                git 'https://github.com/RamshankerLearning/RamLearning.git'
                sh "mvn clean install"
            }
            post {
                success {
                    archiveArtifacts 'target/*.war'
                }
            }
        }
    }
}
