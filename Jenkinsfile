pipeline {
    agent any

    stages {
        stage('Code') {
            steps {
              git 'https://github.com/satyajit929/satyajit_Flipkart.git'
            }
        }
        stage('code-build') {
            steps {
                 sh "mvn clean package"
            }
        }
        stage('Image-build') {
            steps {
                sh 'docker build -t tomcat:app .'
            }
        }
        stage('Deploy') {
            steps {
              sh 'docker run -itd --name app1 -p 8081:8080 tomcat:app'
            }
        }
    }
}
