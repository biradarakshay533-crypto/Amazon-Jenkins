pipeline {
    agent any

    tools {
        maven 'maven3'
        jdk 'jdk21'
    }

    stages {
        stage('clean stage') {
            steps {
                sh 'mvn -B clean'
            }
        }

        stage('compile stage') {
            steps {
                sh 'mvn -B compile'
            }
        }

        stage('test stage') {
            steps {
                sh 'mvn -B test'
            }
        }

        stage('build and install stage') {
            steps {
                sh 'mvn -B clean install'
            }
        }
    }

    post {
        success {
            echo 'dev1 branch pipeline finished successfully.'
        }
        failure {
            echo 'Jenkinsfile pipeline failed.'
        }
    }
}
