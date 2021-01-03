pipeline {
  agent any
  stages {
    stage('Development') {
      steps {
        echo 'Development Phase'
        emailext(subject: 'Development Phase', body: 'Hi, This is regarding the build details taken place at Development phase', attachLog: true, from: 'haridece23@gmail.com', replyTo: 'haridece23@gmail.com,harinathannavarapu@gmail.com', to: 'harinathannavarapu@gmail.com')
      }
    }

    stage('QA') {
      steps {
        git 'https://github.com/HarinathAnnavarapu/Salesforce'
        mail(subject: 'QA Phase mail', body: 'This is the stage where QA phase is taken place', from: 'haridece23@gmail.com', to: 'haridece23@gmail.com', replyTo: 'harinathannavarapu@gmail.com', cc: 'harinathannavarapu@gmail.com')
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