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
    stage('Update Pom'){
        updatePomVersion('MavenProject/pom.xml')
    }
}
