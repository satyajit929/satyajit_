pipeline {
    agent any

    stages {
        stage('Code') {
            steps {
              git 'https://github.com/satyajit929/satyajit_.git'
            }
        }
        stage('code-build') {
            steps {
                 sh "mvn clean package"
            }
        }
        stage('Artifactory') {
            steps {
                sh 'echo "Uploading artifact to Artifactory..."'
            }
        }
        stage('Deploy') {
            steps {
              sh 'docker run -itd --name app1 -p 8081:8080 tomcat:app'
            }
        }
    }
}
