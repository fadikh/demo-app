pipeline {
  agent {
    node {
      label '35.187.73.174'
    }

  }
  stages {
    stage('Dependencies') {
      steps {
        sh 'echo npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'echo npm test'
      }
    }
    stage('build') {
      steps {
        sh 'echo npm run build'
      }
    }
    stage('Archive artifacts') {
      steps {
        archiveArtifacts(artifacts: '*.zip', allowEmptyArchive: true, caseSensitive: true, defaultExcludes: true)
      }
    }
  }
}