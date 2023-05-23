pipeline { 
    agent any
    stages { 
        stage ('Cleanup Workspace') {
            steps {
                script {
                    cleanWs ()
                }
            }
        }
              stages {
        
                  stage('Git Checkout'){
            
                     steps{
                
                        script{
                            git branch: 'main', url: 'https://github.com/Maddalarajesh/pipeline-1.git'
                        }
                     }
                  }
              }
    }
}
