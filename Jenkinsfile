pipeline {
    agent any
    tools {
        maven 'M1'
    }
    stages {
        stage ('Checkout') {
            steps {
                git 'https://github.com/davidmoten/maven-demo.git'
            }
        }
        stage ('Compile') {
            steps {
                sh 'mvn --version'
                sh 'mvn compile'
            }
        }
        stage ('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage ('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage ('Package') {
            steps {
                sh 'mvn package'
                echo
                echo 'packaged the .jar file to the target folder'
            }
        }
    }
}
