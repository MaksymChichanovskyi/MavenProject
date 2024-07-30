pipeline {
    agent any

    stages {
        stage('Run Maven App') {
            steps {
                script {
                   
                    shared.mavenApp()
                }
            }
        }
    }
}
