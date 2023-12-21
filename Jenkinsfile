pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh 'git clone https://github.com/abesrour1111/git_devops.git'
      }
    }

    stage('stage2') {
      steps {
        sh '''if test -f "git_devops/gestion_groupes" && test -f "git_devops/gestion_utilisateurs"; then
    echo "Les deux fichiers existent"
else
    echo "L\'un des fichiers ou les deux fichiers sont manquants"
fi'''
      }
    }

    stage('stage3') {
      parallel {
        stage('stage3') {
          steps {
            sh 'grep -E \'useradd|usermod|userdel\' git_devops/fichier.txt'
          }
        }

        stage('') {
          steps {
            sh 'grep -E \'groupadd|groupmod|groupdel\' git_devops/fichier.txt'
          }
        }

      }
    }

  }
}