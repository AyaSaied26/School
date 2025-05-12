pipeline {
    agent any

    stages {

        stage('Cloner le dépôt') {
            steps {
                // Cloner le dépôt GitHub
                git url: 'https://github.com/AyaSaied26/School.git'
            }
        }

        stage('Construire avec Maven') {
            steps {
                // Nettoyer et construire le projet avec Maven
                sh 'mvn clean install'
            }
        }

    }
}
