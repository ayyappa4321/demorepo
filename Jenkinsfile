node {
    stage('git clone') { 
	git branch: 'main', url: 'https://github.com/ayyappa4321/mymaven.git'
    }
	stage('maven version') {
	
       sh 'mvn -version'
    }
    stage('maven clean') {
	
       sh 'mvn clean'
    }
    stage('maven validate') {
       sh 'mvn validate'
    }
	
	stage('sonascan ') {
       sh 'mvn sonar:sonar -Dsonar.host.url=http://34.125.19.233:9000 -Dsonar.login=314f2c3b1cf8acec1ce99747c37339831cfc5127'
    }
	stage('maven compile') {
       sh 'mvn compile'
    }
	stage('maven test') {
       sh 'mvn test'
    }
	stage('maven package') {
       sh 'mvn package'
    }
	stage('maven deploy') {
       sh 'mvn deploy'
    }
}
