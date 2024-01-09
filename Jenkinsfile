pipeline {
    agent any
    
    tools {
        maven 'my_maven'
    }
    
    environment {
        GITNAME = 'winnertree' 
        GITEMAIL = 'winnertree@naver.com'
        GITWEBADD = 'https://github.com/winnertree/sb_code.git' 
        GITSSHADD = 'git@github.com:winnertree/sb_code.git'
        GITCREDENTIAL = 'git_cre'  
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}