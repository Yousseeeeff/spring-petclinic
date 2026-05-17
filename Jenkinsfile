pipeline {
    agent any
    tools {
        maven 'Maven'
        jdk 'JDK21'
    }
    stages {

        stage ('Build') {
            steps {
                bat 'mvn install'
            }
            post {
                success {

                    junit 'target/surefire-reports/**/*.xml'
                }
            }
        }
    }
}
