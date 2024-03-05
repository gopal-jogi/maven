pipeline {
    agent {
        label 's6'
    }
    stages {
        stage("mvn") {
            steps {
                git branch: 'main', url: 'https://github.com/gopal-jogi/maven.git'
		sh "mvn clean install"
            }
        }
        stage("sh") {
            steps {
                git branch: 'feature', url: 'https://github.com/gopal-jogi/maven.git'
		sh "sh script.sh"
            }
        }
    }
}
