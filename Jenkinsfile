pipeline {
    agent any 
    stages {
        stage('clone repo and clean it') { 
            steps {
                bat "rm -rf my-app"
                bat "git clone https://github.com/hamid79/my-app.git"
                bat "mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
               bat "mvn test -f my-app"
            }
        }
        stage('Deploy') { 
            steps {
                bat "mvn package -f my-app" 
            }
        }
    }
}
