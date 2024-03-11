pipeline {
    agent any
    

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/RuiyangHu22/spring-petclinic.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        
}
        
    
}
