pipeline {
    agent {
        label 's6'
    }
    stages {
        stage("GIT") {
            steps {
                git branch: 'feature', url: 'https://github.com/gopal-jogi/maven.git'
            }
        }
        stage("Run") {
            steps {
                sh "mvn clean install"
		sh "sh script.sh"
            }
        }
    }
}
