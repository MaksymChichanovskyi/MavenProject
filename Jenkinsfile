import ExampleA.Shared

def agentName = 'linux && docker'
def someText = 'Hello!'
 def shared = new Shared()

node(agentName) { //run this part on an agent with label 'linux'
    stage('Checkout') {
       
        checkout scm
    }

    
  stage('Build'){
     def shared = new Shared()
      shared.startBuild()
      
    }
}
