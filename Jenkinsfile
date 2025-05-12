pipeline {
    agent any

    environment {
        DOCKER_IMAGE = 'school-project:latest'
    }

    stages {

        stage('Cloner depuis GitHub') {
            steps {
                git branch: 'main', url: 'https://github.com/AyaSaied26/School.git'
            }
        }

        stage('Build Maven') {
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh "docker build -t ${DOCKER_IMAGE} ."
            }
        }

        stage('Afficher les images Docker') {
            steps {
                sh 'docker images'
            }
        }

    }

    post {
        success {
            echo 'Le pipeline a réussi !'
        }
        failure {
            echo 'Le pipeline a échoué.'
        }
    }
}
