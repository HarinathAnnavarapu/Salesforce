pipeline {
  agent any
  stages {
    stage('Development') {
      steps {
        echo 'Development Phase'
      }
    }

    stage('QA') {
      steps {
        git 'https://github.com/HarinathAnnavarapu/Salesforce'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deployment phase'
        input(message: 'Manual Approval', id: 'Approve it', ok: 'Yes')
      }
    }

  }
}