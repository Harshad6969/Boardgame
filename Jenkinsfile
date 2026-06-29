pipeline {
    agent any 
    
    tools {
        // Removed the colon here
        jdk 'jdk17' 
        // Ensure 'maven3' matches your Global Tool Configuration name
         
    }
    
    // There is only ONE 'stages' block wrapping all individual stages
    stages {
        
        stage('github project') {
            steps {
                git branch: 'main', url: 'https://github.com/Harshad-DevOps-Master/Boardgame_new.git'
            }
        }
        
        stage('compile') {
            steps {
                sh "mvn compile"
            }
        }
        
        stage('test') {
            steps {
                sh "mvn test"
            }
        }
        
        stage('package') {
            steps {
                sh "mvn package"
            }
        }
        
    } // End of stages
}
