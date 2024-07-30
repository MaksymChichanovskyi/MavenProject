import ExampleA.Shared

def agentName = 'linux && docker'
def someText = 'Hello!'


node(agentName) { //run this part on an agent with label 'linux'
    stage('Checkout') {
        def shared = new Shared()
        shared.CheckoutGit()
    }

    
  stage('Build'){
     def shared = new Shared()
      shared.startBuild()
    }
    
    stage('Print JAR Size') {
            steps {
                script {
                    // Ось як ви можете вивести розмір JAR-файлу
                    def jarFile = 'target/your-app-name-${env.BUILD_NUMBER_VERSION}.jar'  // Шлях до вашого JAR-файлу
                    def size = sh(script: "du -sh ${jarFile} | cut -f1", returnStdout: true).trim()
                    echo "Size of the JAR file ${jarFile} is ${size}"
                }
            }
        }
}
