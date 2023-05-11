pipeline {
  agent any
  stages {
    stage('Stage1') {
      steps {
        sh '''sudo apt-get update -y



'''
      }
    }

    stage('Stage2') {
      steps {
        sh 'dpkg -1 > /tmp/paquets'
      }
    }

    stage('Stage3') {
      steps {
        sh '''if [ \'grep -c git /tmp/paquets\' -ne 0]
then
dpkg -s git
else
sudo apt-get install -y git
fi'''
      }
    }

  }
}