pipeline {
    agent any 
    tools {
        maven 'M2_HOME'
    }
    stages{
        stage('sonarqube scan'){
            steps{
              withSonarQubeEnv (sonarserver)
                sh 'mvn verify org.sonarsource.scanner.maven:sonar-maven-plugin:sonar -Dsonar.projectKey=dimitri2399_geo'
            }
        }
        stage('all maven commands'){
            steps{
                sh 'mvn clean test compile install package'
            }
        }
        
    }
}