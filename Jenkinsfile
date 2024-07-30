import ExampleA.Shared

def agentName = 'linux && docker'
def someText = 'Hello!'

node(agentName) { //run this part on an agent with label 'linux'
    stage('Checkout') {
        checkout scm
       /* def shared = new Shared()
        shared.CheckoutGit()*/
    }

    stage('Update Version') {
            steps {
                script {
                    // Формування номера версії, можна змінити формат відповідно до ваших потреб
                    def buildNumber = "1.0-${env.BUILD_NUMBER}"  // Наприклад: "1.0-42"
                    
                    // Виклик функції з бібліотеки для оновлення версії
                    org.example.PomUtils.patchPom(buildNumber)
                }
            }
        }
    
  stage('Build'){
     def shared = new Shared()
      shared.startBuild()
    }
}
