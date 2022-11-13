pipeline {
   agent any
    tools{
        nodejs 'Nodejs'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
                sh 'npm start' 
            }
        }
        stage('Deliver') { 
            steps {
                sh './jenkins/scripts/deliver.sh' 
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                sh './jenkins/scripts/kill.sh' 
            }
    }
}
