pipeline {
    agent any

    stages {
        stage('Cloner le dépôt') {
            steps {
                git branch: 'main', url: 'https://github.com/AyaSaied26/School.git'
            }
        }

        stage('Construire avec Maven') {
            steps {
                sh 'mvn clean install'
            }
        }
    }
}
