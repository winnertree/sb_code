pipeline {
    agent any
    
    tools {
        maven 'my_maven'
    }
    
    environment {
        GITNAME = 'winnertree' # 깃허브 계정
        GITEMAIL = 'winnertree@naver.com'
        GITWEBADD = 'https://github.com/winnertree/sb_code.git' # 레포 주소
        GITSSHADD = 'git@github.com:winnertree/sb_code.git'
        GITCREDENTIAL = 'git_cre'   # 젠킨스 credential
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