import ExampleA.Shared

def agentName = 'linux && docker'
def someText = 'Hello!'

node(agentName) { //run this part on an agent with label 'linux'
    stage('Checkout') {
        checkout scm
       /* def shared = new Shared()
        shared.CheckoutGit()*/
    }

     stage('reading xml')

 ​​ ​​ ​​​​ {

 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ readxml = readMavenPom file: '';  ​​ ​​ ​​ ​​ ​​ ​​​​ 

 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ def name_var = readxml.name;

 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ echo "The value of name is: ${name_var}"

 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ echo "The​​ value of description is: ${readxml.description}"

 ​​ ​​ ​​ ​​ ​​ ​​ ​​​​ echo "The version is: ${readxml.parent.version}"

 ​​ ​​ ​​​​ }


    
  stage('Build'){
     def shared = new Shared()
      shared.startBuild()
    }
}
