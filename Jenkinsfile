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
        sh 'dpkg -l > /tmp/paquets'
      }
    }

    stage('Stage3') {
      steps {
        sh '''if [ $(grep -c git /tmp/paquets) -ne 0 ]
then
dpkg -s nano
else
sudo apt-get install -y nano
fi'''
      }
    }

  }
}