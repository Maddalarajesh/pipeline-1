pipeline {
    agent any
    stages {
        stage('git checkout') {
            git branch: 'main', url: 'https://github.com/Maddalarajesh/pipeline-1.git'
          steps {
               sh 'git'
            }
        }
    }
}
