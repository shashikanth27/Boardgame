pipeline {
    agent any
    
    tools {
        maven 'maven'
        jdk 'jdk17'
    }

    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/shashikanth27/Boardgame.git'
            }
        }
        
       stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn package -DskipTests'
            }
        }
        
        stage('Install') {
            steps {
                sh 'mvn install -DskipTests'
            }
        }
        
        
    }
}
