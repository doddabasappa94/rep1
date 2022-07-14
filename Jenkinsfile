pipeline {
    agent any
    stages {
          stage ('Repo1 checkout') {
              steps{
              checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/doddabasappa94/repo1.git']]])  
              }
          }
  }
}
