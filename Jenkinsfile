pipeline {
    agent any
    stages {
        stage('CI') {
            steps {
                echo 'CI'
            }
        }
        stage('UAT deploy') {
            steps {
                echo 'UAT deploy'
            }
        }
        stage('UAT test') {
            parallel {
                stage('UAT unit test') {
                    steps {
                        echo 'UAT unit tests'
                    }
                }
                stage('UAT functional test') {
                    steps {
                        echo 'UAT functional tests'
                    }
                }
            }
        }   
        stage('PROD') {
            steps {
                echo 'PROD'
            }
        }
    }
}