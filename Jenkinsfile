pipeline {
    agent any
    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/<username>/<repository>.git'
            }
        }
        stage('Compile JAR') {
            steps {
                sh 'javac HelloWorld.java'
                sh 'jar cvf HelloWorld.jar HelloWorld.class'
            }
        }
    }
}
