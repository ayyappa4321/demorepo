pipeline {
    agent any

    tools {
	maven 'maven'
        
    }

    stages {
        stage('maven version') {
            steps {
                sh ' mvn -version'
            }
        }
		stage('git clone') { 
		    steps{
	         git branch: 'main', url: 'https://github.com/ayyappa4321/mymaven.git'
            } 
		}	
	
    stage('maven clean') {
	        steps{
       sh 'mvn clean'
            }
		}	
    stage('maven validate') {
	        steps{
       sh 'mvn validate'
            }
	    }
	stage('sonascan ') {
	    steps{
       sh 'mvn sonar:sonar -Dsonar.host.url=http://34.125.30.16:9000 -Dsonar.login=314f2c3b1cf8acec1ce99747c37339831cfc5127'
         }
		} 
	stage('maven compile') {
	         steps{
       sh 'mvn compile'
            }
		}   
	stage('maven test') {
	     steps{
       sh 'mvn test'
    }
	}
	stage('maven package') {
	       steps{
       sh 'mvn package'
    }
	}
	stage('maven deploy') {
         steps{     
	 sh 'mvn deploy'
    }
	}
	
	
            
        
    }
}