pipeline {
    agent any

    stages {
        stage('Run Maven App') {
            steps {
                script {
                    // Загрузка Shared.groovy
                    def sharedScript = libraryResource 'ExampleA/Shared.groovy'
                    
                    // Оцінка скрипту
                    evaluate sharedScript

                    // Виклик основного методу
                    mavenApp()
                }
            }
        }
    }
}
