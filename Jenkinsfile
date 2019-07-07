pipeline{
    agent{label '35.187.73.174'}
    stages{
        stage('Get Sources'){
            steps{
                git 'https://github.com/fadikh/demo-app.git'
            }
        }
        stage('Restore Dependencies'){
            steps{
                sh label: '', script: 'npm install'
            }
        }
        stage('Test'){
            steps{
                sh label: '', script: 'npm test'
            }
        }
        stage('Package'){
            steps{
                sh label: '', script: 'npm run build'
            }
        }
        stage('Archive artifacts'){
            steps{
                archiveArtifacts '*.zip'
            }
        }
    }
}
