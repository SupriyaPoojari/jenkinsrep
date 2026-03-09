pipeline {
    agent any

    stages {
        stage('Fetch File from my repo') {
            steps {
                git branch: 'main', url: 'https://github.com/SupriyaPoojari/jenkinsrep.git'
            }
            
        }
        stage('build my file'){
            steps {
                echo 'Build Project'
                bat 'javac jen.java'
               
            }
        }
        stage('Execute'){
            steps {
                echo 'Executingg'
                bat 'java jen'
            }
        }
        stage('Deploy'){
            steps {
                echo 'Deploying'
               
            }
        }
    }
    post{
        success{
            echo 'pipeline successful'
        }
        failure{
            echo 'pipeline failed'
        }
    }
}
