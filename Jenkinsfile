pipeline {
    agent any
    stages {
        stage('Pull from GitHub') {
            steps {
                git 'https://github.com/a250026-creator/demo.git'
            }
        }

        stage('Kill Old Node Process') {
            steps {
                bat 'taskkill /F /IM node.exe || exit 0'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run Node App') {
            steps {
                bat 'start cmd /k npm start'
            }
        }
    }
}