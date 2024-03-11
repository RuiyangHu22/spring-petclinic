pipeline {
    agent any
    
    triggers {
        cron('H */10 * * 1') // Run every 10 minutes on Mondays
    }

    stages {
        stage('Check out') {
            steps {
                git url: 'https://github.com/RuiyangHu22/spring-petclinic.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Generate Code Coverage Report') {
            steps {
                sh 'mvn jacoco:report'
            }
            post {
                always {
                    jacoco '**/target/site/jacoco/jacoco.xml'
                }
            }
        }
        
    }
}
