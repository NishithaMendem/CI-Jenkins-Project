pipeline {
    agent any

    stages {
        stage('Check Python') {
            steps {
                bat '"C:\\Users\\Nishitha\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" --version'
            }
        }

        stage('Run Application') {
            steps {
                bat '"C:\\Users\\Nishitha\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
            }
        }

        stage('Run Unit Tests') {
            steps {
                bat '"C:\\Users\\Nishitha\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" test_app.py'
            }
        }
    }

    post {
        success {
            echo 'Build Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}