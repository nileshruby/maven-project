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
            }
        }
        stage('Deploy'){
            steps{
                echo "This is Deploy stage"
            }
        }
    }

}