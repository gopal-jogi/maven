pipeline {
    agent {
        label 's5'
    }
    stages {
        stage("GIT") {
            steps {
                git branch: 'main', url: 'https://github.com/gopal-jogi/maven.git'
            }
        }
        stage("Run") {
            steps {
                sh "mvn clean install"
            }
        }
    }
}
