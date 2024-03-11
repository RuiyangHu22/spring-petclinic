pipeline {
    agent any
    

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
        stage('Deploy'){
            steps{
                echo 'deploying'
            }

    
        
}
        
    
}
