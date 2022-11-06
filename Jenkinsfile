pipeline {
    agent any
    tools {
            maven 'mavenhome'
         }	
    stages {
	
        stage('MAVEN-BUILD') { 
            steps {
                sh 'mvn  compile' 
            }
        }
        stage('Mavev-Test') { 
            steps {
                sh 'mvn clean test' 
            }
        }
        stage('Maven-package') { 
            steps {
                sh 'mvn package -DskipTests' 
            }
        }
		 
		 	
    }

}

