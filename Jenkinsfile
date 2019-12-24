pipeline {
    agent {label: 'master'}
    tools {
        maven 'mvn-362'
    }
    stages {
        stage ('Compile Stage') {

            steps {                
                    bat 'mvn clean compile'                
            }
        }

        stage ('Testing Stage') {

            steps {                
                    bat 'mvn test'                
            }
        }        
       
    }    
    post {         
         always {
             junit '**/target/surefire-reports/TEST-*.xml'
        }              
    }
}
