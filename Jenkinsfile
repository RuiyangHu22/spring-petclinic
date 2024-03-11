pipeline {
    agent any
    
    triggers {
        cron('H */10 * * 1') // Run every 10 minutes on Mondays
    }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        
        
        
    
}
