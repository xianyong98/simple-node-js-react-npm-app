pipeline {
   agent {
        docker {
            image 'hello-world'
            args '-p 3000:3000'
        }
    }
    tools{
        nodejs 'Nodejs'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
