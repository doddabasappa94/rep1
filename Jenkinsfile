pipeline {
    agent any
    parameters{
    choice(name: 'CHOICE', choices: ['Repo1', 'Repo2', 'All'], description: 'Which one you want checkout')}
    stages {
          stage ('checkout') {
              steps{
                  script {
                    switch(params.CHOICE) {
                        case "All":
                           stages{
                              stage('checkout 1'){
                                  parallel {
                                     stage('main of repo1 checkout') {
                                         steps{
                                               echo 'rep1 is executed'
                                               git branch: 'main', url: 'https://github.com/doddabasappa94/rep1.git'
                                         }
                                     }
                                     stage ('test Rep1') {
                                            echo 'repo 1 test done'
                                         }
                                  }
                              stage('checkout 2'){
                                  parallel {
                                      stage('main of repo2 checkout') {
                                         steps{
                                               echo 'rep2 is executed'
                                               git branch: 'main', url: 'https://github.com/doddabasappa94/rep2.git'
                                         }
                                     }
                                      stage ('test repo2') {
                                            echo 'repo 2 test done'
                                         }
                                  }
                                  }
                              }
                           };
                        break
                        case "Repo1":
                           stages{
                              stage('checkout 1'){
                                  parallel {
                                     stage('main of repo1 checkout') {
                                         steps{
                                               echo 'rep1 is executed'
                                               git branch: 'main', url: 'https://github.com/doddabasappa94/rep1.git'
                                         }
                                     }
                                     stage ('test Rep1') {
                                            echo 'repo 1 test done'
                                         }
                                  }
                              }
                           }:
                        break
                    }
                    

                           
                    }
                  }
          }
    }
}


