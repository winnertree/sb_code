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
    
         stage('Checkout Github') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [],
                userRemoteConfigs: [[credentialsId: GITCREDENTIAL, url: GITWEBADD]]])
            }
            post {
                failure {
                    echo 'Repository clone failure'
                }
                success {
                    echo 'Repository clone success'
                }

            }
        }
        
        stage('build') {
            steps {
                sh "mvn clean package"
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