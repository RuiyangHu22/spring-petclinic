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
        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Generate Code Coverage Report') {
    steps {
        // Generate code coverage report using Jacoco
        sh './mvnw clean test jacoco:report'
    }
    post {
        always {
            // Publish code coverage report
            jacoco(execPattern: '**/target/**.exec', classPattern: '**/target/classes', sourcePattern: '**/src/main/java', exclusionPattern: '**/*Test.class', inclusionPattern: '**/*.class')
        }
    }
}
        
    }
}
