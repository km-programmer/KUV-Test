pipeline {

    agent any

    stages {

        stage('Clone') {

            steps {

                git 'https://github.com/km-programmer/KUV-Test.git'

            }

        }

        stage('Build') {

            steps {

                sh echo 'Building the project...,,,'

            }

        }

        stage('Test') {

            steps {

                sh echo 'Running tests...'

            }

        }

        stage('Deploy') {

            steps {

                sh echo 'Deploying...'

            }

        }

    }

}
 
