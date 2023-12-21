pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh '''if id "$USERNAME" &>/dev/null; then
    echo "true"
else
    echo "false"
fi
'''
      }
    }

  }
  environment {
    USERNAME = 'user'
  }
}