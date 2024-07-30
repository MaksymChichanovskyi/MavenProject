pipeline {
    agent any

    stages {
        stage('Run Maven App') {
            steps {
                script {
                    // Завантаження бібліотеки
                    def shared = new ExampleA.Shared()
                    
                    // Виклик основного методу
                    shared.mavenApp()
                }
            }
        }
    }
}
