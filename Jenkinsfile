pipeline {
    agent any

    stages {
        stage('ChekoutProject') {
            steps {
                sh 'docker --version'
            }
        }
        stage('BuildImage'){
          steps{
               sh 'docker build -t tindog .'
          }
        }
        stage('RunProject'){
          steps{
               sh 'docker run -dt -p 4200:4200 tindog'
          }
        }
    }
}
