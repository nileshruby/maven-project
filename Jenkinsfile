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

                echo "Test Build Report"
                junit '**/TEST-*.xml'

                echo "Archive WebApp"
                archive '**/webapp.war'
            }
        }
        stage('Deploy'){
            steps{
                timeout(activity: true, time: 90, unit: 'SECONDS') {
    // some block
     input 'Do you want to continue deploy on dev server?'
}
               
                echo "This is Deploy stage"

            }
        }
    }

}