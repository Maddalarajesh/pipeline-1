pipeline { 
    agent any
    stages {
        stage('Git Checkout'){
            
                     steps{
                
                        script{
                            git branch: 'main', url: 'https://github.com/Maddalarajesh/pipeline-1.git'
                        }
                     }
                  }
                   stage('unit Testing'){
            
                      steps{
                
                       script{
                    
                         sh 'mvn test'
                       }
                          
                      }
                       
                   }
              
    }
}
