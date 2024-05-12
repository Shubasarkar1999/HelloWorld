pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Shubasarkar1999/HelloWorld.git'
            }
        }
        stage('Build') {
            steps {
                sh 'javac -d . *.java'
                sh 'jar cf HelloWorld.jar *.class'
            }
        }
        stage('Publish') {
            steps {
                archiveArtifacts artifacts: 'HelloWorld.jar', fingerprint: true
            }
        }
    }
}
