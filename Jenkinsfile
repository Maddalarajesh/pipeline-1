pipeline { 
    agent any
    stages {
        stage('Git Checkout'){
            
                     steps{
                
                        script{
                            git 'https://github.com/Maddalarajesh/hello-world.git'
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
                   stage('Integration testing'){
            
            steps{
                
                script{
                    
                    sh 'mvn verify -DskipUnitTests'
                }
            }
        }
        stage('Maven build'){
            
            steps{
                
                script{
                    
                    sh 'mvn clean install'
                }
            }
        }
        stage('deploy'){
            
            steps{
                  sshagent(['deploy']) {
                    sh 'scp -o StrictHostKeyChecking=no webapp/target/webapp-2.war ec2-user@3.108.194.134:/home/ec2-user/apache-tomcat-8.5.89/webapps '
            }
        }
              
    }
}
}
