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
       script {
            
                    def jarFile = 'target/Education.ExampleA-${env.BUILD_NUMBER_VERSION}.jar'
                    def size = sh(script: "du -sh ${jarFile} | cut -f1", returnStdout: true).trim()
                    echo "Size of the JAR file ${jarFile} is ${size}"
                }
    }
    
}
