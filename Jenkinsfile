pipeline {
    agent any 
    tools {
        maven 'M2_HOME'
    }
    stages{
        stage('sonarqube scan'){
            steps{
                sh 'mvn sonar:sonar'
            }
        }
        stage('all maven commands'){
            steps{
                sh 'mvn clean test compile install package'
            }
        }
        
    }
}