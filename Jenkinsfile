pipeline {
    agent any
    
    tools {
        maven "M3"
    }
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/terbeee/lbg-hello-world-maven.git'
            }
        }
        stage('Compile'){
            steps {
                sh "mvn clean compile"
            }
        }
        stage ('Test') {
            steps {
                sh "mvn test"
            }
        }
        stage('Package') {
            steps {
                sh "mvn -Dmaven.test.skip -Dmaven.compile.skip package"
            }
        }
    }
}
