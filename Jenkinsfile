pipeline {
    agent any
    tools {
        gradle ‘gradle-8’ // lub inna zainstalowana wersja
    }
    stages {
        stage('Start') {
            steps {
                echo 'Rozpoczynam pipeline...'
            }
        }

        stage('Checkout') {
            steps {
                git url: 'https://github.com/lukaszgolojuch/PlaywrightTests', branch: 'main'
            }
        }

        stage('Test') {
            steps {
                echo 'Uruchamiam testy'
                bat './gradlew clean test'
            }
        }

    }

}