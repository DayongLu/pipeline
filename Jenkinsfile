pipeline {
    agent any

    stages {
        stage('build-test'){
            steps {
                echo 'Checkout from Repo'

                git credentialsId: '6e08ec68-b60e-478c-8956-629fe8ace709', url: 'https://github.com/DayongLu/greeting-service.git'

                withMaven(maven: 'maven352'){
                    sh 'mvn clean package'
                }
            }
        }
            
        stage('Integration-Test'){
            steps {
                echo 'Running Integration Test'

                junit 'reports/**/*.xml'

            }
        }
            
        stage('Deploy-To-DEV'){
            steps {
                echo 'Deploy-To-DEV'
                
                

            }
        }


        
    }
}
