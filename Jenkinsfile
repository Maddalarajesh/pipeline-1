pipeline {
    agent any
    stages {
        stage('GitCheckout') {
            git branch: 'main', url: 'https://github.com/Maddalarajesh/pipeline-1.git'
            steps {
                echo "We're not doing anything particularly special here."
            }
        }
    }
}
