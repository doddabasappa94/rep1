pipeline {
    agent any
    parameters{
    choice(name: 'CHOICE', choices: ['Repo1', 'Repo2', 'All'], description: 'Which one you want checkout')}
    stages {
          stage ('checkout') {
              steps{
                  script {
                    switch(params.CHOICE) {
                        case "Repo1":
                        git branch: 'main', url: 'https://github.com/doddabasappa94/rep1.git';
                        break
                        case "Repo2": 
                        git branch: 'main', url: 'https://github.com/doddabasappa94/rep2.git'; 
                        break
                        case "All":
                        git branch: 'main', url: 'https://github.com/doddabasappa94/rep1.git'
                        git branch: 'main', url: 'https://github.com/doddabasappa94/rep2.git'; 
                        break
                    }
              }
              
          }
  }
}
