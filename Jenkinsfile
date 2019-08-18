pipeline{
    agent any

    tools{maven 'Maven2'
        jdk 'java8'
    }

    stages{
        stage('init'){
            steps{
                echo "init stage"
            }
        }
        stage('Build'){
            steps{
                echo "This is Build stage"
                sh label: '', script: 'mvn clean package checkstyle:checkstyle'

                echo "Check style result"
                checkstyle canComputeNew: false, defaultEncoding: '', healthy: '', pattern: '', unHealthy: ''
            }
        }
        stage('Deploy'){
            steps{
                echo "This is Deploy stage"
            }
        }
    }

}