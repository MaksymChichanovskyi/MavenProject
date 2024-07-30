import ExampleA.Shared

def agentName = 'linux && docker'
def someText = 'Hello!'

node(agentName) { //run this part on an agent with label 'linux'
    stage('Checkout') {
        checkout scm
       /* def shared = new Shared()
        shared.CheckoutGit()*/
    }
    stage('Update pom'){
        steps{
            script{
             UpdatePom.updateVersion(env.BUILD_NUMBER)
        }
    }
    }
  stage('Build'){
     def shared = new Shared()
      shared.startBuild()
    }
}
