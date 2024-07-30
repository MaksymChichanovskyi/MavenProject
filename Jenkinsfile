import ExampleA.Shared

def agentName = 'linux && docker'
def someText = 'Hello!'
 def shared = new Shared()

node(agentName) { //run this part on an agent with label 'linux'
    stage('Checkout') {
       
        checkout scm
    }
     stage('Update Version'){
      shared.updatePomVersion(env.BUILD_NUMBER)
     }
    
  stage('Build'){
      shared.startBuild()
    }
   stage('Get Jar Size'){
    def jarSize = shared.getJarSize('/tmp/jenkins/workspace/MavenProject/target/Education.ExampleA-1.0.${env.BUILD_NUMBER}.jar')
        echo "The size of the JAR file is: ${jarSize} bytes"
   }
 
}
