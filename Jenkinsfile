pipeline {
    agent {
        label 'slave1'
    }
    stages {
        stage("GIT") {
            steps {
                git "https://github.com/gopal-jogi/Jenkins_practice.git"
            }
        }
        stage("Run") {
            steps {
                sh "mvn clean install"
            }
        }
    }
}
