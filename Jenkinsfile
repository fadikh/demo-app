pipeline {
  agent {
    node {
      label '35.187.73.174'
    }

  }
  stages {
    stage('Dependencies') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('build') {
      steps {
        sh 'npm run build'
      }
    }
    stage('Archive artifacts') {
      steps {
        archiveArtifacts(artifacts: '*.zip', allowEmptyArchive: true, caseSensitive: true, defaultExcludes: true)
      }
    }
  }
}